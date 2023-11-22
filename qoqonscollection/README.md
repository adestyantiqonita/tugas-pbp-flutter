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

# TUGAS 8

- ## Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!
Navigator.push() menambahkan suatu route ke dalam stack route yang dikelola oleh Navigator yang berarti route sebelumnya tetap ada di stack route dan user bisa kembali ke route sebelumnya. Contoh navigasi dari halaman Home ke halaman Profile:
'''
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => Profile()),
);
'''
Navigator.pushReplacement() menghapus route yang sedang ditampilkan kepada pengguna dan menggantinya dengan suatu route yang mengakibatkan route sebelumnya dihapus dari stack route sehingga pengguna tidak dapat kembali ke route sebelumnya. Contoh navigasi dari halaman Profile ke halaman Home dan menggantikan Profile dengan Home
'''
Navigator.pushReplacement(
  context,
  MaterialPageRoute(builder: (context) => Home()),
);
'''

- ## Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!
Container : mengatur tata letak dan dekorasi dari widget yang ada di dalamnya, biasanya menetapkan margin, padding, warna latar belakang, dan batas-batas dari widget.
Row : menempatkan widget-widget secara horizontal (ditata dalam satu baris).
Column : menempatkan widget-widget secara vertikal (ditata dalam satu kolom).
ListView : menampilkan daftar item dalam bentuk vertikal atau horizontal.
Stack : menempatkan widget-widget secara tumpang tindih satu sama lain.

- ## Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!
TextFormField : mengambil input teks seperti nama item, deskripsi, dan harga sehingga dapat digunakan untuk memasukkan teks ke dalam bidang input,  kemudian dapat diambil value nya untuk diproses lebih lanjut.
ElevatedButton : menambahkan tombol "Simpan" di bagian bawah form sehingga ketika tombol ini ditekan, dapat mengaktifkan validasi form dan menampilkan dialog konfirmasi setelah berhasil menyimpan item.

- ## Bagaimana penerapan clean architecture pada aplikasi Flutter?
Pisahkan aplikasi menjadi beberapa lapisan. Kemudian domain (logika) nya juga dipisah, begitu pula dengan kode yang berhubungan dengan interface dan lapisan datanya. Dependency-nya pastikan disusun dari luar ke dalam. Terapkan prinsip-prinsip SOLID (Single Responsibility, Open-Closed, Liskov Substitution, Interface Segregation, dan Dependency Inversion). Pastikan setiap lapisan di-test. Gunakan dependency injection untuk mengelola ketergantungan antara komponen aplikasi.

- ## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)
Buat widget form dan isi dengan elemen name, amount, description dengan TextFormField dan definisikan validatornya. Salah satunya menggunakan int.tryParse() untuk memeriksa apakah input amount merupakan angka atau tidak. Kemudian menambahkan ElevatedButton yang berfungsi memvalidasi dan menampilkan dialog setelah tombol 'Save' ditekan. Memunculkan pop-up dengan showDialog pada onPressed Setelahnya buat drawer dengan Drawer. Tambahkan opsinya melalui ListTile dan tidak lupa di routing menggunakan Navigasi.

# TUGAS 9

- ## Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?
Bisa, sering dikenal dengan untyped atau pengambilan data tanpa tipe. Lebih baik menggunakan model sehingga lebih dapat memberikan ststruktur yang jelas dan membantu dalam menghindari kesalahan selama development.

- ## Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
CookieRequest dapat berfungsi untuk menangani proses pembuatan, penyimpanan, dan pengelolaan cookie (managemen cookie), menambahkan cookie ke setiap permintaan HTTP yang dibuat oleh aplikasi (pengiriman cookie dalam HTTP), dan menyimpan dan mengirim token otentikasi atau informasi otentikasi lainnya ke server setiap kali permintaan dilakukan.

