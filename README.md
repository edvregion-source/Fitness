# Ember Fitness

Aplikasi fitness tema gelap merah-putih. Kode aplikasinya ada di `www/index.html`, lalu dibungkus jadi aplikasi Android dengan Capacitor.

## Cara mendapatkan APK

1. Buat repo baru di GitHub, lalu unggah semua isi folder ini (termasuk folder `.github`).
2. Buka tab **Actions** di repo, pilih **Build Android APK**, lalu **Run workflow**. Build juga jalan otomatis setiap push ke branch `main`.
3. Tunggu sekitar 5 menit sampai build hijau.
4. Buka run yang selesai, lalu unduh **ember-fitness-apk** dari bagian Artifacts. Di dalamnya ada `app-debug.apk`.
5. Kirim APK ke HP Android, buka, lalu izinkan pemasangan dari sumber tidak dikenal.

## Mengubah aplikasi

Edit `www/index.html`, lalu push. APK baru dibuat otomatis.

## Catatan

- APK ini bertipe debug, cukup untuk dipakai sendiri. Untuk Play Store perlu APK/AAB bertanda tangan (release).
- Data latihan tersimpan di penyimpanan aplikasi pada perangkat itu saja.
- Versi iOS butuh Mac dan akun Apple Developer, jadi belum disertakan.
