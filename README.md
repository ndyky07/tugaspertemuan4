Nama: Indi Warda Ramadhani
<br>NIM: 2341760026
<br>Kelas: SIB 3D
<br>Mata Kuliah: Pemrograman Mobile

Tugas 3 : Create Project

1. Ketik "flutter new". Pilih perintah Flutter: New Project. 

![Screenshot tugaspertemuan4](images/01.png)

2. Berikutnya, pilih Application lalu folder tempat proyek akan dibuat. Folder ini dapat 
berupa direktori utama Anda, atau direktori seperti C:\src\. 

![Screenshot tugaspertemuan4](images/02.png)

3. Pada panel sebelah kiri VS Code, pastikan bahwa Penjelajah dipilih lalu buka file 
pubspec.yaml.

![Screenshot tugaspertemuan4](images/03.png)

Ganti konten file ini dengan kode berikut: 

![Screenshot tugaspertemuan4](images/04.png)

4. Berikutnya, buka file konfigurasi lainnya dalam proyek tersebut, analysis_options.yaml. 

![Screenshot tugaspertemuan4](images/05.png)

Ganti konten file tersebut dengan kode berikut: 

![Screenshot tugaspertemuan4](images/06.png)

5. Terakhir, buka file main.dart pada direktori lib/. 

![Screenshot tugaspertemuan4](images/07.png)

Ganti konten file ini dengan kode berikut: 

![Screenshot tugaspertemuan4](images/08.png)

Selagi lib/main.dart terbuka, temukan tombol "play" di pojok kanan atas jendela VS Code lalu klik tombol tersebut.

![Screenshot tugaspertemuan4](images/09.png)

6. Di bagian bawah lib/main.dart, tambahkan teks pada objek Text pertama lalu simpan (Ctrl+S/Cmd+S). Aplikasi akan langsung berubah tetapi kata acak tetap sama—ini menunjukkan fitur stateful Hot Reload Flutter yang bekerja setiap kali file disimpan.

![Screenshot tugaspertemuan4](images/10.png)

7. Tambahkan tombol di bawah Text kedua pada `Column`. Simpan file, aplikasi akan ter-update: tombol muncul, dan saat diklik konsol VS Code menampilkan pesan button pressed!."

![Screenshot tugaspertemuan4](images/11.png)

8. Di MyAppState, tambahkan metode `getNext()` untuk mengisi ulang `current` dengan `WordPair.random()` lalu panggil `notifyListeners()` agar widget yang menggunakan state ikut diperbarui.

![Screenshot tugaspertemuan4](images/12.png)

9. Terakhir, panggil `getNext()` di callback tombol. Kini setiap menekan Next, aplikasi menampilkan pasangan kata acak baru.

![Screenshot tugaspertemuan4](images/13.png)

![Screenshot tugaspertemuan4](images/14.png)

![Screenshot tugaspertemuan4](images/15.png)

Baris `Text(appState.current.asLowerCase)` sebaiknya diekstrak menjadi widget terpisah agar lebih mudah dikelola. Baris ini tidak perlu akses penuh ke `appState`, cukup menerima pasangan kata saat ini.

10. Tulis ulang `MyHomePage` dengan Extract Widget (Refactor → Extract Widget), beri nama misalnya BigCard, lalu klik Enter.

![Screenshot tugaspertemuan4](images/16.png)

11. Tindakan ini secara otomatis membuat class baru, BigCard, di akhir file saat ini. Class tersebut akan terlihat seperti berikut: 

![Screenshot tugaspertemuan4](images/17.png)

Edit class BigCard di metode `build()`. Pada widget `Text`, lakukan Refactor → Wrap with Padding. Setelah disimpan, teks akan dibungkus `Padding` sehingga tampil dengan ruang lebih luas."

![Screenshot tugaspertemuan4](images/18.png)

12. Ubah padding menjadi 20 untuk ruang lebih luas. Lalu pilih Refactor → Wrap with widget..., ketik Card, tekan Enter. Kini teks berada dalam `Card` dengan padding lebih besar.

![Screenshot tugaspertemuan4](images/19.png)

Gabungkan `Padding` + `Text` dalam `Card`, lalu beri warna dari Theme agar kartu lebih menarik dan konsisten dengan skema aplikasi.

![Screenshot tugaspertemuan4](images/20.png)

13. Buat perubahan berikut untuk metode build() BigCard.

![Screenshot tugaspertemuan4](images/21.png)

