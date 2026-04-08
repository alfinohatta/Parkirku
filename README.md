# ParkRight - Manual Parking Management System

ParkRight adalah aplikasi manajemen parkir modern berbasis web yang dirancang untuk mengelola operasional parkir secara manual namun terstruktur. Sistem ini memfasilitasi pencatatan kendaraan masuk dan keluar, perhitungan tarif otomatis, manajemen langganan, hingga pelaporan keuangan yang mendalam bagi pemilik fasilitas.

## 📌 Kategori Proyek
**Manajemen Operasional / Enterprise Resource Planning (ERP) Sederhana**

## 🚀 Fitur Utama
- **Multi-Role Access Control**: Dashboard khusus untuk Admin, Petugas (Attendant), dan Owner.
- **Manajemen Transaksi**: Input plat nomor manual dengan perhitungan biaya otomatis berdasarkan durasi dan jenis kendaraan.
- **Tarif Dinamis**: Pengaturan tarif jam pertama, jam berikutnya, dan batas maksimum harian oleh Admin.
- **Sistem Langganan (Subscription)**: Pelacakan kendaraan member dengan pemotongan biaya otomatis jika masa aktif masih berlaku.
- **Dashboard Analitik**: Visualisasi pendapatan, komposisi kendaraan, dan jam sibuk menggunakan grafik interaktif.
- **AI-Powered Insights**: Asisten AI (Genkit) untuk membantu memberikan ringkasan operasional harian dan analisis data keuangan.
- **Audit Log**: Pencatatan setiap aktivitas penting yang dilakukan oleh semua pengguna sistem.

## 🛠️ Teknologi & Tools
- **Framework**: [Next.js 15](https://nextjs.org/) (App Router)
- **Bahasa**: [TypeScript](https://www.typescriptlang.org/)
- **UI/UX**: [Tailwind CSS](https://tailwindcss.com/) & [ShadCN UI](https://ui.shadcn.com/)
- **State Management**: Custom Persistent State (LocalStorage)
- **Charts**: [Recharts](https://recharts.org/)
- **AI Integration**: [Genkit](https://firebase.google.com/docs/genkit) dengan model Google Gemini
- **Icons**: [Lucide React](https://lucide.dev/)
- **Validasi**: [Zod](https://zod.dev/) & [React Hook Form](https://react-hook-form.com/)

## 📂 Struktur Proyek
```text
src/
├── ai/                 # Konfigurasi Genkit dan AI Flows (Insights & Assistant)
├── app/                # Next.js App Router (Halaman & Layout)
│   ├── login/          # Halaman autentikasi
│   └── page.tsx        # Entry point (Dashboard Router)
├── components/         # Komponen React reusable
│   ├── dashboard/      # UI spesifik untuk Admin, Petugas, dan Owner
│   ├── layout/         # Header, Footer, dan Navigasi
│   └── ui/             # Komponen dasar ShadCN (Button, Card, Input, dll.)
├── hooks/              # Custom React Hooks (Persistent State, Real-time Clock, dll.)
├── lib/                # Utilitas, tipe data (Typescript), dan mock data
└── firebase/           # (Opsional) Konfigurasi Firebase Client SDK
```

## 💻 Pengembangan Lokal

### Prasyarat
- [Node.js](https://nodejs.org/) (Versi 20.x atau lebih baru)
- npm (biasanya terinstal bersama Node.js)

### Langkah-langkah Instalasi
1. **Clone repositori**:
   ```bash
   git clone <repository-url>
   cd parkright
   ```

2. **Instal dependensi**:
   ```bash
   npm install
   ```

3. **Konfigurasi Environment**:
   Buat file `.env` di root folder dan tambahkan kunci API jika diperlukan (misal untuk Genkit/Gemini):
   ```env
   GOOGLE_GENAI_API_KEY=your_api_key_here
   ```

### Menjalankan Aplikasi
- **Mode Pengembangan**:
  ```bash
  npm run dev
  ```
  Aplikasi akan berjalan di [http://localhost:9002](http://localhost:9002).

- **Menjalankan Genkit UI** (untuk debug AI):
  ```bash
  npm run genkit:dev
  ```

- **Build untuk Produksi**:
  ```bash
  npm run build
  npm start
  ```

## 🔑 Kredensial Default
Untuk keperluan pengujian, gunakan akun berikut:
- **Admin**: `admin` / `password123`
- **Petugas**: `petugas1` / `password123`
- **Owner**: `owner` / `password123`

Detail lengkap dapat dilihat di file `credential.md`.

---
© 2024 ParkRight - Solusi Parkir Cerdas & Transparan.
