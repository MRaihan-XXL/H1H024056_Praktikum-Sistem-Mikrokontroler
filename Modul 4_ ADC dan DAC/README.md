# Pertemuan 4

## 3.5.4 Percobaan 4A: Analog to Digital Converter (ADC)

1. Apa fungsi perintah analogRead() pada rangkaian praktikum ini?

> User mengetik karakter di Serial Monitor Arduino IDE, kemudian menekan enter. Komputer mengirimkan karakter tersebut melalui kabel USB ke Arduino. Di dalam loop(), Serial.available() mendeteksi adanya data (bernilai >0). char data = Serial.read() membaca satu karakter. Program membandingkan data dengan '1' atau '0'. Jika cocok, digitalWrite(PIN_LED, HIGH/LOW) mengubah status LED. Arduino mengirim balasan "LED ON" atau "LED OFF" ke Serial Monitor sebagai konfirmasi.

2. Mengapa diperlukan fungsi map() dalam program tersebut?

> Serial.available() digunakan untuk mengecek apakah ada data yang masuk ke buffer serial. Jika tidak ada, program tidak perlu membaca karena Serial.read() akan mengembalikan nilai -1 yang dapat menyebabkan error logika sehingga program menjadi tidak efisien (banyak pembacaan percuma).

3. Modifikasi program berikut agar servo hanya bergerak dalam rentang 30° hingga 150°, meskipun potensiometer tetap memiliki rentang ADC 0–1023. Jelaskan program pada file README.md 

```c++
// Modifikasi 3A: LED berkedip saat input '2', berhenti saat input '0'
#include <Arduino.h>

const int PIN_LED = 12;
bool blinkMode = false;   // status mode berkedip
unsigned long previousMillis = 0;
const long interval = 500; // jeda 500ms
bool ledState = false;

void setup() {
    Serial.begin(9600);
    Serial.println("Ketik '1' (ON), '0' (OFF), '2' (BLINK)");
    pinMode(PIN_LED, OUTPUT);
}

void loop() {
    // Baca perintah dari serial
    if (Serial.available() > 0) {
        char data = Serial.read();
        if (data == '1') {
            blinkMode = false;
            digitalWrite(PIN_LED, HIGH);
            Serial.println("LED ON");
        }
        else if (data == '0') {
            blinkMode = false;
            digitalWrite(PIN_LED, LOW);
            Serial.println("LED OFF");
        }
        else if (data == '2') {
            blinkMode = true;
            Serial.println("BLINK MODE ON");
        }
        else if (data != '\n' && data != '\r') {
            Serial.println("Perintah tidak dikenal");
        }
    }
    
    // Jika mode blink aktif, lakukan kedip tanpa delay() blocking
    if (blinkMode) {
        unsigned long currentMillis = millis();
        if (currentMillis - previousMillis >= interval) {
            previousMillis = currentMillis;
            ledState = !ledState;
            digitalWrite(PIN_LED, ledState);
        }
    }
}
```

## 3.6.4 Percobaan 4B: Pulse Width Modulation (PWM)

1. Jelaskan mengapa LED dapat diatur kecerahannya menggunakan fungsi analogWrite()!

> Hanya terdapat dua kabel: SDA (data) dan SCL (clock). Arduino mengirimkan alamat slave (0x27) terlebih dahulu untuk "memanggil" LCD. Setelah LCD merespon dengan acknowledge (ACK), Arduino mengirimkan perintah atau data (misal inisialisasi, set kursor, karakter). Library LiquidCrystal_I2C.h menyembunyikan detail ini. Fungsi lcd.print() akan mengirimkan data karakter ke alamat 0x27 melalui bus I2C. Karena I2C adalah protokol sinkron, clock (SCL) diatur oleh Arduino agar kedua perangkat sinkron. Keuntungan: dengan 2 kabel, bisa dihubungkan banyak slave (masing-masing dengan alamat unik).

2. Apa hubungan antara nilai ADC (0–1023) dan nilai PWM (0–255)?

> Potensiometer tetap berfungsi, tetapi arah putaran menjadi terbalik. Artinya, jika diputar searah jarum jam biasanya nilai ADC naik (0→1023), setelah tertukar akan turun (1023→0). Secara teknis tidak merusak, hanya membalik skala. Nilai maksimum dan minimum tetap sama (0 dan 1023). Untuk aplikasi yang menginginkan arah tertentu (misal kanan = naik), perlu disesuaikan.

3. Modifikasilah program berikut agar LED hanya menyala pada rentang kecerahan sedang, yaitu hanya ketika nilai PWM berada pada rentang 50 sampai 200. Jelaskan program pada file README.md.

```c++
// Modifikasi 3B: Tampilan ke Serial Monitor dan LCD dengan format rapi
#include <Wire.h>
#include <LiquidCrystal_I2C.h>
#include <Arduino.h>

LiquidCrystal_I2C lcd(0x27, 16, 2);
const int pinPot = A0;

void setup() {
    Serial.begin(9600);
    lcd.init();
    lcd.backlight();
}

void loop() {
    int nilaiADC = analogRead(pinPot);
    if (nilaiADC < 1) nilaiADC = 1;   // hindari pembagian nol (opsional)
    
    float tegangan = (nilaiADC / 1023.0) * 5.0;
    int persen = map(nilaiADC, 0, 1023, 0, 100);
    
    // --- Serial Monitor format sesuai tabel (UART) ---
    Serial.print("ADC: ");
    Serial.print(nilaiADC);
    Serial.print(" Volt: ");
    Serial.print(tegangan, 2);
    Serial.print(" V Persen: ");
    Serial.print(persen);
    Serial.println("%");
    
    // --- LCD baris 1: "ADC: nilai persen%" (I2C) ---
    lcd.setCursor(0, 0);
    lcd.print("ADC: ");
    lcd.print(nilaiADC);
    lcd.print(" ");
    lcd.print(persen);
    lcd.print("%   ");   // hapus sisa karakter
    
    // --- LCD baris 2: bar grafis (I2C) ---
    int panjangBar = map(nilaiADC, 0, 1023, 0, 16);
    lcd.setCursor(0, 1);
    for (int i = 0; i < 16; i++) {
        if (i < panjangBar) {
            lcd.print((char)255);   // blok
        } else {
            lcd.print(" ");
        }
    }
    
    delay(200);
}
```
