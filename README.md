# 🎮 GAMEZONE - Aplikasi Web Booking Rental PlayStation

**Proyek UAS:** Aplikasi Web Booking Rental PlayStation (GAMEZONE) berbasis _website_ responsif dengan fitur autentikasi, manajemen inventaris, dan sistem penyewaan (booking) jadwal.

---

## 👥 Tim Pengembang (Kelompok)

| Nama Anggota         | Peran / Fokus Pekerjaan                     |
| :------------------- | :------------------------------------------ |
| **Ruli**             | Project Manager & System Analyst            |
| **Hafidhin Adinata** | UI/UX Designer & Frontend Developer         |
| **M. Risal**         | Database Administrator (DBA) & ERD Designer |
| **Geraldhino**       | Backend Developer & API Integrator          |

---

### 📸 Cuplikan Tampilan Aplikasi

<div align="center">
  <img src="docs/home.jpeg" width="800" alt="Halaman Utama GameZone">
  <br><br>
  <img src="docs/admin.jpeg" width="800" alt="Dashboard Admin GameZone">
  <br><br>
  <img src="docs/lokasi.jpeg" width="800" alt="Peta Lokasi Rental">
</div>

---

## 🚀 Fitur Utama

- 🔐 **Sistem Autentikasi & Multi-role:** Pemisahan hak akses antara Admin dan Pelanggan.
- 📊 **Dashboard Admin:** Pengelolaan data pelanggan dan manajemen inventaris mesin PS (PS5, PS4, PS3).
- 📅 **Sistem Booking:** Pemesanan jadwal sewa PlayStation secara _real-time_.
- 💰 **Riwayat Transaksi:** Pencatatan histori penyewaan beserta kalkulasi harga otomatis.
- 💬 **WhatsApp Integration:** Tombol _chat_ langsung untuk menghubungi admin.

---

## 💻 Teknologi yang Digunakan

- **Backend:** Laravel Framework (PHP)
- **Frontend:** Tailwind CSS / Bootstrap (Blade Templating)
- **Database:** MySQL
- **Tools:** Git, GitHub, VSCode

---

## 🛠️ Cara Instalasi (Lokal)

Ikuti langkah-langkah berikut untuk menjalankan proyek ini di komputer Anda:

1. **Clone Repositori:**

    ```bash
    git clone https://github.com/ruli162/gamezone-rental-ps.git
    cd gamezone-rental-ps
    ```

2. **Install Dependensi:**
   Pastikan Anda sudah menginstall Composer dan Node.js.

    ```bash
    composer install
    npm install
    ```

3. **Pengaturan Environment (.env):**
   Salin file `.env.example` menjadi `.env`.

    ```bash
    cp .env.example .env
    ```

4. **Generate Application Key:**

    ```bash
    php artisan key:generate
    ```

5. **Pengaturan Database:**
    - Buat database baru di MySQL/phpMyAdmin (contoh: `gamezone_db`).
    - Buka file `.env`, lalu ubah konfigurasi database Anda:
        ```env
        DB_CONNECTION=mysql
        DB_HOST=127.0.0.1
        DB_PORT=3306
        DB_DATABASE=gamezone_db
        DB_USERNAME=root
        DB_PASSWORD=
        ```
    - Import file `rental_ps_db.sql` ke dalam database Anda ATAU jalankan migrasi:
        ```bash
        php artisan migrate --seed
        ```

6. **Jalankan Aplikasi:**
   Buka dua jendela terminal, lalu jalankan:

    _Terminal 1 (Menjalankan server PHP):_

    ```bash
    php artisan serve
    ```

    _Terminal 2 (Menjalankan Vite/Frontend build):_

    ```bash
    npm run dev
    ```

    Buka `http://localhost:8000` di _browser_ Anda untuk melihat hasilnya.

---

_Dibuat untuk memenuhi Tugas Akhir Semester._

---

## 🔑 Akun Demo (Default Login)

Untuk keperluan pengujian aplikasi dan penilaian, silakan gunakan kredensial berikut untuk masuk sebagai Admin:

- **Email:** adminrentalps@gmail.com
- **Password:** rahasia

## 📈 Manajemen Proyek (Agile Workflow)

Progres pengerjaan tugas (_Issues_) dan pembagian kerja tim kami dikelola secara transparan menggunakan GitHub Projects.
Silakan cek alur kerja (_Kanban Board_) kami pada tautan berikut:
**[Lihat GameZone Development Board Disini](https://github.com/users/ruli162/projects/4/views/1)**

## 📄 Dokumen Laporan & Proposal Proyek

Untuk membaca proposal resmi proyek dan rincian lengkap mengenai spesifikasi kebutuhan perangkat lunak (*Software Requirements Specification*), silakan unduh dokumen kami di bawah ini:

📥 **[Unduh Dokumen Proposal Proyek Kelompok 4 Disini](docs/Proposal_Kelompok_4.pdf)**
📥 **[Unduh Dokumen Laporan SRS Kelompok 4 Disini](docs/Laporan_SRS_Kelompok_4.pdf)**
