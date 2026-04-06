# Praktikum-Sistem-Mikrokontroler
<div align="center">
  <img width="791" height="222" alt="g9" src="https://github.com/user-attachments/assets/aad932ac-5ed9-4cbe-bd83-e55935355433" />
</div>
<br>
<p>Mikrokontroler adalah inti sistem embedded. Mikrokontroler hanyalah IC tunggal yang tidak dapat langsung digunakan tanpa rangkaian pendukung. Project board hadir sebagai solusi untuk mempermudah proses belajar dan eksperimen. Arduino merupakan project board yang mengintegrasikan mikrokontroler dengan rangkaian pendukung sehingga siap digunakan.</p>

<p>Untuk memahami Arduino, terlebih dahulu kita harus memahami terlebih dahulu apa yang dimaksud dengan physical computing. Physical computing adalah membuat sebuah sistem atau perangkat fisik dengan menggunakan software dan hardware yang sifatnya interaktif yaitu dapat menerima rangsangan dari lingkungan dan merespon balik. Arduino dikatakan sebagai sebuah platform dari physical computing yang bersifat open source.</p>

![arduino-build-electronic-projects](https://github.com/user-attachments/assets/9c957307-ebdd-406d-b533-31d6843b19f5)

<h2>🔗 Mengapa Mempelajari Physical Computing?</h2>

Physical computing dipelajari karena memungkinkan komputer berinteraksi langsung dengan dunia fisik melalui sensor dan aktuator, sehingga komputasi tidak lagi terbatas pada layar, tetapi hadir secara kontekstual, cerdas, dan bermakna dalam kehidupan nyata. Selain itu, mempelajari physical computing karena adanya tiga tren teknologi dan sosial yang saling berkaitan:
<ul>
  <li>Physical computing menjadi sangat relevan saat ini karena perkembangan teknologi dan perubahan cara manusia berinteraksi dengan komputer. Gerakan DIY dan komunitas maker membuat perangkat keras seperti Arduino mudah diakses oleh siapa saja, sehingga kita bisa dengan cepat membuat dan menguji sistem yang menggabungkan bentuk fisik dan komputasi. Selain itu, banyak tutorial dan sumber belajar tersedia secara gratis di internet.</li>
  <li>Komputer tidak lagi hanya berbentuk PC atau laptop. Smartphone dan perangkat IoT selalu aktif dan berada di sekitar kita, serta dilengkapi dengan berbagai sensor yang memungkinkan komputer memahami gerakan, posisi, dan kondisi lingkungan. Hal ini membuka peluang interaksi baru yang tidak bergantung pada layar, keyboard, atau mouse.</li>
  <li>Kemajuan machine learning dan computer vision memungkinkan data dari sensor diolah secara cerdas untuk menciptakan interaksi manusia–komputer yang lebih alami, tanpa mengharuskan pengguna menjadi ahli di bidang kecerdasan buatan.</li>
</ul>

Dengan kondisi ini, cara berinteraksi dengan komputer tidak lagi terbatas pada antarmuka grafis tradisional seperti jendela, ikon, menu, dan pointer. Physical computing menghadirkan model interaksi baru yang lebih kontekstual, alami, dan terhubung langsung dengan dunia fisik.

<h2>📚 Prasyarat Pembelajaran</h2>

<p>Untuk mengikuti materi ini, peserta diharapkan sudah memiliki pengalaman dasar dalam pemrograman, seperti memahami variabel, perulangan, fungsi, dan percabangan. Pemrograman mikrokontroler akan menggunakan bahasa C/C++, tetapi peserta tidak harus sudah menguasai C/C++ sebelumnya. Jika sudah pernah menggunakan bahasa seperti Java, C#, atau Python, proses belajar C/C++ akan relatif mudah karena konsep dasarnya serupa. Pada tahap lanjutan, peserta akan diperkenalkan pada konsep pemrograman yang lebih kompleks, seperti pengelolaan memori dan pembuatan library.</p>

<p>Di sisi lain, peserta lebih baik memiliki pengalaman di bidang perangkat keras atau elektronika. Meskipun materi akan dimulai dari dasar sehingga dapat diikuti oleh pemula di bidang hardware.</p>

<p>Physical computing merupakan bidang lintas disiplin yang menggabungkan banyak area keilmuan, seperti teknik elektro, ilmu komputer, interaksi manusia–komputer, dan kecerdasan buatan. Karena cakupannya sangat luas, materi yang disajikan difokuskan pada topik-topik inti yang relevan bagi mahasiswa dengan latar belakang teknik atau informatika.</p>

##💻 Install Arduino IDE
<p>Sebelum mulai memprogram Arduino, pastikan <a href="https://support.arduino.cc/hc/en-us/articles/360019833020-Download-and-install-Arduino-IDE">Arduino IDE</a> sudah terpasang di komputer Anda. Jika belum, unduh dan instal Arduino IDE dengan mengikuti panduan instalasi yang disediakan secara bertahap melalui tautan berikut <a href="https://support.arduino.cc/hc/en-us/articles/360019833020-Download-and-install-Arduino-IDE#installation-instructions">disini</a></p>

<p>Secara default jika IDE sudah berhasil diinstal dan dibuka, jendela awal akan memunculkan code sebagai berikut</p>

```cpp
void setup() {
  // put your setup code here, to run once:

}

void loop() {
  // put your main code here, to run repeatedly:

}
```

## 📄 Dokumentasi
<p>Sebagai tahap awal memulai menggunakan mikrokontroler Arduino Uno, secara lengkap dapat disimak pada dokumentasi yang telah disediakan oleh Arduino yang dapat diakses melalui <a href="https://docs.arduino.cc/tutorials/uno-rev3/getting-started/?_gl=1*i7yfbm*_up*MQ..*_ga*MTM4NzkzOTY3Ni4xNzcxMDc4MjAx*_ga_NEXN8H46L5*czE3NzEwNzgxOTgkbzEkZzAkdDE3NzEwNzgxOTgkajYwJGwwJGgyNzQ3MjQ5NQ..">Arduino Docs</a></p>

## 🗂️ Modul Praktikum Embedded System dan Mikrokontroler
Dalam modul ini berisi kegiatan berkesinambungan tentang penggunaan arduino uno sebagai project board untuk mikrokontroler baik secara teori maupun langkah-langkah pengerjaan. Berikut modulnya:

<h3><a href="/Modul 1: Percabangan dan Perulangan">Modul 1 : Percabangan dan Perulangan</a></h3>
<p>Praktikum ini mempelajari penggunaan percabangan dan perulangan pada pemrograman Arduino untuk mengontrol alur logika program dan menghasilkan perilaku sistem yang dinamis.</p>

<h3><a href="/Modul 2: Pemrograman Input Output">Modul 2 : Pemrograman Input Output</a></h3>
<p>Praktikum ini membahas penggunaan pin GPIO pada mikrokontroler sebagai input dan output untuk mengendalikan perangkat digital seperti LED dan membaca kondisi tombol, sehingga mahasiswa memahami dasar interaksi perangkat keras dengan program.</p>

<h3><a href="/Modul 3: Serial Communication">Modul 3: Komunikasi Serial</a></h3>
<p>Praktikum ini memperkenalkan komunikasi serial untuk pertukaran data antara mikrokontroler dan komputer, termasuk pengiriman dan penerimaan data melalui Serial Monitor sebagai sarana monitoring dan debugging sistem.</p>

<h3><a href="/Modul 4: ADC dan DAC">Modul 4: ADC dan DAC</a></h3>
<p>Praktikum ini mempelajari konversi sinyal analog ke digital (ADC) dan digital ke analog (DAC) pada mikrokontroler untuk membaca sensor analog dan menghasilkan keluaran analog sesuai kebutuhan aplikasi.</p>

<h3><a href="/Modul 5 : RTOS">Modul 5: Real-Time Operating System (RTOS)</a></h3>
<p>Praktikum ini memperkenalkan konsep dasar Real-Time Operating System (RTOS), termasuk pengelolaan task dan penjadwalan sederhana, untuk memahami pengembangan aplikasi multitasking pada sistem mikrokontroler.</p>

<h3><a href="/Modul 6 (Tambahan): Pengenalan IoT">Modul (Tambahan): Pengenalan Internet of Things</a></h3>
<p>Modul ini memperkenalkan dasar-dasar Internet of Things (IoT), yaitu konsep menghubungkan perangkat fisik ke internet untuk mengirim dan menerima data.
</p>

<p>Praktikum disusun berdasarkan pendekatan pemrograman mulai dari Bare-Metal Programming sampai dengan Real-Time Operating System (RTOS) dengan modul tambahan yaitu Pengenalan Internet of Things</p>

<h2>💡 Laporan Praktikum</h2>
<p>Setiap praktikum yang telah selesai dilakukan hasilnya dikumpulkan dalam bentuk laporan dan Kode yang digunakan melalui <a href="https://eldiru.unsoed.ac.id/">eLdiru</a> (ruang unggah disediakan dimasing-masing pertemuan) dengan format sebagai berikut:</p>
<p>Nama file laporan: [kode mata kuliah]_[modul ke]_[NIM] contoh TK2440005_01_H1H022001</p>

<p>Dikirimkan dalam bentuk attachment dengan format .pdf bentuk laporan seperti template berikut ini.</p>

<table border="1" align="center" width="100%" cellpadding="0" cellspacing="0">
  <tr>
    <td>
      <h2>
        <a href="https://docs.google.com/document/d/17EwpGksKAiaKBgLu6zKR_RNZT5vykKdZ/edit?usp=sharing&ouid=114215355724116733257&rtpof=true&sd=true">
          TEMPLATE LAPORAN PRAKTIKUM
        </a>
      </h2>
    </td>
  </tr>
</table>

<h2>📓 Buku Catatan Praktikum</h2>
<p>Buku catatan praktikum adalah catatan yang digunakan dalam eksperimen langsung di laboratorium yang memuat aktivitas selama praktikum berlangsung berisi rangkaian, kode dan hasil yang bertujuan sebagai dokumentasi percobaan.</p>

<p>Petunjuk pengisian Buku Catatan Praktikum adalah sebagai berikut:</p>
<ul>
  <li>Gunakan buku catatan ini hanya untuk keperluan lab</li>
  <li>Tulis identitas sesuai dengan format</li>
  <li>Mahasiswa mencatat hasil dan jawaban pertanyaan praktikum dengan pena bertinta, bukan pensil</li>
  <li>Bila terjadi terjadi kesalahan, coretlah bagian yang salah. Jangan menggunakan penghapus atau menutup (tip-ex) catatan yang salah</li>
  <li>Buat catatan berkesinambungan, jangan meninggalkan ruang atau halaman kosong</li>
  <li>Tutup bagian akhir catatan dengan memberikan garis</li>
  <li>Bila catatan terakhir satu modul hanya mengisi beberapa baris teratas saja, lanjutkan catatan berikutnya pada halaman yang sama</li>
  <li>Tidak diperkenankan untuk merobek buku catatan praktikum</li>
  <li>Tandatangani dan beri tanggal setiap halaman yang memiliki data</li>
  <li>Adapun hal yang perlu dicatat saat proses praktikum meliputi:</li>
  <ul>
    <li>Tujuan praktikum berdasarkan pemahaman praktikan setelah melakukan proses praktikum</li>
    <li>Gambar rangkaian setiap percobaan</li>
    <li>Penjelasan program yang digunakan</li>
    <li>Hasil pengamatan dan jawaban pertanyaan praktikum</li>
    <li>Catatan Kendala</li>
  </ul>
  <li>Catat semua kejadian, baik positif ataupun negatif, yang terjadi di lab</li>
  <li>Catat tidak hanya data, namun juga permasalahan yang ditemui pada alat yang digunakan, pengesetan peralatan, teknik pengukuran, atau prosedur penting yang disarankan manual lab</li>
  <li>Saat membuat grafik, beri label setiap sumbu grafik dengan nama variabel, satuan, origin (titik nol), dan skala.</li>
  <li>Asisten menandatangani dan memberi tanggal sebelum sesi lab selesai</li>
  <li>Tanggung jawab bersama antara asisten dan mahasiswa untuk memastikan data yang diambil sesuai dengan harapan sebelum mahasiswa meninggalkan setiap sesi lab</li>
</ul>

<table border="1" align="center" width="100%" cellpadding="0" cellspacing="0">
  <tr>
    <td>
      <h2>
        <a href="https://docs.google.com/document/d/1H7cjsJ31MNUCidYrXR4XzcVPMSk_7Lf-/edit?usp=sharing&ouid=114215355724116733257&rtpof=true&sd=true">
          TEMPLATE BUKU CATATAN PRAKTIKUM 
        </a>
      </h2>
    </td>
  </tr>
</table>

<h2>⚙️ Bagian-bagian Pada Arduino</h2>
<p>Dengan mengambil contoh sebuah papan Arduino tipe USB, bagian-bagiannya dapat dijelaskan sebagai berikut.</p>

![Pengenalan Arduino](https://github.com/user-attachments/assets/b8d8aeed-4793-41b2-be9a-198c81d6a4bb)

<p>Berikut penjelasan singkat terkai dengan fungsi bagian pada papan Arduino:</p>
<ol>
  <li><b>Mikrokontroler ATmega328P:</b> “Otak” Arduino. Bagian ini yang menjalankan program, memproses data, dan mengontrol semua komponen yang terhubung.</li>
  <li><b>Digital Pin I/O (Input/Output):</b> Pin untuk membaca atau mengirim sinyal digital (hanya 0 atau 1 / LOW atau HIGH). Contoh: menyalakan LED, membaca tombol.</li>
  <li><b>Analog Pin I/O:</b> Pin untuk membaca nilai analog (nilai bertingkat, bukan hanya 0 dan 1). Contoh: membaca sensor suhu, cahaya, atau potensiometer.</li>
  <li><b>Power Pin:</b> Pin untuk memberi daya listrik ke Arduino atau komponen lain (3.3V, 5V, GND)</li>
  <li><b>USB Connector:</b> Untuk menghubungkan Arduino ke komputer. Fungsinya upload program dan memberi daya.</li>
  <li><b>Serial Pin (Tx = Out, Rx = In):</b> Untuk komunikasi data dengan perangkat lain. Tx untuk mengirim data, Rx untuk menerima data</li>
  <li><b>Onboard LED:</b> LED bawaan Arduino (biasanya di pin 13). Digunakan untuk percobaan atau indikator program.</li>
  <li><b>Reset:</b> Tombol untuk mengulang program dari awal.</li>
  <li><b>USB Interface:</b> Bagian yang mengubah komunikasi USB dari komputer menjadi komunikasi serial agar bisa dipahami mikrokontroler.</li>
  <li><b>Power Connector (Jack DC):</b> Untuk memberi daya dari adaptor atau baterai eksternal.</li>
  <li><b>Oscillator:</b> Untuk memberi daya dari adaptor atau baterai eksternal.</li>
</ol>

<p>Tanpa melakukan konfigurasi apapun, begitu sebuah papan Arduino dikeluarkan dari kotak pembungkusnya ia dapat langsung disambungkan ke sebuah komputer melalui kabel USB. Selain berfungsi sebagai penghubung untuk pertukaran data, kabel USB ini juga akan mengalirkan arus DC 5 Volt kepada papan Arduino sehingga praktis tidak diperlukan sumber daya dari luar. Saat mendapat suplai daya, lampu LED indikator daya pada papan Arduino akan menyala menandakan bahwa ia siap bekerja. </p>

## ⛓️ Acknowledgments
Diagram, animasi, gambar, dan video dibuat menggunakan <a href="https://www.tinkercad.com/">Tinkercad Circuits</a>, <a href="https://fritzing.org/">Fritzing</a> dan <a href="https://www.microsoft.com/en-us/microsoft-365/powerpoint">Microsoft Power Point</a>

## 🤝 Kontributor

Terima kasih kepada semua kontributor yang telah berkontribusi 🙏

<!-- <a href="https://github.com/uckypradestha/embeddedsystem/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=uckypradestha/embeddedsystem&max=1000" />
</a> -->

<h2></h2>

<a href="https://komputer.ft.unsoed.ac.id/">![Footer](https://github.com/user-attachments/assets/4db5037b-a9cc-44c6-a4cb-7618f3db244e)</a>

<p align="center">
  <br> <a href="https://twitter.com/uckypradestha" target="blank">
    <img src="https://img.shields.io/badge/-Twitter-%23042AFF?style=flat-square&logo=twitter&logoColor=%23042AFF&labelColor=%23ffffff00" height="35" hspace="15" />
  </a>
  <a href="https://linkedin.com/in/uckypradestha" target="blank">
    <img src="https://img.shields.io/badge/-LinkedIn-%23042AFF?style=flat-square&logo=linkedin&logoColor=%23042AFF&labelColor=%23ffffff00" height="35" hspace="15" />
  </a>
  <a href="https://instagram.com/pradestha" target="blank">
    <img src="https://img.shields.io/badge/-Instagram-%23042AFF?style=flat-square&logo=instagram&logoColor=%23042AFF&labelColor=%23ffffff00" height="35" hspace="15" />
  </a>
  <a href="https://www.youtube.com/c/uckypradestha" target="blank">
    <img src="https://img.shields.io/badge/-YouTube-%23042AFF?style=flat-square&logo=youtube&logoColor=%23042AFF&labelColor=%23ffffff00" height="35" hspace="15" />
  </a>

  <br> </p>
