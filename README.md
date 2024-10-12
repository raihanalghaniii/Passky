<h1 align="center">
  <img src="https://passky.org/images/logo.png" alt="Logo" width="400" height="400">
</h1>

# Aplikasi Web "Passky"


## Sekilas Tentang

**Passky** adalah _password manager_ open-source yang sederhana, modern, ringan, dan aman. Aplikasi ini menggunakan arsitektur _zero trust_ dengan metode enkripsi canggih, seperti `XChaCha20` untuk mengamankan data sensitif dan `Argon2id` untuk hashing kata sandi master, yang dirancang untuk tahan terhadap serangan **brute-force.** Passky memungkinkan pengguna untuk menyimpan hingga 100 kata sandi secara gratis, dengan opsi upgrade ke paket premium untuk menyimpan jumlah kata sandi tak terbatas.

Passky juga mendukung berbagai platform, termasuk aplikasi web, ekstensi browser, aplikasi desktop, dan aplikasi Android, memberikan fleksibilitas dalam mengelola kata sandi di berbagai perangkat


## Instalasi

Passky Server dapat dengan mudah diinstal dengan berbagai cara.
- Docker (Recommended)
- Linode (One-click Install)
- Umbrel (One-click Install)
- Shared Hosting

#### Kebutuhan Sistem:
- OS: Linux (Ubuntu 20.04 atau lebih baru)
- RAM: Minimal 1 GB
- Storage: Minimal 10 GB ruang kosong
- Dependencies: Docker, Docker Compose, Git

#### Proses Instalasi:
1. Langkah pertama, jalankan perintah berikut untuk menginstal Docker dan Docker Compose di VPS :
   
     ```bash
     # Install docker
     $ curl -sSL https://get.docker.com/ | CHANNEL=stable bash
     # Start dan aktifkan Docker agar berjalan otomatis saat boot
     $ sudo systemctl enable --now docker
     # Install docker compose
     $ sudo apt install docker-compose -y

2. Login ke VPS menggunakan SSH dengan perintah berikut:
   
   ```bash
   $ ssh root@160.19.166.139

3. Setelah berhasil login ke server, clone repository Passky Server:
   
   ```bash
   $ git clone https://github.com/Rabbit-Company/Passky-Server.git 

4. Masuk ke direktori tempat repository Passky Server di-clone:
   
   ```bash
   $ cd Passky-Server

5. Jika file environment belum tersedia, jalankan installerGUI.sh untuk membuat file environment:
   
   ```bash
   $ ./installerGUI.sh

6. Ikuti petunjuk instalasi:
   - Pilih Yes untuk melanjutkan proses pembuatan file .env baru. File .env sebelumnya akan dihapus dan yang baru akan dibuat berdasarkan jawaban yang Anda berikan selama instalasi.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky1.png?raw=true)
   - Masukkan username yang akan Anda gunakan untuk mengelola Passky Admin Panel.yang Anda berikan selama instalasi. Misalnya: admin128.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky2.png?raw=true)
   - Masukkan password untuk akun admin yang Anda buat pada langkah sebelumnya.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky3.png?raw=true)
   - Pilih lokasi server yang sesuai dengan tempat Anda ingin menempatkan server Passky.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky5.png?raw=true)
   - Masukkan jumlah maksimal akun yang dapat dibuat di server Passky ini. Jika Anda menginginkan jumlah akun tanpa batas, masukkan -1.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky6.png?raw=true)
   - Masukkan jumlah maksimal password yang bisa disimpan oleh akun premium. Jika Anda ingin membebaskan jumlah password untuk akun premium, gunakan -1.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky7.png?raw=true)
   - Masukkan tipe database yang ingin digunakan. Jika memilih SQLite, Passky akan menggunakan database berbasis file yang lebih sederhana.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky8.png?raw=true)
   - Masukkan nama file untuk database jika Anda memilih SQLite sebagai database engine. Jika Anda memilih MySQL, Anda mungkin perlu memberikan nama database MySQL.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky9.png?raw=true)
   - Pilih apakah Anda ingin mengaktifkan SMTP Email untuk mengirimkan email dari server. Jika Anda tidak membutuhkan fitur ini, pilih No.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky10.png?raw=true)
   - Pilih apakah Anda ingin mengaktifkan API Call Limiter untuk membatasi jumlah panggilan API per perangkat. Jika server ini akan diakses melalui internet, lebih baik mengaktifkan fitur ini untuk keamanan. Pilih Yes jika ingin mengaktifkannya.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky11.png?raw=true)
   - Setelah konfigurasi selesai, Passky Installer akan menampilkan pesan bahwa file .env telah berhasil dibuat.
     
     ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky12.png?raw=true)
     
7. Setelah konfigurasi selesai, jalankan server dengan Docker
   ```bash
   $ sudo docker-compose up -d
   
