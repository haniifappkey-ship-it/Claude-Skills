---
name: laporan-harian
description: Membuat laporan harian kerja dalam format yang rapi dan terstruktur. Gunakan skill ini setiap kali pengguna ingin mencatat kegiatan kerja harian, membuat daily report, atau mendokumentasikan hasil kerja hari ini. Trigger skill ini ketika pengguna menyebut kata "laporan", "laporan harian", "laporan kerja", "bikin laporan", "catat kegiatan", "log kerja", "daily report", atau ingin merangkum aktivitas kerjanya hari ini.
---

# Laporan Harian Kerja

Skill ini membantu user untuk membuat laporan harian yang rapi, singkat, dan profesional — mencakup identitas, kegiatan yang dikerjakan, kendala, dan hasil pada hari ini.

---

## Cara Kerja Skill Ini

### Langkah 1: Tanyakan Informasi yang Dibutuhkan

Tanyakan semua informasi berikut dalam **satu pesan sekaligus**, jika belum disebutkan pengguna:

> "Halo! Yuk bikin laporan hariannya 📝 Aku butuh beberapa info dulu:
> 1. 📅 Hari, tanggal, dan jam berapa sekarang?
> 2. 👤 Nama kamu siapa?
> 3. ✅ Kegiatan apa aja yang kamu kerjakan hari ini? (boleh lebih dari satu)
> 4. 🎯 Apa hasil dari kegiatan tersebut?
> 5. ⚠️ Ada kendala nggak?

Tunggu pengguna menjawab sebelum membuat laporan.

> jika dijawab, coba tanyakan sekali lagi, apakah ada rencana untuk besok. jika memang user tidak ingin dibuatkan dan membuat rencana besok., skip,  dan lanjutkan ke berikutnya.

> Jika pengguna sudah menyebutkan sebagian informasi di awal, jangan tanya ulang — langsung tanyakan yang kurang saja.

---

### Langkah 2: Buat Laporan dalam Format Teks Rapi

Setelah semua data terkumpul, susun laporan dengan format berikut:

```
📋 LAPORAN HARIAN 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

👤 Nama    : [Nama]
📅 Tanggal : [Hari, DD Bulan YYYY]
🕐 Waktu   : [HH.MM] WIB

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
KEGIATAN YANG DILAKUKAN
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. [Kegiatan pertama]
2. [Kegiatan kedua]
3. [dst...]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
KENDALA
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Isi kendala yang dihadapi, atau "-" jika tidak ada]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
HASIL & CATATAN
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Apa yang berhasil diselesaikan atau dicapai hari ini]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
REMINDER!! 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[rencana yang disiapkan untik hari berikutnya. jika user tidak meminta, cukup berikan "-"]
```

---

## Aturan Penting

- Judul section selalu UPPERCASE
- Jika kendala dikosongkan atau diisi "-", tetap tampilkan bagian KENDALA dengan isi "-"
- Jika pengguna menyebutkan lebih dari satu kegiatan, buat sebagai list bernomor
- Gunakan bahasa yang sopan dan profesional di dalam laporan
- Output laporan berupa teks plain (bukan artifact, bukan HTML) — langsung di chat
- Setelah laporan selesai, tambahkan 1 kalimat pendek yang semangat/encouraging

---

## Catatan untuk Claude

- Jika pengguna langsung kasih semua info dalam satu pesan, jangan tanya lagi — langsung buatkan laporan
- Jika ada info yang kurang, tanyakan yang kurang saja (bukan semua ulang dari awal)
- Kegiatan yang disebutkan dengan bahasa santai boleh sedikit dirapikan ke bahasa yang lebih formal untuk isi laporan
- Jangan ubah makna atau fakta yang disampaikan pengguna
