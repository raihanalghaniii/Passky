<h1 align="center">
  <img src="https://passky.org/images/logo.png" alt="Logo" width="400" height="400">
</h1>

# Aplikasi Web "Passky"


## Sekilas Tentang

**Passky** adalah _password manager_ open-source yang sederhana, modern, ringan, dan aman. Aplikasi ini menggunakan arsitektur _zero trust_ dengan metode enkripsi canggih, seperti `XChaCha20` untuk mengamankan data sensitif dan `Argon2id` untuk hashing kata sandi master, yang dirancang untuk tahan terhadap serangan **brute-force.** Passky memungkinkan pengguna untuk menyimpan hingga 100 kata sandi secara gratis, dengan opsi upgrade ke paket premium untuk menyimpan jumlah kata sandi tak terbatas.

Passky juga mendukung berbagai platform, termasuk aplikasi web, ekstensi browser, aplikasi desktop, dan aplikasi Android, memberikan fleksibilitas dalam mengelola kata sandi di berbagai perangkat


## Instalasi

- Prasyarat, apa saja yang harus diinstal sebelumnya.
- Langkah instalasi dalam CLI.
- Ini masih kasarnya bentarrr gua masih nyoba nyoba

#### Kebutuhan Sistem:

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

7. Setelah semua konfigurasi selesai, jalankan Docker Compose untuk memulai server:
    
   ```bash
   $ sudo docker-compose up -d

8. 

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


## Pembahasan

- Pendapat anda tentang aplikasi web ini
    - kelebihan
    - kekurangan
- Bandingkan dengan aplikasi web lain yang sejenis


## Referensi

Cantumkan tiap sumber informasi yang anda pakai.
