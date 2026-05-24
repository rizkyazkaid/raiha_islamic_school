# 📚 Rekap Absen & Nilai - Raiha Islamic School

![Version](https://img.shields.io/badge/version-1.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-active-success)

Aplikasi web interaktif untuk mencatat dan mengelola data absensi dan nilai siswa di Raiha Islamic School dengan fitur lengkap dan desain modern.

---

## ✨ Fitur Utama

### 📝 **Manajemen Data**
- ✅ **Tambah Data** - Menambahkan data siswa baru dengan validasi lengkap
- ✏️ **Edit Data** - Mengubah data siswa yang sudah ada via modal form
- 🗑️ **Hapus Data** - Menghapus data individual dengan konfirmasi
- 🗑️ **Hapus Semua** - Menghapus seluruh data sekaligus dengan warning

### 💾 **Penyimpanan Data**
- 🔒 Semua data disimpan **LOKAL** di Browser (localStorage)
- 📱 Data **otomatis tersimpan** setiap kali ada perubahan
- ⚡ Data **tidak hilang** saat refresh halaman
- 🌐 **Bekerja offline** - Tidak perlu koneksi internet

### 🔍 **Pencarian & Filter**
- 🔎 **Cari berdasarkan nama** - Real-time search
- 🎯 **Filter berdasarkan kelas** - Pilih kelas tertentu
- 📊 **Filter berdasarkan status absen** - Hadir, Tidak Hadir, Sakit, Izin
- 🔄 **Reset filter** - Kembali ke tampilan semua data

### 📊 **Statistik Real-time**
- 👥 Total jumlah siswa terdaftar
- ✅ Jumlah siswa hadir
- ❌ Jumlah siswa tidak hadir
- 🤒 Jumlah siswa sakit
- 📝 Jumlah siswa izin
- 📈 Rata-rata nilai seluruh siswa

### 📥 **Export & Print**
- 📥 **Export CSV** - Unduh data dalam format .csv untuk Excel/Google Sheets
- 🖨️ **Print** - Cetak laporan langsung dari browser
- 📄 **Automatic naming** - File diberi nama dengan tanggal otomatis

### 🎨 **User Interface**
- 💎 Desain modern dengan gradient colors
- 📱 **Responsive design** - Bekerja sempurna di desktop, tablet, mobile
- ⚡ **Loading cepat** - Vanilla JavaScript, tanpa dependency eksternal
- 🎯 **User-friendly** - Interface yang intuitif dan mudah digunakan
- 🔔 **Toast notifications** - Alert berhasil/error yang informatif

### 🏫 **Kelengkapan Kelas & Status**
```
Kelas Tersedia: 10A, 10B, 11A, 11B, 12A, 12B
Status Absen: ✅ Hadir, ❌ Tidak Hadir, 🤒 Sakit, 📝 Izin
```

---

## 🚀 Cara Menggunakan

### 1️⃣ **Membuka Aplikasi**

**Online (Recommended):**
```
https://raw.githubusercontent.com/rizkyazkaid/raiha_islamic_school/main/preview.html
```

**Atau offline:**
- Download file `preview.html`
- Buka dengan double-click atau drag ke browser

### 2️⃣ **Menambah Data Siswa**

1. Masukkan **Nama Siswa** di field input
2. Pilih **Kelas** dari dropdown (10A - 12B)
3. Masukkan **Nilai** (0-100)
4. Pilih **Status Absen** (Hadir/Tidak Hadir/Sakit/Izin)
5. Klik tombol **➕ Tambah Data**
6. Data akan muncul di tabel dan **otomatis tersimpan**

### 3️⃣ **Mengedit Data**

1. Temukan data yang ingin diubah di tabel
2. Klik tombol **Edit** pada baris tersebut
3. Modal form akan muncul dengan data lama
4. Ubah data sesuai kebutuhan
5. Klik **Simpan** untuk menyimpan perubahan

### 4️⃣ **Menghapus Data**

**Hapus satu data:**
1. Klik tombol **Hapus** pada baris data
2. Konfirmasi penghapusan
3. Data akan terhapus dan tabel terupdate

**Hapus semua data:**
1. Klik tombol **🗑️ Hapus Semua**
2. Baca warning dengan seksama
3. Konfirmasi untuk menghapus semua data sekaligus

### 5️⃣ **Memfilter & Mencari**

**Filter Kelas:**
```
1. Buka dropdown "Filter Kelas"
2. Pilih kelas yang ingin dilihat
3. Tabel akan update otomatis
```

**Filter Status Absen:**
```
1. Buka dropdown "Filter Absen"
2. Pilih status (Hadir/Tidak Hadir/Sakit/Izin)
3. Tabel akan menampilkan data sesuai filter
```

**Cari Berdasarkan Nama:**
```
1. Ketik nama siswa di field "Cari Nama"
2. Pencarian real-time akan bekerja
3. Tabel update saat Anda mengetik
```

**Reset Semua Filter:**
```
1. Klik tombol "🔄 Reset Filter"
2. Semua data akan ditampilkan kembali
```

### 6️⃣ **Export Data**

**Export ke CSV (Excel):**
1. Klik tombol **📥 Export CSV**
2. File `rekap_absen_YYYY-MM-DD.csv` akan diunduh
3. Buka di Excel atau Google Sheets

**Format CSV yang dihasilkan:**
```csv
No,Nama,Kelas,Nilai,Absen
1,Ahmad Rizki,10A,85,Hadir
2,Siti Nurhaliza,10B,92,Hadir
3,Budi Santoso,11A,78,Sakit
```

### 7️⃣ **Mencetak Laporan**

1. Klik tombol **🖨️ Print**
2. Preview cetak akan muncul
3. Sesuaikan pengaturan printer (ukuran kertas, margin, dll)
4. Klik **Print** untuk mencetak

---

## 📊 Struktur Data

Setiap entri siswa menyimpan informasi berikut:

```javascript
{
  "nama": "Nama Siswa",      // String
  "kelas": "10A",            // String (10A-12B)
  "nilai": 85,               // Number (0-100)
  "absen": "Hadir"           // String (Hadir/Tidak Hadir/Sakit/Izin)
}
```

**Contoh array lengkap:**
```javascript
[
  { nama: "Ahmad Rizki", kelas: "10A", nilai: 85, absen: "Hadir" },
  { nama: "Siti Nurhaliza", kelas: "10B", nilai: 92, absen: "Hadir" },
  { nama: "Budi Santoso", kelas: "11A", nilai: 78, absen: "Sakit" }
]
```

---

## 💾 Penyimpanan Data (localStorage)

**Key**: `rekapData`  
**Format**: JSON Array  
**Lokasi**: Browser's Local Storage  
**Kapasitas**: ~5-10MB (tergantung browser)  
**Durasi**: Permanen (sampai dihapus atau cache dibersihkan)

### Cara Mengecek Data di Console:
```javascript
// Buka DevTools (F12), masuk tab Console, ketik:
JSON.parse(localStorage.getItem('rekapData'))

// Hapus semua data:
localStorage.removeItem('rekapData')

// Backup data:
copy(localStorage.getItem('rekapData'))
```

---

## 🎨 Desain & UI

### Palet Warna
| Elemen | Warna | Kode |
|--------|-------|------|
| Primary | Purple | #667eea to #764ba2 |
| Success | Green | #28a745 to #20c997 |
| Danger | Red | #dc3545 to #fd7e14 |
| Background | Light Gray | #f8f9fa |

### Komponen UI
- ✅ Form input dengan validasi
- ✅ Tabel responsif dengan action buttons
- ✅ Modal dialog untuk edit data
- ✅ Statistics cards dengan gradient
- ✅ Alert notifications (success/error)
- ✅ Filter dropdown dengan real-time search

---

## 📱 Kompatibilitas

### Browser yang Didukung
| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 60+ | ✅ Penuh |
| Firefox | 55+ | ✅ Penuh |
| Safari | 12+ | ✅ Penuh |
| Edge | 79+ | ✅ Penuh |
| Opera | 47+ | ✅ Penuh |

### Perangkat yang Didukung
- ✅ Desktop (Windows, Mac, Linux)
- ✅ Laptop
- ✅ Tablet (iPad, Android)
- ✅ Mobile (Smartphone Android & iOS)

---

## 🔐 Keamanan & Privasi

### Data Privacy
- ✅ **Semua data tersimpan LOKAL** di device Anda
- ✅ **TIDAK ada data** yang dikirim ke server eksternal
- ✅ **Bekerja OFFLINE** - tidak perlu internet setelah pertama kali loading
- ✅ **Aman dari pihak ketiga** - hanya browser Anda yang bisa akses

### Catatan Penting
- ⚠️ Data akan terhapus jika Anda **clear browser cache/cookies**
- ⚠️ Data tidak tersinkronisasi antar device
- ⚠️ Backup data secara berkala dengan export CSV

---

## 📝 Validasi Form

### Input Validation
- ✅ Nama siswa **tidak boleh kosong**
- ✅ Nama siswa **tidak boleh hanya spasi**
- ✅ Kelas **harus dipilih**
- ✅ Nilai **harus angka**
- ✅ Nilai **harus 0-100**
- ✅ Status absen **harus dipilih**

### Error Messages
```
"Semua field harus diisi dengan benar!" - Ada field yang kosong
"Nilai harus antara 0-100!" - Nilai di luar range
"Tidak ada data untuk diekspor!" - Tabel kosong saat export
"Tidak ada data untuk dicetak!" - Tabel kosong saat print
```

---

## 🎯 Tips & Trik

### 💡 Tips Penggunaan
1. **Backup Data Rutin** - Export CSV setiap minggu untuk backup
2. **Gunakan Nama Unik** - Hindari nama yang sama untuk kemudahan pencarian
3. **Clear Filter Sebelum Menambah** - Pastikan filter reset saat tambah data
4. **Gunakan Offline** - Buka sekali, gunakan berkali-kali tanpa internet

### ⚠️ Peringatan Penting
1. **Jangan hapus cache browser** - Data akan hilang selamanya
2. **Jangan copy data manual** - Gunakan export CSV untuk backup
3. **Backup di multiple devices** - Gunakan cloud storage untuk file CSV

---

## 🆘 Troubleshooting

### ❓ Data Hilang?
**Penyebab:** Browser cache/cookies dihapus, atau storage limit tercapai
**Solusi:** 
- Restore dari backup CSV jika ada
- Masukkan ulang data
- Gunakan export CSV rutin

### ❓ Export CSV tidak bekerja?
**Penyebab:** Browser tidak support atau blocked
**Solusi:**
- Gunakan browser modern (Chrome, Firefox, Edge)
- Disable ad-blocker
- Coba browser berbeda

### ❓ Filter tidak bekerja?
**Penyebab:** Cache browser atau JavaScript disabled
**Solusi:**
- Refresh halaman (F5)
- Buka di Incognito Mode
- Enable JavaScript di browser

### ❓ Modal edit tidak muncul?
**Penyebab:** JavaScript error atau CSS conflict
**Solusi:**
- Buka DevTools (F12) cek Console
- Clear browser cache
- Coba browser berbeda

---

## 🛠️ Teknologi yang Digunakan

### Frontend Stack
| Teknologi | Fungsi |
|-----------|--------|
| HTML5 | Struktur halaman |
| CSS3 | Styling & Responsive Design |
| JavaScript (Vanilla) | Logika aplikasi, tanpa dependency |
| LocalStorage API | Penyimpanan data lokal |
| Print API | Fungsi cetak |
| Fetch API | Potensial integrasi backend |

### Fitur Modern yang Digunakan
- ES6 Arrow Functions
- Template Literals
- Array Methods (filter, map, reduce)
- Event Listeners
- DOM Manipulation
- Modal Dialog Pattern

---

## 📥 Download & Deploy

### Cara Menggunakan Lokal

1. **Download File**
   ```
   Klik tombol Raw di GitHub
   Simpan as preview.html
   ```

2. **Buka di Browser**
   ```
   Double-click preview.html
   atau
   Drag ke window browser
   ```

3. **Mulai Gunakan**
   ```
   Aplikasi siap digunakan offline
   Data otomatis tersimpan
   ```

### Cara Deploy ke GitHub Pages

1. **Fork Repositori**
   ```
   https://github.com/rizkyazkaid/raiha_islamic_school
   ```

2. **Enable GitHub Pages**
   - Settings → Pages
   - Source: main branch
   - Custom domain: (optional)

3. **Akses Aplikasi**
   ```
   https://username.github.io/raiha_islamic_school/preview.html
   ```

### Cara Deploy ke Hosting Lain

1. **Upload file**
   - preview.html
   - README.md (optional)

2. **Akses via URL**
   ```
   https://yourdomain.com/preview.html
   ```

3. **Share link**
   ```
   Guru bisa akses kapan saja
   ```

---

## 📞 Support & Kontribusi

### Lapor Bug
Jika menemukan bug, silakan:
1. Buka GitHub Issues
2. Jelaskan bug dengan detail
3. Sertakan screenshot jika perlu

### Saran Fitur
Punya ide fitur baru? 
1. Buka GitHub Discussions
2. Jelaskan fitur yang diinginkan
3. Tunggu feedback dari tim

### Kontribusi Kode
Ingin berkontribusi?
1. Fork repositori
2. Buat branch baru
3. Commit changes
4. Push dan buat Pull Request

---

## 📄 Lisensi & Kredit

**Lisensi**: MIT License  
**Pembuat**: Raiha Islamic School  
**Last Updated**: 2026-05-24

### Terimakasih kepada:
- ✅ HTML5 & CSS3 Standards
- ✅ JavaScript Community
- ✅ GitHub Platform
- ✅ All contributors

---

## 📋 Changelog

### Version 1.0 (2026-05-24)
- ✨ Release fitur lengkap
- ✅ Edit & Delete functionality
- ✅ LocalStorage persistence
- ✅ Advanced filtering & search
- ✅ Real-time statistics
- ✅ CSV export & Print
- ✅ Responsive design
- ✅ Dark mode support (planned)
- ✅ Multi-language support (planned)

---

## 🎓 Catatan untuk Pengguna

Aplikasi ini dirancang khusus untuk **Raiha Islamic School** dengan tujuan:
- 📚 Memudahkan pencatatan absensi siswa
- 📊 Memudahkan pencatatan nilai siswa
- 📈 Analisis data attendance & performance
- 🎯 Mendukung proses pembelajaran yang lebih efisien

**Semoga aplikasi ini bermanfaat!** 🙏

---

**Made with ❤️ for Raiha Islamic School**

`Last Updated: 2026-05-24 | Version 1.0 | Status: Active ✅`