instance CookieRequest dibagikan ke semua komponen dapat memastikan setiap aplikasi dapat mengakses informasi otentikasi yang dikelola oleh CookieRequest, menghindari duplikasi, memastikan konsistensi dalam penggunaan informasi otentikasi, mengurangi redundansi kode, meningkatkan efisiensi pengembangan, dan apabila ada pembaharuan maka semua komponen dapat ter-sinkronisasi dengan baik secara otomatis.

- ## Jelaskan mekanisme pengambilan data dari JSON hingga dapat ditampilkan pada Flutter.

membuat model Dart yang mencerminkan struktur data JSON, kemudian menggunakan package seperti http untuk mengambil data dari API, kemudian data diterima dalam format JSON, kemudian menggunakan package seperti dart:convert untuk mengonversinya ke dalam objek Dart (model) atau memproses JSON secara langsung dalam Flutter.

- ## Jelaskan mekanisme autentikasi dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
Buat widget Form untuk memasukkan informasi akun pada Flutter, pakai package 'http' untuk mengirim data akun ke endpoint autentikasi Django, kasih response sehingga bisa tau udah terautentifikasi atau belum, tampilin bisa pake navigator, gunakan token kalo mau lebih aman.  

- ## Sebutkan seluruh widget yang kamu pakai pada tugas ini dan jelaskan fungsinya masing-masing.
MaterialApp: Digunakan sebagai root widget untuk mendefinisikan aspek-aspek dasar dari aplikasi seperti judul, tema, dan halaman utama.

Provider: Digunakan untuk menyediakan instance CookieRequest ke seluruh komponen di aplikasi menggunakan Provider.

MyApp (StatelessWidget): Menyediakan MaterialApp dan instance CookieRequest kepada seluruh aplikasi.

LoginPage (StatefulWidget): Menerima input, berkomunikasi dengan Django untuk proses autentikasi, dan menangani 
respons.

LeftDrawer: Membuat drawer (panel samping) dengan daftar menu.

ProductPage (StatefulWidget): Menampilkan daftar produk dari Django.

ElevatedButton, TextField, CircularProgressIndicator, SnackBar, AlertDialog: Masing-masing digunakan untuk membuat tombol login, input teks, indikator loading, pesan notifikasi, dan dialog peringatan.

ListView, Column, Container: Membuat tata letak yang sesuai untuk menampilkan daftar produk.

FutureBuilder: Mengelola state dan membangun widget berdasarkan hasil dari Future.

AppBar, Scaffold: Membuat tata letak, AppBar dan navigasi halaman.

Navigator, MaterialPageRoute: Berpindah antar halaman saat login atau menekan tombol navigasi.

SnackBar: Menampilkan pesan singkat pada bagian bawah layar.

Drawer, ListTile: Membuat drawer dan item menu.

QuickType: Menghasilkan model Dart dari data JSON untuk integrasi dengan aplikasi Flutter.

http package: Digunakan untuk berkomunikasi dengan backend Django, misalnya untuk mengambil data atau mengirim data.

InkWell: Membuat area yang dapat diklik dengan efek animasi.

- ## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).
Membuat Django App dengan nama 'authentication' dan tak lupa tambahkan di settings.py variabel yang diperlukan dan appnya serta pip install django-cors-headers. Membuat view untuk login serta implementasinya dalam 'authentication'. Instal package yang disediakan dosen dan provider. Buat file baru pada folder screens dengan nama login dengan menggunakan widget TextField dan ElevatedButton. Buat endpoint dan view di Django kemudian gunakan Quicktype agar lebih cepat meng-generate kodenya untuk membuat Model dart. Buat endpoint baru di Django untuk mendapatkan daftar produk. Implementasikan halaman (ProductPage) di Flutter untuk menampilkan daftar produk.
Tambahkan menu navigasi ke halaman produk di left_drawer.dart. Tambahkan endpoint dan view untuk logout di Django.
Implementasikan fungsi logout di Flutter dan tambahkan ke menu navigasi. Makin hari makin bingung ini pertanyaan terakhir harus jelasinnya gimana :"