# Project Requirement Document (PRD)

**Nama Proyek:** SIMPEL (Sistem Informasi Manajemen Pendidikan Terintegrasi)
**Platform:** Web
**Tanggal:** _______________
**Versi:** 1.0

---

## 2.1 Ringkasan Proyek

Sistem berbasis web untuk mengelola kegiatan akademik di TK, SD, SMP, SMA.
Target pengguna: guru, siswa, staf akademik, orang tua.

---

## 2.2 Ruang Lingkup Fungsional (Modul)

| Modul | Deskripsi |
|---|---|
| Manajemen Pengguna | Registrasi, login, role-based access (admin, guru, siswa, orang tua) |
| Manajemen Kelas & Mapel | Buat kelas, rombel, mata pelajaran, jadwal |
| Manajemen Nilai | Input nilai harian, UTS, UAS, hitung rata-rata |
| Manajemen Absensi | Rekap kehadiran per siswa per pertemuan |
| Manajemen Tugas | Guru buat tugas, siswa upload, nilai otomatis/tulis |
| Laporan Akademik | Cetak rapor, transkrip, rekap kelas |
| Dashboard Orang Tua | Monitoring nilai, absensi, pengumuman |
| Pengumuman & Notifikasi | Broadcast pengumuman ke level kelas/sekolah |

---

## 2.3 Kebutuhan Non-Fungsional

| Aspek | Spesifikasi |
|---|---|
| Performa | Waktu muat halaman < 2 detik |
| Keamanan | Password hash (BCrypt), session timeout, HTTPS |
| Ketersediaan | Uptime 99% (jam sekolah 07.00–17.00) |
| Skalabilitas | Dukung hingga 5.000 pengguna aktif per sekolah |
| Kompatibilitas | Chrome, Firefox, Edge, Safari (2 versi terakhir) |
| Aksesibilitas | Ramah pengguna dengan keterbatasan (WCAG 2.1 level A) |

---

## 2.4 Arsitektur Teknis (Direkomendasikan)

| Komponen | Teknologi |
|---|---|
| Frontend | HTML5, CSS3, JavaScript (React.js atau Laravel Blade) |
| Backend | Laravel (PHP) atau Node.js + Express |
| Database | MySQL / PostgreSQL |
| Authentication | JWT + Session-based (role: admin/guru/siswa/orangtua) |
| Hosting | Cloud (AWS, DigitalOcean, atau shared hosting support PHP/MySQL) |

---

## 2.5 User Stories

1. **Sebagai guru**, saya ingin menginput nilai per siswa per mata pelajaran agar dapat melihat rata-rata kelas secara otomatis.
2. **Sebagai orang tua**, saya ingin melihat kehadiran anak saya hari ini tanpa harus datang ke sekolah.
3. **Sebagai siswa**, saya ingin mengunduh jadwal pelajaran dalam format PDF.
4. **Sebagai staf akademik**, saya ingin mencetak rapor seluruh kelas dalam satu klik.

---

## 2.6 Batasan & Risiko

| Risiko | Mitigasi |
|---|---|
| Orang tua tidak melek teknologi | Web sederhana + panduan penggunaan (video/PDF) |
| Gangguan server saat ujian | Backup server atau mode offline temporer |
| Data hilang | Backup database terjadwal setiap hari |

---

## 2.7 Deliverables

- Source code sistem web
- Database schema & seed data
- Panduan instalasi & admin manual
- User guide untuk guru, siswa, orang tua
- Demo / staging server untuk uji coba

---

## 2.8 Timeline Indikatif (12 Minggu)

| Minggu | Aktivitas |
|---|---|
| 1–2 | Analisis kebutuhan, desain database |
| 3–6 | Pengembangan backend & REST API |
| 7–9 | Frontend & integrasi |
| 10 | UAT (User Acceptance Test) di 1 sekolah rintisan |
| 11 | Perbaikan & deployment |
| 12 | Serah terima & pelatihan |