8. Kunjungi alamat IP server pada browser untuk mengakses Passky Admin Panel:
   
   ![alt text](https://github.com/raihanalghaniii/Passky/blob/main/Screenshots/passky13.png?raw=true) 
   
## Konfigurasi (opsional)

Setting server tambahan yang diperlukan untuk meningkatkan fungsi dan kinerja aplikasi, misalnya:
- batas upload file
- batas memori
- dll

Plugin untuk fungsi tambahan
- login dengan Google/Facebook
- editor Markdown
- dll


##  Maintenance (opsional)

Setting tambahan untuk maintenance secara periodik, misalnya:
- buat backup database tiap pekan
- hapus direktori sampah tiap hari
- dll


## Otomatisasi (opsional)

Skrip shell untuk otomatisasi instalasi, konfigurasi, dan maintenance.


## Cara Pemakaian

- Tampilan aplikasi web
- Fungsi-fungsi utama
- Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot
- WEIT MO AI DULS


## Pembahasan

**Passky** adalah aplikasi _password manager_ open-source yang berfokus pada **keamanan dan kesederhanaan**. Sebagai salah satu aplikasi _password manager_ yang ada, aplikasi ini menawarkan beberapa kelebihan di antaranya:
- _Open-source,_ sehingga pengguna memiliki kontrol penuh atas kode sumber dan dapat memodifikasinya sesuai kebutuhan.
- Menggunakan arsitektur _zero trust_ yang memastikan data pengguna terenkripsi sepenuhnya dan tidak dapat diakses tanpa izin.
- Mengimplementasikan enkripsi `XChaCha20` dan _hashing_ `Argon2id`, yang menawarkan perlindungan tinggi terhadap serangan seperti **brute-force.**
- Mendukung berbagai platform, seperti web, desktop, aplikasi Android, dan ekstensi browser, yang memudahkan akses di berbagai perangkat.
- Menawarkan paket gratis yang memungkinkan pengguna menyimpan hingga 100 kata sandi, dengan opsi upgrade ke premium untuk fitur yang lebih banyak.

Namun, aplikasi ini tetap memiliki beberapa kekurangan seperti:
- Fitur premium tidak sebanyak aplikasi lain seperti _Dashlane_ atau _LastPass_, yang memiliki fitur tambahan seperti pelacakan _dark web_ atau VPN.
- Proses instalasi di server atau Docker bisa cukup kompleks bagi pengguna awam, terutama bagi mereka yang belum terbiasa dengan pengelolaan _hosting._
- Penggunaan Redis dan pengaturan cron mungkin memerlukan pemahaman teknis yang lebih mendalam.

Jika dibandingkan dengan aplikasi sejenis seperti **dashlane,** terdapat beberapa kelebihan maupun kekurangan yang dapat kita bandingkan, di antaranya:
- Dashlane memiliki antarmuka modern dan intuitif yang mendukung pelengkapan otomatis untuk kata sandi dan form, sedangkan Passky memiliki desain yang lebih sederhana dan berfokus pada fungsi dasar tanpa fitur visual canggih atau pelengkapan otomatis.
- Dashlane menawarkan berbagai fitur tambahan seperti VPN bawaan, pelacakan dark web, dan laporan kesehatan kata sandi, sedangkan Passky lebih minimalis dan hanya menawarkan fitur manajemen kata sandi dengan keamanan tinggi.
- Dashlane memiliki dukungan pelanggan yang kuat, termasuk layanan premium untuk pengguna berbayar, sedangkan Passky, karena berbasis open-source, memiliki komunitas lebih kecil dan tidak menyediakan dukungan pelanggan premium, meskipun pengguna bisa memodifikasi kode sumbernya sendiri.
- Dashlane mudah diakses melalui web dan aplikasi tanpa instalasi rumit, sedangkan Passky memerlukan instalasi teknis yang lebih kompleks jika di-hosting sendiri, termasuk pengaturan server dan cron jobs, yang bisa menjadi tantangan bagi pengguna awam.

## Referensi

1. [About Passky](https://github.com/Rabbit-Company/Passky-Server) - Passky
2. 
