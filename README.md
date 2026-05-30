# 🚀 RecruitSync Enterprise - ATS Dashboard

![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-Single_File-E34F26?style=flat-square&logo=html5&logoColor=white)
![No Build Step](https://img.shields.io/badge/Build-Zero_Install-success?style=flat-square)

**RecruitSync** adalah purwarupa _Applicant Tracking System_ (ATS) berbasis _Single-Page Application_ (SPA) yang dirancang untuk mensimulasikan alur kerja rekrutmen Enterprise.

> **💡 Keunikan Proyek:** Aplikasi ini dibangun sepenuhnya di dalam **satu file HTML tunggal (`dashboard.html`)** tanpa memerlukan proses _build_ (tanpa Node.js, Webpack, Vite, atau NPM). Sangat portabel dan berjalan langsung di peramban (browser)!

## ✨ Fitur Utama

- 🔐 **Role-Based Access Control (RBAC):** Pemisahan akses UI dan fungsionalitas antara **HR Admin** (Akses penuh ke Pipeline & Pengaturan Lowongan) dan **Interviewer** (Hanya melihat jadwal wawancara & Portal Karir).
- 📋 **Drag & Drop Kanban Pipeline:** Papan manajemen kandidat interaktif menggunakan _HTML5 Drag API_ untuk memindahkan pelamar antar tahap (Applied ➡️ Interview ➡️ Hired).
- 🤖 **AI Job Description Generator:** Simulasi integrasi AI yang secara otomatis menghasilkan deskripsi pekerjaan berdasarkan judul/posisi (Frontend, Backend, UI/UX, dll).
- 🌐 **Public Job Board Simulator:** Halaman karir eksternal tempat pelamar (dummy) dapat mendaftar, di mana datanya akan langsung tersinkronisasi masuk ke dalam pipeline ATS internal.
- 💾 **Offline Data Persistence:** Menggunakan pangkalan data lokal peramban (`LocalStorage`) agar data (Pekerjaan, Kandidat, Jadwal, Aktivitas Log) tidak hilang saat halaman di-_refresh_.
- 📧 **Automation Hub:** Simulasi pengiriman _template_ email otomatis (Undangan Wawancara & _Offering Letter_) kepada kandidat.

## 🛠️ Teknologi yang Digunakan

Proyek ini menggunakan arsitektur _CDN-based_ murni:

- **[React 18 (UMD)](https://react.dev/):** Mengelola rendering UI, _state management_ (`useState`, `useMemo`), dan _lifecycle_.
- **[Babel Standalone](https://babeljs.io/):** Melakukan _transpile_ sintaks JSX & ES6+ langsung di sisi klien (_in-browser compiler_).
- **[Tailwind CSS (CDN)](https://tailwindcss.com/):** _Utility-first framework_ untuk penataan gaya (UI/UX) yang modern, bersih, dan sangat responsif.
- **Browser APIs:** Memanfaatkan murni fitur peramban seperti `LocalStorage` dan `HTML5 Drag and Drop`.

## 📂 Struktur Aplikasi

Keseluruhan sistem berada di dalam file `dashboard.html`, dengan segmentasi komponen React sebagai berikut:

- **`App()`** - Inti aplikasi pembungkus Router & Global State.
- **`LoginPage()`** - Modul autentikasi dan gerbang RBAC (Admin/Interviewer).
- **Fitur Tab Utama:**
  - `DashboardTab()` - Metrik analitik rekrutmen.
  - `JobManagementTab()` - Tabel CRUD lowongan pekerjaan.
  - `PipelineTab()` - Modul interaktif _Drag & Drop_ Kanban.
  - `SchedulerTab()` - Manajemen logistik jadwal wawancara.
  - `CareersBoardTab()` - _Frontend_ publik untuk pendaftaran pelamar.
- **Fitur Overlay (Modal):**
  - `JobFormModal()`, `CandidateDetailModal()`, `ScheduleInterviewModal()`.

## 🚀 Cara Menjalankan

Karena tidak ada sistem _backend_ atau rantai _build_ (build-chain) yang diperlukan, menjalankan aplikasi ini sangat mudah:

1. **Unduh atau _Clone_** repositori ini ke komputer Anda.
2. Buka folder proyek.
3. Klik ganda pada file **`index.html`** (atau seret file tersebut ke Google Chrome / Firefox / Edge / Safari).
4. Aplikasi akan langsung berjalan. Anda dapat masuk dengan kredensial _dummy_ apa saja (formulir sudah terisi otomatis).

## 📸 Tangkapan Layar (Screenshots)

|                          Dashboard HR Admin                          |                             Dashboard Interviewer                              |
| :------------------------------------------------------------------: | :----------------------------------------------------------------------------: |
| <img width="1366" height="607" alt="hradmin" src="https://github.com/user-attachments/assets/d27ba291-0439-4059-8131-3a37e422b81a" /> | <img width="1366" height="607" alt="interviewer" src="https://github.com/user-attachments/assets/2ab7bc17-7262-4f53-87e0-84aa0cddb242" />
 |
