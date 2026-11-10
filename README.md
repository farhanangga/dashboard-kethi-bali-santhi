# Dashboard Kerthi Bali Santhi (KBS)

Dashboard monitoring dan pengelolaan data **Kerthi Bali Santhi** yang dibangun menggunakan **Laravel**. Aplikasi ini menyajikan ringkasan statistik kendaraan secara visual, mulai dari identifikasi kendaraan masuk/keluar, registrasi, penerbitan RFID, penindakan, hingga pengaduan.

> Dikembangkan oleh **Farhan Angga Riyanto**

---

## Daftar Isi

- [Fitur Utama](#fitur-utama)
- [Modul Dashboard](#modul-dashboard)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Prasyarat](#prasyarat)
- [Instalasi](#instalasi)
- [Konfigurasi Environment](#konfigurasi-environment)
- [Menjalankan Aplikasi](#menjalankan-aplikasi)
- [Struktur Folder](#struktur-folder)
- [Screenshot](#screenshot)
- [Kontribusi](#kontribusi)
- [Lisensi](#lisensi)

---

## Fitur Utama

- Dashboard interaktif dengan **kartu statistik** (total data real-time).
- **Grafik** batang, garis/area, dan donat untuk visualisasi data.
- **Filter periode**: 7 Hari, 14 Hari, dan 1 Bulan.
- Pemisahan data kendaraan **Plat DK** dan **Plat Non DK**.
- Sidebar navigasi antar modul.
- Autentikasi pengguna (login/logout).
- Tampilan responsif dan modern.

## Modul Dashboard

### 1. Identifikasi
- Total Kendaraan Masuk
- Total Kendaraan Keluar
- Total Kendaraan Overstay
- Total Kendaraan On Stay
- Grafik Kendaraan Masuk & Keluar (Plat DK vs Non DK)
- Grafik Komersial Eksisting Masuk & Keluar
- Grafik Kendaraan On Stay & Overstay (Registrasi vs Non Registrasi)

### 2. Registrasi
- Total Registrasi
- Total Komersial Registrasi
- Total Registrasi Aktif
- Total Registrasi Non Aktif
- Total Pengajuan/Perpanjangan Registrasi
- Grafik Total Registrasi per Periode
- Grafik Donat Total Registrasi per Jenis Kendaraan (Motor, Mobil, Truk, Pickup, Trailer, Bus 3/4, Bus Besar, dll.)

### 3. Penerbitan
- Total Sudah Cetak RFID
- Total Belum Cetak RFID
- Total Kirim ke Alamat
- Total Kirim ke Kantor
- Grafik Cetak RFID
- Grafik Cetak Alamat

### 4. Penindakan
- Rekap data penindakan kendaraan.

### 5. Pengaduan
- Rekap data pengaduan masyarakat.

---

## Teknologi yang Digunakan

| Kategori | Teknologi |
|----------|-----------|
| Backend | Laravel (PHP) |
| Frontend | Blade Template, Tailwind CSS |
| Grafik | Chart.js |
| Database | MySQL / MariaDB |
| Build Tool | Vite |
| Package Manager | Composer & NPM |

> Sesuaikan tabel di atas jika ada perbedaan dengan stack yang Anda gunakan.

## Prasyarat

Pastikan sudah terpasang:

- PHP >= 8.1
- Composer
- Node.js >= 18 & NPM
- MySQL / MariaDB
- Git

## Instalasi

1. **Clone repository**

   ```bash
   git clone https://github.com/username/dashboard-kerthi-bali-santhi.git
   cd dashboard-kerthi-bali-santhi
   ```

2. **Install dependency PHP**

   ```bash
   composer install
   ```

3. **Install dependency frontend**

   ```bash
   npm install
   ```

4. **Salin file environment**

   ```bash
   cp .env.example .env
   ```

5. **Generate application key**

   ```bash
   php artisan key:generate
   ```

## Konfigurasi Environment

Buka file `.env` lalu sesuaikan konfigurasi database:

```env
APP_NAME="Dashboard Kerthi Bali Santhi"
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost:8000

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=kerthi_bali_santhi
DB_USERNAME=root
DB_PASSWORD=
```

Kemudian jalankan migrasi dan seeder:

```bash
php artisan migrate --seed
```

## Menjalankan Aplikasi

Jalankan server Laravel:

```bash
php artisan serve
```

Pada terminal lain, jalankan Vite:

```bash
npm run dev
```

Buka di browser: [http://localhost:8000](http://localhost:8000)

Untuk build production:

```bash
npm run build
```

## Struktur Folder

```
dashboard-kerthi-bali-santhi/
├── app/
│   ├── Http/Controllers/     # Controller tiap modul
│   └── Models/               # Model Eloquent
├── database/
│   ├── migrations/           # Struktur tabel
│   └── seeders/              # Data awal
├── public/                   # Aset publik
├── resources/
│   ├── css/
│   ├── js/                   # Script grafik
│   └── views/
│       ├── layouts/          # Layout & sidebar
│       └── dashboard/        # Identifikasi, Registrasi, Penerbitan,
│                             # Penindakan, Pengaduan
├── routes/
│   └── web.php               # Routing aplikasi
├── .env.example
└── README.md
```

## Screenshot

Letakkan gambar di folder `docs/screenshots/` lalu tautkan di sini:

| Identifikasi | Registrasi |
|:---:|:---:|
| ![Identifikasi](docs/screenshots/identifikasi.png) | ![Registrasi](docs/screenshots/registrasi.png) |

| Penerbitan | Penindakan & Pengaduan |
|:---:|:---:|
| ![Penerbitan](docs/screenshots/penerbitan.png) | ![Penindakan](docs/screenshots/penindakan.png) |

## Kontribusi

1. Fork repository ini
2. Buat branch fitur: `git checkout -b fitur/nama-fitur`
3. Commit perubahan: `git commit -m "Menambahkan fitur ..."`
4. Push ke branch: `git push origin fitur/nama-fitur`
5. Buat Pull Request

## Lisensi

Proyek ini dirilis di bawah lisensi [MIT](LICENSE).

---

**Farhan Angga Riyanto**
