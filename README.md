# Showtix: Aplikasi Pemesanan Tiket Pertunjukan Seni

Showtix adalah aplikasi mobile Android (Jetpack Compose) untuk melihat event
pertunjukan seni seperti teater, orkestra, dan tari, lalu memesan tiketnya.
Pengguna bisa melihat detail event, sisa tiket, dan batas pendaftaran, lalu
memesan tiket dengan transfer bank (upload bukti) atau bayar di loket. Admin
mengelola event dan tipe tiket, serta memverifikasi pesanan.

## Teknologi
- Android: Kotlin, Jetpack Compose, Navigation Compose, MVVM
- Backend: Node.js + Express (REST API, JSON)
- Database: PostgreSQL (cloud, [nama layanan])
- Autentikasi: JWT (access token) + refresh token

## Fitur
| No | Fitur | Status |
|----|-------|--------|
| 1 | Autentikasi (register, login, JWT, refresh token) 
| 2 | Kelola Kategori (CRUDS) 
| 3 | Kelola dan Lihat Event (CRUDS) 
| 4 | Kelola Tipe Tiket (CRUDS) 
| 5 | Pemesanan Tiket (CRUDS, upload bukti, invoice) 
| 6 | Favorit (CRUDS) 

### Week 9 [15 November 2026] - [19 November 2026]: SRS Bab 1 sampai Bab 3
- **Bab 1 (Pendahuluan)**: menyusun tujuan dokumen, konvensi penulisan
  (kode kebutuhan REQ-nomor dan prioritas), target pembaca, ruang lingkup
  project, referensi, serta daftar singkatan dan akronim.
- **Bab 2 (Deskripsi Umum)**: menjelaskan perspektif produk (aplikasi Android
  terhubung ke REST API dan database MySQL), merangkum enam fitur utama
  (Autentikasi, Kategori, Event, Tipe Tiket, Pemesanan, Favorit),
  mendefinisikan dua kelas pengguna (Admin dan Pengguna), lingkungan operasi,
  batasan desain, serta asumsi dan ketergantungan sistem.
- **Bab 3 (Fitur Sistem)**: menyusun kebutuhan fungsional untuk keenam fitur,
  masing-masing berisi deskripsi dan prioritas, urutan aksi dan respons,
  serta daftar kebutuhan (REQ). Di dalamnya dirinci logika sisa tiket per tipe,
  label "Tiket habis terjual", status pesanan (Menunggu, Dikonfirmasi,
  Ditolak), dan dua metode pembayaran (transfer dengan upload bukti, dan
  bayar di loket).

### Week 10 [20 November 2026 - 24 November 2026] Penyempurnaan SRS (Bab 4 sampai 6) dan Pembuatan Diagram

Di minggu ini aku melanjutkan penyusunan dokumen SRS Showtix dan melengkapi diagram pendukungnya. Belum ada kode aplikasi yang ditulis, jadi fokusnya masih di perancangan.

**Bab 4: Kebutuhan Antarmuka Eksternal**
Berisi gambaran bagaimana aplikasi berhubungan dengan pihak luar, yaitu antarmuka pengguna (halaman-halaman yang dipakai pengguna dan admin), antarmuka perangkat keras (kebutuhan perangkat Android, kamera untuk memindai barcode, dan akses penyimpanan), serta antarmuka perangkat lunak (komunikasi aplikasi dengan REST API dan basis data).

**Bab 5: Kebutuhan Nonfungsional**
Berisi syarat mutu aplikasi di luar fitur utama, seperti kinerja, keamanan (login, token, dan penyimpanan kata sandi), kemudahan penggunaan, keandalan, dan kemudahan pemeliharaan. Isinya kubuat secara umum agar tetap sesuai dengan aplikasi ketika sudah jadi.

**Bab 6: Kebutuhan Lain (Basis Data)**
Berisi rancangan data aplikasi, terdiri dari:
- **ERD**: gambaran data apa saja yang dikelola dan bagaimana hubungannya (User, Kategori, Event, TipeTiket, Pemesanan, dan Favorit).
- **RAT (Relasi Antar Tabel)**: struktur tabel yang sebenarnya, lengkap dengan kunci utama dan kunci tamu, beserta aturan saat data induk dihapus.
- **Kamus Data**: daftar kolom setiap tabel beserta tipe datanya.

**Diagram pendukung**
- Use case diagram beserta penjelasan alurnya.
- Flowchart untuk tiap fitur utama (Autentikasi, Kategori, Event, Tipe Tiket, Pemesanan, dan Favorit), dengan pembagian peran Admin dan Pengguna.
- ERD dan RAT.

**Keputusan teknis yang diambil**
- Backend memakai Node.js dengan Express (REST API).
- Basis data memakai PostgreSQL di layanan cloud.
- Autentikasi memakai JWT dengan refresh token.

**Rencana minggu berikutnya**
Menyiapkan struktur proyek (Android dan backend), membuat basis data sesuai RAT, lalu mulai mengerjakan fitur autentikasi.
