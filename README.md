# Nama         :Elisabeth Banjarnahor  
# Nim          :312410525
# Kls          :Ti.24.A5


# Penjelasan Project

![Foto](https://github.com/Elisabethbanjarnahor/PEM-WEB-UAS/blob/e25ae15364aeded1f7374c704aede179b3500451/img/Screenshot%202026-01-07%20113025.png)
Halaman Login (Autentikasi Pengguna)

Ini adalah halaman pertama yang muncul saat aplikasi diakses. Halaman ini berfungsi sebagai gerbang keamanan (security gate) untuk membatasi akses ke sistem inventaris.
* Fitur: Validasi username dan password.
* Keamanan: Menggunakan PHP Session untuk memastikan hanya user terdaftar yang bisa masuk ke Dashboard. Jika username/password salah, sistem akan menolak akses.
* Desain: Menggunakan komponen Card Bootstrap 5 yang responsif dan ditempatkan presisi di tengah layar (Center Alignment).

![foto](https://github.com/Elisabethbanjarnahor/PEM-WEB-UAS/blob/ba03a1a1bde3210b0d9dd00e9a2a8494f4865910/img/Screenshot%202026-01-07%20113101.png)
Implementasi Halaman Dashboard (Beranda)

Setelah berhasil login, pengguna akan diarahkan ke Dashboard ini sebagai pusat navigasi sistem. Halaman ini dirancang untuk memberikan ringkasan status dan akses cepat ke fitur utama.

* Sapaan Dinamis: Sistem secara otomatis mendeteksi waktu saat ini (Pagi/Siang/Sore/Malam) dan menyapa pengguna berdasarkan nama akun yang sedang login.
* Navigasi Cepat: Terdapat 3 kartu menu utama (Data Barang, Profil Pengguna, dan Info Sistem) untuk memudahkan akses ke modul-modul aplikasi.
* Status Login: Memberikan indikasi visual bahwa sesi login pengguna sedang aktif dan aman.

![foto](https://github.com/Elisabethbanjarnahor/PEM-WEB-UAS/blob/ba03a1a1bde3210b0d9dd00e9a2a8494f4865910/img/Screenshot%202026-01-07%20113202.png)
Halaman Kelola Inventaris (CRUD Barang)

Ini adalah modul utama aplikasi di mana administrator dapat mengelola seluruh data stok barang. Halaman ini dibagi menjadi dua bagian utama untuk efisiensi penggunaan:Ini adalah modul utama aplikasi di mana administrator dapat mengelola seluruh data stok barang. Halaman ini dibagi menjadi dua bagian utama untuk efisiensi penggunaan:

* Form Tambah Barang (Kiri): Memungkinkan admin memasukkan data barang baru meliputi Kode, Nama, Kategori, dan Jumlah Stok awal.
* Tabel Daftar Barang (Kanan): Menampilkan seluruh data yang tersimpan di database.
* Fitur keunggulan
  * Search (Pencarian): Memudahkan pencarian barang spesifik berdasarkan nama atau kode.
  * Pagination: Membagi tampilan data menjadi 5 baris per halaman agar tabel tetap rapi meskipun data mencapai ratusan.
  * Action Buttons: Akses cepat untuk Mengedit atau Menghapus barang.

![foto](https://github.com/Elisabethbanjarnahor/PEM-WEB-UAS/blob/ba03a1a1bde3210b0d9dd00e9a2a8494f4865910/img/Screenshot%202026-01-07%20113234.png)
Halaman Edit & Restock Barang

Fitur ini digunakan untuk memperbarui informasi barang yang sudah tersimpan. Saat admin memilih tombol "Edit" pada tabel, sistem akan mengarahkan ke halaman ini dengan formulir yang sudah terisi otomatis oleh data barang tersebut.

* Fungsi Utama: Memperbaiki kesalahan penulisan nama/kategori dan melakukan Restock (menambah jumlah stok barang).
* Kemudahan Akses: Admin tidak perlu mengetik ulang seluruh data, cukup mengubah kolom yang diperlukan saja (misalnya hanya mengubah angka stok) lalu menyimpan perubahan.



![foto](https://github.com/Elisabethbanjarnahor/PEM-WEB-UAS/blob/ba03a1a1bde3210b0d9dd00e9a2a8494f4865910/img/Screenshot%202026-01-07%20113334.png)
Hapus Barang (Delete Action)

Fitur ini memungkinkan admin menghapus data barang yang sudah tidak diperlukan dari database.

* Keamanan: Sistem menggunakan Dialog Konfirmasi Bawaan Browser (Browser Native Alert) sebelum menghapus data.
* Cara Kerja: Saat tombol hapus diklik, browser otomatis memunculkan peringatan (Pop-up) untuk meminta persetujuan admin. Jika admin menekan "Cancel", proses penghapusan dibatalkan otomatis oleh browser tanpa perlu memuat ulang halaman.



![foto](https://github.com/Elisabethbanjarnahor/PEM-WEB-UAS/blob/ba03a1a1bde3210b0d9dd00e9a2a8494f4865910/img/Screenshot%202026-01-07%20113631.png)
Halaman Profil Pengguna (User Profile)

Halaman ini menampilkan detail informasi akun administrator yang sedang login.
* Informasi Akun: Menampilkan Nama Lengkap, Username, Role, dan Tanggal Bergabung secara dinamis dari database.
* Avatar Dinamis: Jika pengguna belum mengunggah foto profil, sistem secara otomatis men-generate avatar berbasis inisial nama (contoh: "FH" untuk Fajar Habibillah) menggunakan API UI Avatars, sehingga tampilan antarmuka tetap estetis dan personal.


![foto](https://github.com/Elisabethbanjarnahor/PEM-WEB-UAS/blob/ba03a1a1bde3210b0d9dd00e9a2a8494f4865910/img/Screenshot%202026-01-07%20113914.png)
Peringatan Stok Menipis (Low Stock Alert)

Fitur notifikasi cerdas yang muncul otomatis di Halaman Utama (Dashboard) ketika sistem mendeteksi ada barang dengan stok kritis (di bawah 5 unit).

* Tujuan: Membantu admin segera melakukan Restock (isi ulang) agar stok tidak sampai kosong.
* Tampilan: Menggunakan panel berwarna merah (Danger Alert) yang mencolok agar admin langsung sadar.


![foto](https://github.com/Elisabethbanjarnahor/PEM-WEB-UAS/blob/ba03a1a1bde3210b0d9dd00e9a2a8494f4865910/img/Screenshot%202026-01-07%20114008.png)
Halaman Profile Developer (About Creator)

Halaman khusus yang memuat informasi identitas pengembang aplikasi.

* Identitas Lengkap: Menampilkan Nama, NIM, Kelas, dan Mata Kuliah secara terstruktur.
* Fitur Upload Foto: Mendemonstrasikan kemampuan aplikasi dalam menangani File Handling (Upload Image). Foto profil pengembang dapat diubah sewaktu-waktu dan tersimpan otomatis di server.
* Integrasi Sosial Media: Tombol akses langsung (Direct Link) menuju akun Instagram pengembang.




