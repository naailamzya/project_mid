# Sistem Manajemen Universitas

## Deskripsi
Sistem Manajemen Universitas adalah aplikasi berbasis console yang memungkinkan mahasiswa untuk login, melihat profil, mengisi dan melihat KRS. Aplikasi ini juga menyediakan fitur untuk dosen agar dapat mengelola dan memantau data mahasiswa serta mata kuliah yang diajarkan.

## Fitur Aplikasi
1. Login
    - Pengguna dapat login dengan memasukkan username, password, dan kode verifikasi.
    - Mahasiswa dan dosen memiliki akses yang berbeda tergantung perannya setelah login berhasil.

2. Kode Verifikasi
    - Setiap kali pengguna login, sistem akan menghasilkan kode verifikasi yang acak dan setiap pengguna akan mendapatkan kode yang berbeda.
2. Menu Dosen
   - Lihat KRS Mahasiswa: Dosen dapat melihat KRS yang diambil oleh mahasiswa yang terdaftar di mata kuliah yang diajarkan.
   - Cari Mahasiswa Berdasarkan NIM: Dosen dapat mencari mahasiswa berdasarkan NIM untuk melihat informasi mahasiswa lebih lanjut.
   - Lihat Maha Kuliah yang Diajarkan: Dosen dapat melihat daftar mata kuliah yang diajarkan kepada mahasiswa
3. Menu Mahasiswa
    - Lihat Profil: Mahasiswa dapat melihat informasi profil mereka seperti nama, NIM, dan program studi.
    - Lihat Daftar Mata Kuliah: Mahasiswa dapat melihat daftar mata kuliah yang tersedia di semester ini.
    - Tambah Mata Kuliah: Mahasiswa dapat mengisi KRS dengan memilih mata kuliah yang ingin diambil
    - Lihat KRS yang Diambil: Mahasiswa dapat melihat mata kuliah yang telah mereka ambil pada semester tersebut.
4. Logout 
## Struktur Class
- `Main`
- `User` (abstract class)
- `Mahasiswa` (extends User)
- `Dosen`
- `Role`
- `MataKuliah`
- `IManageKRS` (interface)
- `KRSManager` (implements IManageKRS)
- `LoginHelper`
- `UserManager`

## Cara Menjalankan
1. Clone Repository
    `https://github.com/nurulmarisa8/project_mid`
2. Compile semua file `.java`
3. Jalankan `Main.java`
4. Ikuti instruksi pada terminal

## Pengujian Aplikasi

Aplikasi **Sistem Manajemen Universitas** telah diuji untuk memastikan bahwa setiap fitur berfungsi dengan baik. Berikut adalah daftar pengujian yang telah dilakukan dan hasil yang diharapkan:

| **No** | **Deskripsi Pengujian**                                      | **Hasil yang Diharapkan**                                       | **Hasil**      |
|--------|---------------------------------------------------------------|---------------------------------------------------------------|----------------|
| 1      | Login dengan username atau password salah                    | Sistem menampilkan pesan kesalahan yang sesuai                 | Berhasil       |
| 2      | Login tanpa mengisi username atau password                   | Aplikasi menampilkan pesan kesalahan yang sesuai               | Berhasil       |
| 3      | Login dengan username dan password benar                     | Berpindah ke halaman verifikasi   | Berhasil       |
| 4      | Memasukkan kode verifikasi yang sudah kadaluwarsa |Sistem menampilkan pesan kesalahan yang sesuai| Berhasil   |
| 5      | Memasukkan kode verifikasi yang benar | Aplikasi berhasil masuk ke halaman utama sesuai dengan peran pengguna | Berhasil |
| 6      | Dosen Mengklik menu "Lihat KRS Mahasiswa" pada menu dosen       | Menampikan halaman untuk memasukkan NIM mahasiswa | Berhasil |
| 7      | Dosen salah memasukkan NIM mahasiswa          |Sistem menampilkan pesan kesalahan yang sesuai dan kembali ke menu dosen | Berhasil |
| 8      | Dosen memasukkan NIM mahasiswa dengan benar | Menampilkan KRS mahasiswa berisi mata kuliah yang terdaftar   | Berhasil       |
| 9      | Dosen mengklik menu "Cari Mahasiswa Berdasarkan NIM"  | Sistem berhasil mencari mahasiswa berdasarkan NIM yang dimasukkan    | Berhasil |
|10     | Dosen mengklik menu "Lihat Mata Kuliah yang diajarkan" | Siste menampilkan Daftar Mata Kuliah yang diajarkan oleh dosen | Berhasil   |
|11     | Mahasiswa mengklik menu "Lihat Profil" pada menu mahasiswa | Menampilkan Profil lengkap mahasiswa | Berhasil   |
|12     | Mahasiswa mengklik menu "Lihat Daftar Mata Kuliah" pada mahasiswa | Menampilkan daftar mata kuliah yang tersedia untuk diambil   | Berhasil |
| 13   | Mahasiswa mengklik menu "Isi KRS" pada menu mahasiswa   | Mahasiswa dapat memilih dan menambahkan mata kuliah ke dalam KRS   | Berhasil |
| 14     | Mahasiswa mengklik menu "Lihat KRS yang Diambil" pada menu mahasiswa   | Menampilkan daftar mata kuliah yang telah diambil mahasiswa | Berhasil   |
| 15     | Pengujian validasi data KRS (memilih mata kuliah yang tidak tersedia)   | Sistem menampilkan pesan kesalahan jika mata kuliah tidak valid     | Berhasil   |




## Pembagian Tugas
- Gyerend Nydle Linta Mangaluk: Class `User`
- Julio Rema Palotongan: Class `MataKuliah`
- Davidzen: Class `IManageKRS`
- Naa'ilah Mazaya: Class `Mahasiswa`
- Nurul Marisa Clara Waldi: Class `KRSManager`,`Main` dan dokumentasi
