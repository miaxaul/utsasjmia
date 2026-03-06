# UTS ASJ - Member Management System
Sistem manajemen data pengguna berbasis microservices yang mengintegrasikan PostgreSQL dan MinIO dalam ekosistem kontainer Docker Compose.

---

## Langkah Menjalankan Project

### 1. Membuat Direktori Kerja

Buat direktori project dan masuk ke dalamnya.

```bash
mkdir utsmia
cd utsmia
```

---

### 2. Membuat File `docker-compose.yaml`

Buat file `docker-compose.yaml`, lalu salin isi dari source code yang telah disediakan.

```bash
nano docker-compose.yaml
```

---

### 3. Membuat File Environment

Buat file `.env`, kemudian salin isi dari file `env.txt`.

```bash
nano .env
```

---

### 4. Membuat Direktori Backend dan Frontend

Buat dua direktori untuk memisahkan layanan backend dan frontend.

```bash
mkdir backend
mkdir frontend
```

---

### 5. Menyiapkan Backend

Masuk ke direktori `backend`.

```bash
cd backend
```

Buat file–file yang dibutuhkan untuk backend.

```bash
nano Dockerfile
nano main.py
nano requirements.txt
```

Kemudian salin isi file sesuai dengan source code yang diberikan.

---

### 6. Menyiapkan Frontend

Kembali ke direktori utama project (`utsmia`) lalu masuk ke direktori (`frontend`).

```bash
cd ..
cd frontend
```

Buat file `index.html`.

```bash
nano index.html
```

Salin isi file frontend, lalu ubah bagian berikut:

```javascript
const API_URL = "http://IP_ADDRESS:8080";
```

Ganti `IP_ADDRESS` dengan IP terbaru dari interface `enp0s3`.
IP dapat dilihat dengan perintah:

```bash
ip -c a
```

---

### 7. Menjalankan Docker Compose

Pastikan berada di direktori `utsmia`, lalu jalankan:

```bash
docker compose up --build -d
```

---

### 8. Mengecek Container

Pastikan semua container berjalan dengan:

```bash
docker ps
```

Status container seharusnya **Up**.

---

### Troubleshooting

Jika terjadi error, cek log container dengan:

```bash
docker logs <nama_container>
```

Dari log tersebut biasanya bisa diketahui sumber masalahnya.

---


