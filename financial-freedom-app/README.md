# Financial Freedom: aplikasi HP

Paket ini berisi Financial Freedom dalam dua bentuk:

- **Aplikasi web yang bisa dipasang (PWA)**: dibuka dari Chrome, lalu dipasang ke layar utama. Tampil layar penuh dengan ikon sendiri dan tetap jalan tanpa internet.
- **Aplikasi Android (APK)**: dibangun otomatis oleh GitHub dari proyek ini, lalu dipasang seperti aplikasi biasa.

Keduanya gratis dan cukup memakai satu akun GitHub. Proses upload paling mudah dilakukan dari **komputer**.

## Isi folder

| Folder / file | Fungsi |
|---|---|
| `www/` | Aplikasinya (index.html, ikon, manifest, service worker) |
| `assets/` | Ikon & layar pembuka untuk APK |
| `capacitor.config.json`, `package.json` | Pengaturan proyek Android (Capacitor) |
| `.github/workflows/` | Perintah build otomatis: APK dan versi web |

> Folder `.github` tersembunyi di Mac. Tekan **Cmd + Shift + .** di Finder supaya terlihat.

## Langkah 1: Upload ke GitHub

1. Buat akun gratis di github.com, lalu tekan **New repository**.
2. Beri nama `financial-freedom`, pilih **Public**, lalu tekan **Create repository**.
3. Tekan **uploading an existing file**. Ekstrak ZIP ini, lalu seret **semua isi** folder `financial-freedom-app` (termasuk folder `.github`) ke halaman itu.
4. Tekan **Commit changes**.

## Langkah 2: Ambil APK Android

1. Buka tab **Actions** di repository. Build **"Build APK Android"** berjalan otomatis setelah upload, sekitar 5 sampai 10 menit.
2. Setelah ada tanda centang hijau, buka build itu, lalu di bagian **Artifacts** unduh **financial-freedom-apk**.
3. Ekstrak ZIP-nya di HP, lalu buka **financial-freedom.apk**. Kalau diminta, izinkan "Instal aplikasi tidak dikenal" untuk aplikasi File atau Chrome.

APK ini ditandatangani dengan kunci *debug*. Aman untuk dipakai sendiri, tapi belum bisa diunggah ke Play Store.

## Langkah 3 (opsional): Versi web yang bisa dipasang

1. Di repository, buka **Settings → Pages**, lalu ubah **Source** ke **GitHub Actions**.
2. Buka tab **Actions**, pilih **"Terbitkan versi web"**, lalu tekan **Run workflow**.
3. Buka `https://NAMA-AKUN.github.io/financial-freedom/` di Chrome HP, lalu tekan **Pasang** (atau menu ⋮ → **Instal aplikasi**).

## Memperbarui aplikasi

Ganti file `www/index.html` di GitHub (**Add file → Upload files**), lalu commit. APK dan versi web akan dibangun ulang otomatis. Setelah itu, pasang APK baru di atas yang lama. Datanya tetap ada.

## Tentang data

- Data tersimpan **di HP** dan tidak dikirim ke mana pun.
- APK, versi web, dan versi di Claude masing-masing punya data sendiri. Untuk memindahkan data, pakai **Pengaturan → Cadangkan data** di satu versi, lalu **Pulihkan data** di versi lain.
- Cadangkan rutin. Aplikasi akan mengingatkanmu kalau sudah lebih dari 14 hari.

## Scan struk

Di APK dan versi web, struk dibaca langsung di HP (OCR). Saat pertama kali dipakai, HP perlu internet untuk mengunduh pembaca teksnya. Selalu periksa total dan tanggal sebelum menyimpan.
