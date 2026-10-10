# FAHGIT (File Access & GitHub Integration Tool)

> **Author / Creator:** Faiz_Fahmi_ID  
> **Repository:** [GitHub Releases Page](https://github.com/Faiz-Fahmi-ID/FAHGIT/releases)

---

## 📌 Tentang Proyek
**FAHGIT** (*File Access & GitHub Integration Tool*) adalah aplikasi manajemen file dan repositori GitHub revolusioner yang dirancang khusus dengan pendekatan *mobile-first*. Aplikasi ini memungkinkan pengguna Android dan pengembang web untuk mengelola file lokal secara langsung, mengedit kode dengan editor pintar, serta melakukan sinkronisasi penuh (*commit, push, pull*) ke GitHub langsung dari perangkat seluler tanpa hambatan.

---

## 🛑 Masalah yang Diselesaikan
Mengelola repositori GitHub secara langsung dari perangkat seluler sering kali menemui berbagai kendala teknis dan ergonomis:
1. **Antarmuka Web Sempit & Tidak Responsif:** Antarmuka web standar GitHub di browser seluler sangat tidak ramah untuk pengeditan file teks, *debugging* kode, atau navigasi folder yang mendalam.
2. **Ketiadaan Workspace Lokal Mandiri:** Kesulitan dalam mengunduh, memodifikasi, dan menyimpan file repositori secara lokal di dalam memori internal perangkat sebelum dikirim kembali ke remote server.
3. **Alur Kerja Commit yang Rumit:** Proses *staging*, penulisan pesan *commit*, dan pengelolaan branch yang kurang praktis jika harus dilakukan melalui antarmuka browser seluler biasa.

---

## 💡 Solusi yang Ditawarkan
FAHGIT hadir untuk menyelesaikan masalah di atas dengan menyediakan solusi terpadu:
* **Manajemen Repository Mudah:** Cukup masukkan URL repositori publik atau privat dan lakukan autentikasi menggunakan *Personal Access Token* (PAT).
* **Workspace Lokal Terisolasi:** Menggunakan penyimpanan lokal berbasis *IndexedDB* dan penyimpanan aman perangkat untuk mengelola file secara *offline* sebelum disinkronkan.
* **Editor Kode Bawaan Lengkap:** Mendukung berbagai format file teks dan pemrograman (TXT, JSON, MD, HTML, CSS, JS, Python, Kotlin, Gradle, YAML, dll.) lengkap dengan pelacakan perubahan (*diff*).
* **Kontrol Commit & Sync yang Aman:** Antarmuka langsung untuk membuat pesan *commit*, memilih *branch* tujuan, mendeteksi konflik secara dini, dan mengunggah perubahan dengan aman.

---

## ✨ Fitur Utama
1. **GitHub Connection:** Autentikasi aman via Personal Access Token (PAT) dengan fitur uji koneksi, indikator akun aktif, dan manajemen sesi terenkripsi.
2. **Repository Manager:** Penambahan repo via URL, validasi otomatis pemilik dan nama repo, dukungan *branch selector*, serta manajemen daftar repo lokal tanpa menghapus data remote.
3. **Local File Manager:** Pengunduhan file/repo penuh, pembuatan folder/file baru, *rename*, *copy*, *move*, *delete*, pencarian file instan, serta ekspor ke folder bersama Android.
4. **Built-in Editor:** Editor teks responsif dengan indikator file belum disimpan (*unsaved changes*) dan pembanding versi lokal vs remote.
5. **Commit & Upload Engine:** Alur *commit* langsung ke *remote branch* pilihan dengan deteksi konflik dasar guna mencegah penimpaan data secara diam-diam.
6. **Auto Sync & Storage Configuration:** Pengaturan ruang cache, pembersihan file sementara, antrean pekerjaan (*job queue*), serta perlindungan terhadap token agar tidak terekspos di log aplikasi.

---

## 🛠️ Tech Stack
* **Frontend:** React, TypeScript, Tailwind CSS / Modul UI responsif.
* **Penyimpanan Lokal:** IndexedDB & HTML5 LocalStorage untuk pengelolaan workspace perangkat seluler.
* **Integrasi API:** GitHub REST API v3.
* **Mobile Framework:** Capacitor (untuk membungkus aplikasi web menjadi APK Android natif).

---

## 📥 Download & Instalasi APK (Resmi)
Bagi Anda yang ingin langsung memasang aplikasi FAHGIT di perangkat Android tanpa harus membangun dari source code, Anda dapat mengunduh file instalasi siap pakai melalui halaman rilis resmi:

* **Link Download APK:** [GitHub Releases - FAHGIT by Faiz_Fahmi_ID](https://github.com/Faiz-Fahmi-ID/FAHGIT/releases)
* **Kreator:** `Faiz_Fahmi_ID`

### Langkah Pemasangan:
1. Kunjungi tautan halaman rilis GitHub di atas dari browser perangkat Android Anda.
2. Unduh file `app-release.apk` dari rilis terbaru.
3. Berikan izin instalasi dari sumber tidak dikenal pada pengaturan ponsel Anda jika diminta.
4. Buka file APK yang telah diunduh dan ketuk **Install**.
5. Buka aplikasi FAHGIT dan mulai hubungkan akun GitHub Anda menggunakan Personal Access Token (PAT).

---

## 🚀 Panduan Menjalankan di Google AI Studio
1. Buka lingkungan Google AI Studio.
2. Muat *prompt* pengembangan FAHGIT untuk menghasilkan kode sumber lengkap (*React + TypeScript*).
3. Jalankan aplikasi pada pratinjau web bawaan AI Studio untuk menguji antarmuka, navigasi, dan fungsionalitas manajemen file lokal secara interaktif.

---

## 📱 Panduan Build APK Mandiri (Menggunakan Capacitor)
Jika Anda ingin melakukan *build* file APK sendiri dari kode sumber:

1. **Inisialisasi Proyek Lokal:**
   ```bash
   npm install
   npm run build
   ```
2. **Tambahkan Capacitor ke Proyek:**
   ```bash
   npm install @capacitor/core @capacitor/cli
   npx cap init FAHGIT com.faizfahmi.fahgit
   ```
3. **Tambahkan Platform Android:**
   ```bash
   npm install @capacitor/android
   npx cap add android
   ```
4. **Sinkronkan File Web ke Android:**
   ```bash
   npx cap sync
   ```
5. **Buka Android Studio untuk Build APK:**
   ```bash
   npx cap open android
   ```
   * Di Android Studio, pilih menu **Build > Build Bundle(s) / APK(s) > Build APK(s)** untuk menghasilkan file instalasi APK.

---

## 🔒 Keamanan & Batasan
* **Keamanan Token:** Personal Access Token (PAT) disimpan di memori terenkripsi perangkat lokal. Jangan pernah membagikan token Anda atau menanamnya secara *hardcode* ke dalam repositori publik.
* **Batasan Storage Web:** Penyimpanan berbasis browser/IndexedDB memiliki kuota tertentu tergantung pada kapasitas sistem operasi perangkat seluler Anda.
* **Konflik Sinkronisasi:** Jika terjadi perubahan secara bersamaan pada remote repository, lakukan *pull* atau resolusi konflik secara manual sebelum melakukan *push* ulang.

---
*Developed with dedication by **Faiz_Fahmi_ID**.*