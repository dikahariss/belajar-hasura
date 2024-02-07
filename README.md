# Belajar Hasura

Proyek ini mengatur instansi Hasura GraphQL Engine dengan Docker Compose, menggunakan PostgreSQL sebagai basis data. Hasura adalah engine GraphQL yang memberikan API GraphQL instan untuk database PostgreSQL Anda. Proyek ini juga termasuk Data Connector Agent untuk integrasi dengan berbagai sumber data eksternal.

## Prasyarat

Pastikan Anda sudah menginstal Docker dan Docker Compose di sistem Anda.

## Pengaturan

### Klon Repositori

Klon repositori ini dan masuk ke direktori:

```
git clone https://github.com/dikahariss/belajar-hasura.git
cd belajar-hasura
```

### Konfigurasi Variabel Lingkungan

Sebelum memulai, pastikan untuk mengubah nilai default untuk **POSTGRES_PASSWORD** dan **HASURA_GRAPHQL_ADMIN_SECRET** di file `docker-compose.yml` untuk meningkatkan keamanan.

### Mulai Layanan

Untuk menjalankan layanan, gunakan perintah berikut:

```
docker-compose up -d --build
```

### Akses Hasura Console

Setelah layanan berjalan, Hasura Console dapat diakses melalui:

```
http://localhost:8080
```

Anda akan diminta memasukkan `HASURA_GRAPHQL_ADMIN_SECRET` yang telah Anda set sebelumnya untuk mengakses konsol.

### Menghentikan Layanan

Untuk menghentikan dan membersihkan semua layanan, gunakan perintah:

```
docker-compose down
```

## Informasi Tambahan

- **Database**: Layanan PostgreSQL disiapkan sebagai database untuk menyimpan data Anda dan metadata Hasura.
- **Data Connector Agent**: Digunakan untuk menghubungkan Hasura dengan berbagai sumber data eksternal seperti Athena, MariaDB, MySQL8, Oracle, dan Snowflake.
- **Catatan Keamanan**: Pastikan untuk selalu menggunakan `HASURA_GRAPHQL_ADMIN_SECRET` yang kuat dan unik. Jangan gunakan konfigurasi ini seperti apa adanya untuk produksi tanpa melakukan penyesuaian keamanan lebih lanjut.
