Project Membersihkan Data Sales (SQL)
Di sini saya mendokumentasikan proses cleaning dan transformasi data penjualan yang awalnya masih berantakan. Saya menggunakan SQLite untuk seluruh prosesnya.

Hal-hal yang dikerjakan:
Pembersihan Teks: Menggunakan fungsi TRIM untuk menghapus spasi yang tidak diinginkan pada kolom nama dan email. Kategori barang juga diseragamkan menjadi huruf kapital menggunakan fungsi UPPER agar hasil perhitungan lebih akurat.

Penggabungan Tabel (JOIN): Menghubungkan tabel transaksi dengan tabel pelanggan, produk, dan wilayah supaya informasi yang ditampilkan lebih lengkap dan mudah dibaca.

Kontrol Kualitas Data: Membuat query untuk mendeteksi data duplikat dan mencari kolom yang masih memiliki nilai kosong (NULL). Hal ini penting untuk menjaga integritas data sebelum masuk ke tahap analisis.

Pembuatan View: Membuat VIEW clean_sales sebagai tabel virtual hasil akhir yang sudah bersih, sehingga jika ingin menarik data untuk laporan tidak perlu lagi menulis query yang panjang.

Daftar File:
data_cleaning_and_transformation.sql: Berisi semua kode SQL yang digunakan dalam proyek ini.
chinook.db: File database untuk mencoba menjalankan script secara langsung.
clean_sales.csv: Hasil data bersih yang sudah diolah
