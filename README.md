# Sistem Manajemen Universitas

## Deskripsi
Sistem Manajemen Universitas adalah aplikasi berbasis console yang memungkinkan mahasiswa untuk login, melihat profil, mengisi dan melihat KRS. Aplikasi ini juga menyediakan fitur untuk dosen agar dapat mengelola dan memantau data mahasiswa serta mata kuliah yang diajarkan.

## Fitur Aplikasi
1. Login
    - Pengguna dapat login dengan memasukkan username dan password
    - Mahasiswa dan dosen memiliki akses yang berbeda tergantung perannya setelah login berhasil.
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
    - Pengguna dapat logout setelah selesai.

## Struktur Class
- `Main`
- `AppMenu` (polymorphism)
- `DataLoader` (encapsulation)
- `User` (abstract class)
- `Mahasiswa` (extends `User`)
- `Dosen` (extends `User`)
- `MataKuliah`
- `IManageKRS` (interface)
- `KRSManager` (implements `IManageKRS`)
- `UserManager`
- `ViewKRSService` (encapsulation)

## Cara Menjalankan
1. Clone Repository
    `https://github.com/nurulmarisa8/project_mid`
2. Compile semua file `.java`
3. Jalankan `Main.java`
4. Ikuti instruksi pada terminal

## Pengujian Aplikasi

Aplikasi **Sistem Manajemen Universitas** telah diuji untuk memastikan bahwa setiap fitur berfungsi dengan baik. Berikut adalah daftar pengujian yang telah dilakukan dan hasil yang diharapkan:

| **No** | **Deskripsi Pengujian**                                                | **Hasil yang Diharapkan**                                                   | **Hasil**      |
|--------|-----------------------------------------------------------------------|----------------------------------------------------------------------------|----------------|
| 1      | Login dengan username atau password salah                              | Sistem menampilkan pesan kesalahan yang sesuai                             | Berhasil       |
| 2      | Login tanpa mengisi username atau password                             | Aplikasi menampilkan pesan kesalahan yang sesuai                           | Berhasil       |
| 3      | Login dengan username dan password benar                               | Berpindah ke menu utama                                                    | Berhasil       |
| 4      | Dosen mengklik menu "Lihat KRS Mahasiswa" pada menu dosen              | Menampilkan halaman untuk memasukkan NIM mahasiswa                         | Berhasil       |
| 5      | Dosen salah memasukkan NIM mahasiswa                                   | Sistem menampilkan pesan kesalahan yang sesuai dan kembali ke menu dosen    | Berhasil       |
| 6      | Dosen memasukkan NIM mahasiswa dengan benar                            | Menampilkan KRS mahasiswa berisi mata kuliah yang terdaftar                | Berhasil       |
| 7      | Dosen mengklik menu "Cari Mahasiswa Berdasarkan NIM"                  | Sistem berhasil mencari mahasiswa berdasarkan NIM yang dimasukkan           | Berhasil       |
| 8      | Dosen mengklik menu "Lihat Mata Kuliah yang diajarkan"                | Sistem menampilkan daftar mata kuliah yang diajarkan oleh dosen             | Berhasil       |
| 9      | Mahasiswa mengklik menu "Lihat Profil" pada menu mahasiswa             | Menampilkan profil lengkap mahasiswa                                       | Berhasil       |
| 10     | Mahasiswa mengklik menu "Lihat Daftar Mata Kuliah" pada menu mahasiswa | Menampilkan daftar mata kuliah yang tersedia untuk diambil                 | Berhasil       |
| 11     | Mahasiswa mengklik menu "Isi KRS" pada menu mahasiswa                  | Mahasiswa dapat memilih dan menambahkan mata kuliah ke dalam KRS            | Berhasil       |
| 12     | Mahasiswa mengklik menu "Lihat KRS yang Diambil" pada menu mahasiswa   | Menampilkan daftar mata kuliah yang telah diambil mahasiswa                | Berhasil       |
| 13     | Pengujian validasi data KRS                                            | Sistem menampilkan pesan kesalahan jika mata kuliah tidak valid             | Berhasil       |

## Pembagian Tugas
- Gyerend Nydle Linta Mangaluk: Class `User` dan `DataLoader` 
- Julio Rema Palotongan: Class `Mahasiswa` dan `UserManager`
- Davidzen: Class `IManageKRS` dan `AppMenu`
- Naa'ilah Mazaya: Class `MataKuliah` dan `Dosen`
- Nurul Marisa Clara Waldi: Class `KRSManager`,`Main` dan dokumentasi
