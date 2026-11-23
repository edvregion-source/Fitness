# FORGE Fitness Goal Tracker (PWA starter)

## Jalankan lokal
Service worker/PWA membutuhkan HTTPS atau localhost. Dari folder ini jalankan:

```bash
python -m http.server 8000
```

Lalu buka `http://localhost:8000` di browser.

## Deploy
Upload seluruh isi folder ke static hosting yang menyediakan HTTPS (misalnya Netlify, Vercel static, atau GitHub Pages). Jangan hanya upload `index.html`; semua file harus berada dalam satu folder dengan struktur yang sama.

## Fitur yang tersedia
- Mode Trainer dan Client (pemilihan akun demo)
- CRUD profil client
- Measurement log (berat badan dan body fat)
- Workout log
- Nutrition/food log dan makro
- Progress photo upload (batas 1.8 MB per foto)
- Goal progress dashboard
- PWA manifest dan service worker cache untuk akses offline setelah kunjungan pertama

## Catatan penting sebelum dipakai oleh client sungguhan
Versi ini adalah prototype fungsional local-first. Data disimpan di `localStorage` browser/perangkat yang digunakan. Artinya data tidak otomatis tersinkron antar perangkat, browser, trainer, dan client. Pemilihan role adalah mode demo, bukan autentikasi aman; jangan memasukkan data pribadi sensitif atau membagikan deployment ini untuk penggunaan produksi multi-user.

Agar trainer dan client memiliki akun masing-masing dengan data yang tersinkron, perlu ditambahkan backend seperti Supabase atau Firebase, autentikasi, database terpusat, storage foto privat, serta aturan akses per client. Service worker hanya menyediakan cache/offline dasar; perubahan data offline belum memiliki mekanisme sinkronisasi konflik.
