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

### Minggu 1 ([15 November 2026] - [19 November 2026]): SRS Bab 1 sampai Bab 3
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

## Rencana Minggu Berikutnya
1. Melengkapi SRS (Bab 4 sampai 6).
2. Membuat ERD dan skema database MySQL.
3. Menyiapkan backend dan mulai mengerjakan fitur Autentikasi.
