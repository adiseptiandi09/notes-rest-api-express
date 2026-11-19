# Notes REST API — Express.js

Layanan back-end RESTful API berbasis **Node.js** dan **Express** untuk mengelola data catatan (*notes*). Proyek ini mendokumentasikan penerapan fondasi pembangunan layanan API yang terstruktur, tervalidasi, dan siap dijalankan pada lingkungan server.

## Konsep Fundamental yang Dipraktikkan

- **Arsitektur REST API Modular:** Menerapkan pemisahan tanggung jawab (*separation of concerns*) antara konfigurasi server, pemetaan rute endpoint, logika bisnis CRUD, dan penyimpanan data *in-memory*.
- **Operasi CRUD & Pertukaran Data JSON:** Mengelola siklus pembuatan, pembacaan, pembaruan, dan penghapusan data catatan menggunakan metode HTTP standar dengan format respons JSON yang konsisten.
- **Middleware & Konfigurasi Environment:** Mengelola pemrosesan *payload* JSON, kebijakan akses lintas origin (CORS), serta penyesuaian host dan port secara dinamis berdasarkan lingkungan eksekusi.
- **Identifikasi Unik & Kode Status HTTP Semantik:** Menerapkan pembuatan identitas sumber daya secara unik pada setiap catatan baru serta mengembalikan kode status HTTP yang sesuai dengan hasil pemrosesan permintaan.
- **Standarisasi Kualitas Kode:** Menerapkan pemeriksaan konsistensi gaya penulisan kode otomatis menggunakan ESLint.

## Ringkasan Endpoint

| Method | Endpoint | Fungsi |
| :--- | :--- | :--- |
| `POST` | `/notes` | Menambahkan catatan baru |
| `GET` | `/notes` | Menampilkan seluruh daftar catatan |
| `GET` | `/notes/:id` | Menampilkan detail catatan berdasarkan ID |
| `PUT` | `/notes/:id` | Memperbarui data catatan berdasarkan ID |
| `DELETE` | `/notes/:id` | Menghapus catatan berdasarkan ID |