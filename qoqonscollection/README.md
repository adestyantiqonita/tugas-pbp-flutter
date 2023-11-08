# Qonita Adestyanti
# 2106750925
# qoqonscollection

# TUGAS 7

- ## Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?
Stateful Widget dapat mempertahankan keadaan internal dan dapat merender ulang tampilan berdasarkan perubahan keadaan sedangkan Stateless Widget tidak dapat mempertahankan keadaan internal dan tidak perlu merender ulang jika tidak ada perubahan yang mempengaruhi widget. Singkat kata, Stateful Widget bersifat mutable sedangkan Stateless Widget bersifat immutable. 

- ## Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.
MaterialApp : mengkonfigurasi aplikasi sepertu judul, tema dan tampilan awal
Scaffold : penyedia struktur daasar untuk mengimplementasikan Material Design, dengan menyediakan komponen seperti AppBar, Body, dan lainnya
AppBar : menampilkan bilah aplikasi di bagian atas layar
SingleChildScrollView : membuat di dalamnya dapat di-scroll jika melebihi ukuran layar
Padding : memberikan jarak di sekitar widget
Column : menampilkan widget anaknya dalam ukuran vertikal
Text : menampilkan teks di layar
GridView.count : mengatur item dalam tata letak grid berdasarkan jumlah lintasan lintas yang diatur
ShopCard : menampilkan item dari daftar belanja. Ini memiliki ikon, teks, dan merespons sentuhan pengguna
Material : mengimplementasikan komponen Material Design
InkWell : memberikan respons terhadap sentuhan pengguna
Container : menyusun widget lain, memberikan padding, warna, dan lainnya
Icon : menampilkan ikon berdasarkan IconData yang diberikan
SnackBar : menampilkan pesan singkat di bagian bawah layar

- ## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
Buat proyek Flutter baru menggunakan perintah flutter create qoqonscollection di terminal.
Buka file lib/main.dart dan tambahkan import package serta buat menu.dart dalam file lib.
Buat kelas MyApp sebagat root dari aplikasi dan konfigurasi widget menggunakan MaterialApp
Isi menu.dart dengan kelas MyHomePage yang merupakan halaman utama aplikasi serrta tampilkan tata letak dasar aplikasi menggunakan Scaffold.
Dicoba, flutter run kemudian push ke repositori github.