Kartu kini berwarna sesuai warna primer aplikasi. Untuk mengubahnya, ubah seedColor pada `ColorScheme` di class MyApp.

![Screenshot tugaspertemuan4](images/22.png)

14. Perbesar ukuran teks dan ubah warna teks agar lebih kontras dalam metode `build()` `BigCard`.

![Screenshot tugaspertemuan4](images/23.png)

Posisikan UI di tengah layar aplikasi setelah menampilkan pasangan kata acak dengan gaya visual

![Screenshot tugaspertemuan4](images/24.png)

15. Ubah alignment Column di build() MyHomePage agar BigCard tidak menempel di atas, misalnya dengan mengatur mainAxisAlignment

![Screenshot tugaspertemuan4](images/25.png)

Atur mainAxisAlignment Column ke MainAxisAlignment.center agar anak-anaknya berada di tengah vertikal

![Screenshot tugaspertemuan4](images/26.png)

UI sudah berada di tengah horizontal di dalam Column, tapi Column belum berada di tengah Scaffold; gunakan Widget Inspector untuk memverifikasi.

![Screenshot tugaspertemuan4](images/27.png)

Kini, aplikasi akan terlihat seperti berikut: 

![Screenshot tugaspertemuan4](images/28.png)

Hapus teks di atas BigCard untuk tampilan lebih bersih dan tambahkan SizedBox(height: 10) antara BigCard dan ElevatedButton untuk memberi jarak visual.

16. Dengan perubahan opsional, MyHomePage kini memiliki kode yang membuat tampilan aplikasi seperti di bawah ini.

![Screenshot tugaspertemuan4](images/29.png)

17. Untuk menambahkan logika bisnis, buka `MyAppState` dan tambahkan kode berikut.

![Screenshot tugaspertemuan4](images/30.png)

Untuk menambahkan tombol, letakkan tombol ‘Like’ di kiri tombol ‘Next’ dengan membungkus keduanya dalam `Row` menggunakan opsi Wrap with Row di `build()` MyHomePage.

![Screenshot tugaspertemuan4](images/31.png)

UI kembali ke tempat sebelumnya. 

![Screenshot tugaspertemuan4](images/32.png)

18. Tambahkan tombol kedua di MyHomePage menggunakan `ElevatedButton.icon()` dengan ikon yang disesuaikan berdasarkan status favorit, dan gunakan `SizedBox` untuk memberi jarak antar tombol.

![Screenshot tugaspertemuan4](images/33.png)

19. Pisahkan MyHomePage menjadi dua widget terpisah dengan mengganti seluruh kode MyHomePage dengan kode baru berikut.

![Screenshot tugaspertemuan4](images/34.png)

![Screenshot tugaspertemuan4](images/35.png)

![Screenshot tugaspertemuan4](images/36.png)

![Screenshot tugaspertemuan4](images/37.png)

Saat disimpan, Anda akan melihat sisi visual UI telah siap—tetapi tidak bekerja. Mengklik ♥︎ (hati) pada kolom samping navigasi tidak melakukan apa pun.

![Screenshot tugaspertemuan4](images/38.png)

20. Widget stateful baru hanya perlu melacak satu variabel: selectedIndex. Buat 3 perubahan berikut untuk _MyHomePageState:

![Screenshot tugaspertemuan4](images/39.png)

21.  Tempatkan kode berikut di bagian atas metode build _MyHomePageState, tepat sebelum return Scaffold:

![Screenshot tugaspertemuan4](images/40.png)

![Screenshot tugaspertemuan4](images/41.png)

22.  Sekarang kode Anda dapat memutuskan untuk menampilkan label dengan membuat kueri constraints saat ini atau tidak. Buat perubahan baris tunggal berikut untuk metode build _MyHomePageState: 

![Screenshot tugaspertemuan4](images/42.png)

![Screenshot tugaspertemuan4](images/43.png)

![Screenshot tugaspertemuan4](images/44.png)

23. Berikut salah satu cara membuat halaman favorit yang bisa Anda kembangkan dan ubah sesuai keinginan. Berikut class `FavoritesPage`:

![Screenshot tugaspertemuan4](images/45.png)

![Screenshot tugaspertemuan4](images/46.png)

24. Bereksperimenlah lebih lanjut dengan aplikasi yang Anda buat selama menjalani lab ini. 

![Screenshot tugaspertemuan4](images/47.png)

![Screenshot tugaspertemuan4](images/48.png)

Jika dihapus 

![Screenshot tugaspertemuan4](images/49.png)












