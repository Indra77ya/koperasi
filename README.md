# Sistem Manajemen Koperasi

Aplikasi web untuk mengelola operasional koperasi termasuk manajemen anggota, simpanan, pinjaman, dan laporan keuangan.

## Fitur Utama

- **Manajemen Anggota**: Pendaftaran dan pengelolaan data anggota koperasi
- **Manajemen Simpanan**: Pencatatan simpanan sukarela dan wajib anggota
- **Manajemen Pinjaman**: Proses pengajuan, persetujuan, dan pembayaran pinjaman
- **Manajemen Kas**: Pencatatan kas masuk dan kas keluar
- **Laporan Keuangan**: 
  - Neraca
  - Buku Besar
  - Jurnal Umum
  - Laporan Laba/Rugi
  - Trial Balance
  - SHU (Sisa Hasil Usaha)
  - Dan laporan lainnya
- **Manajemen Akun**: Pengelolaan akun, grup akun, dan user management

## Prasyarat

Sebelum menginstal, pastikan Anda telah menginstal:

- **XAMPP** (versi 7.0 atau lebih tinggi) atau web server lainnya dengan PHP
- **PHP** 5.6 atau lebih tinggi
- **MySQL** 5.5 atau lebih tinggi
- **Web Browser** modern (Chrome, Firefox, Safari, Edge)

## Instalasi

### 1. Download dan Extract

```bash
# Clone atau download repository
git clone https://github.com/username/koperasi.git
# atau
# Download ZIP dan extract ke folder koperasi
```

### 2. Letakkan di Folder Web Server

```bash
# Untuk XAMPP, copy ke folder htdocs
cp -r koperasi C:\xampp\htdocs\
# atau untuk Linux/Mac
cp -r koperasi /Applications/XAMPP/htdocs/
```

### 3. Konfigurasi Database

1. Buat database baru di MySQL:
```sql
CREATE DATABASE koperasi;
```

2. Buka file `application/config/database.php` dan sesuaikan konfigurasi:

```php
$db['default'] = array(
    'dsn'   => '',
    'hostname' => 'localhost',
    'username' => 'root',           // User MySQL Anda
    'password' => '',               // Password MySQL Anda
    'database' => 'koperasi',       // Nama database
    'dbdriver' => 'mysqli',
    'char_set' => 'utf8',
    'dbcollat' => 'utf8_general_ci',
    // ... konfigurasi lainnya
);
```

### 4. Import Database

1. Buka phpMyAdmin: `http://localhost/phpmyadmin`
2. Pilih database `koperasi`
3. Buka tab **Import**
4. Pilih file `database/database.sql`
5. Klik **Go** untuk mengimport

Atau gunakan command line:
```bash
mysql -u root -p koperasi < database/database.sql
```

### 5. Konfigurasi Base URL

Edit file `application/config/config.php`:

```php
$config['base_url'] = 'http://localhost/koperasi/';
```

Sesuaikan dengan URL aplikasi Anda (misalnya: `http://nama-domain.com/` jika deployment ke server)

### 6. Folder Permissions

Pastikan folder berikut memiliki permission yang tepat:

```bash
# Untuk Linux/Mac
chmod 755 application/cache
chmod 755 application/logs
chmod 755 uploads

# Untuk Windows, pastikan folder accessible oleh web server
```

### 7. Akses Aplikasi

Buka browser dan akses:
```
http://localhost/koperasi/
```

## Struktur Folder

```
koperasi/
├── application/           # Main application folder
│   ├── config/           # Konfigurasi aplikasi
│   ├── controllers/      # Controller classes
│   ├── models/           # Model classes
│   ├── views/            # View templates
│   ├── libraries/        # Custom libraries
│   ├── helpers/          # Helper functions
│   ├── cache/            # Cache files
│   └── logs/             # Log files
├── system/               # CodeIgniter core files
├── assets/               # Static files (CSS, JS, images)
│   ├── theme_admin/      # Admin theme
│   ├── easyui/           # EasyUI library
│   ├── jquery_ui/        # jQuery UI library
│   └── uploads/          # User uploads directory
├── database/             # Database files
│   ├── database.sql      # Main database dump
│   └── views/            # Database views scripts
├── views/                # Standalone view files
├── index.php             # Entry point
└── README.md             # Documentation (file ini)
```

## Konfigurasi Awal Aplikasi

### Akun Login Default

Setelah mengimport database, Anda dapat login dengan akun default:

- **Username**: `admin`
- **Password**: `admin`

⚠️ **Penting**: Ubah password default setelah login pertama kali!

### Konfigurasi Setting Aplikasi

1. Login ke aplikasi
2. Masuk ke menu **Setting**
3. Atur:
   - Nama koperasi
   - Alamat
   - Kontak
   - Periode/Tahun buku
   - Dan pengaturan lainnya

## Database Schema

Database terdiri dari beberapa tabel utama:

- **tbl_anggota**: Data anggota koperasi
- **tbl_simpanan**: Transaksi simpanan
- **tbl_pinjaman**: Data pinjaman
- **tbl_angsuran**: Pembayaran angsuran
- **tbl_akun**: Daftar akun (Chart of Accounts)
- **tbl_jurnal**: Jurnal transaksi
- **tbl_kas_masuk**: Kas masuk
- **tbl_kas_keluar**: Kas keluar
- **tbl_user**: Data user/admin

## Penggunaan

### Menu Utama

1. **Dashboard**: Overview aplikasi
2. **Anggota**: Manajemen data anggota
3. **Simpanan**: Pencatatan simpanan anggota
4. **Pinjaman**: Manajemen pengajuan dan pembayaran pinjaman
5. **Kas**: Pencatatan kas masuk dan keluar
6. **Laporan**: Berbagai laporan keuangan
7. **Setting**: Konfigurasi aplikasi dan user

## Troubleshooting

### Masalah Koneksi Database

Jika mendapat error koneksi database:

1. Pastikan MySQL service berjalan
2. Cek username dan password di `application/config/database.php`
3. Pastikan database `koperasi` sudah dibuat
4. Cek bahwa file database sudah di-import

### Masalah File Upload

Jika upload gagal:

1. Pastikan folder `uploads/` ada dan writable
2. Cek folder `application/cache/` permissions
3. Cek PHP `max_upload_size` dan `post_max_size`

### Masalah Base URL

Jika halaman tidak tampil dengan benar:

1. Verifikasi konfigurasi `application/config/config.php`
2. Pastikan folder `koperasi/` sudah di root web server
3. Jika menggunakan subdomain, update base URL sesuai

## Teknologi yang Digunakan

- **Framework**: CodeIgniter 2.x
- **Database**: MySQL
- **Frontend**: jQuery, EasyUI, jQuery UI
- **Bahasa**: PHP, JavaScript, HTML/CSS

## Lisensi

[Tentukan lisensi Anda di sini]

## Support & Dokumentasi

Untuk dokumentasi lebih lanjut atau bantuan:
- [Dokumentasi CodeIgniter](https://codeigniter.com/user_guide/)
- [Dokumentasi EasyUI](https://www.jeasyui.com/documentation/)

## Notes Pengembang

- Aplikasi menggunakan CodeIgniter framework
- Database migration disimpan di folder `database/`
- Custom libraries berada di `application/libraries/`
- Helper functions tersimpan di `application/helpers/`

## Changelog

### v1.0
- Initial release
- Fitur dasar manajemen koperasi

---

**Dibuat dengan ❤️ untuk pengelolaan koperasi yang lebih baik**
