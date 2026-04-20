# Project Setup: Bun + ElysiaJS + Drizzle + MySQL

## Tujuan
Menginisialisasi project backend baru menggunakan stack Bun di direktori saat ini.

## Kebutuhan / Dependency Utama
- **Runtime:** Bun
- **Framework:** ElysiaJS
- **ORM:** Drizzle ORM
- **Database:** MySQL

## Langkah-langkah Implementasi (High-Level)

1. **Inisialisasi Project**
   - Lakukan inisialisasi project Bun kosong di folder ini.
   - Pastikan `package.json` dan file konfigurasi dasar TypeScript/Bun telah terbuat.

2. **Instalasi Dependency**
   - Install ElysiaJS sebagai web framework.
   - Install Drizzle ORM dan driver MySQL yang kompatibel dengan Bun.

3. **Setup Database (Drizzle & MySQL)**
   - Buat konfigurasi koneksi database MySQL (gunakan environment variables untuk kredensial).
   - Definisikan schema database sederhana menggunakan Drizzle (contoh: tabel `users` dasar).
   - Siapkan script di `package.json` untuk melakukan *generate* dan *push* migrasi database.

4. **Setup Server (ElysiaJS)**
   - Buat file entry point (misalnya `src/index.ts`).
   - Inisialisasi server ElysiaJS.
   - Buat sebuah endpoint sederhana (contoh: `GET /`) untuk melakukan pengecekan kesehatan (*health check*) bahwa server menyala.

5. **Integrasi**
   - Integrasikan koneksi Drizzle ke dalam endpoint ElysiaJS (contoh: buat endpoint `GET /users` yang mengambil data dari database menggunakan Drizzle) untuk membuktikan semua dependency terhubung dengan baik.

## Kriteria Penerimaan (Acceptance Criteria)
- Project dapat dijalankan (misalnya dengan `bun run dev`).
- Server merespon permintaan pada endpoint yang dibuat.
- Koneksi ke database MySQL berhasil dan query Drizzle berjalan tanpa error.
- Struktur folder cukup rapi dan terpisah secara mendasar (contoh: pisahkan file konfigurasi database/schema dengan file server).

**Catatan:** Fokus pada *proof of concept* bahwa semua teknologi di atas terintegrasi dan berjalan. Detail implementasi *low-level* (seperti validasi *schema* kompleks atau penanganan *error* yang sangat spesifik) tidak diperlukan pada tahap ini.
