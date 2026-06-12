# Analisis-Distribusi-dan-Risiko-Portofolio-Pinjaman-IBRD-Menggunakan-Data-Warehouse-dan-OLAP
Repository ini berisi kode program untuk analisis distribusi dan risiko portofolio pinjaman IBRD (International Bank for Reconstruction and Development) menggunakan arsitektur Data Warehouse dan OLAP. Proyek ini mencakup pipeline ETL end-to-end mulai dari akuisisi data periodik, transformasi, hingga analisis multidimensi berbasis star schema.

**Tujuan**
1. Merancang dan mengimplementasikan arsitektur Data Warehouse berbasis star schema pada dataset pinjaman IBRD
2. Membangun pipeline ETL asinkronus dengan simulasi akuisisi data periodik per kuartal
3. Mengoptimalkan performa query analitik menggunakan Materialized View, Index, dan partisi tabel PostgreSQL
4. Menganalisis distribusi geografis, tren temporal, dan profil risiko portofolio pinjaman IBRD secara multidimensi

**Metodologi**
1. Ekstraksi dataset IBRD Historical Data (1.537.969 baris, 33 kolom) dari World Bank Finance Portal
2. Simulasi akuisisi data periodik per kuartal menggunakan APScheduler
3. Transformasi data: pembersihan, normalisasi, deteksi anomali, dan pembentukan fitur turunan (disbursement ratio, risk ratio, risk category)
4. Pemuatan ke PostgreSQL cloud (Supabase) dengan desain star schema dan partisi tabel
5. Optimasi OLAP dengan 5 Materialized View, 7 index, dan 3 ekstensi PostgreSQL
6. Pembangunan DataMart dan OLAP Cube menggunakan Atoti untuk operasi drill-down, roll-up, slice, dan dice
7. Visualisasi interaktif distribusi regional, tren temporal, dan profil risiko menggunakan Plotly

**Teknologi yang Digunakan**
1.  Python
2.  PostgreSQL (Supabase)
3.  Atoti (ActiveViam)
4.  asyncio & aiofiles
5.  APScheduler
6.  Plotly
7.  Pandas

**Hasil**
1. Amerika Latin & Karibia mencatat komitmen tertinggi; India merupakan negara penerima pinjaman terbesar
2. Lonjakan komitmen pada 2008–2009 dan 2020 berkorelasi dengan krisis keuangan global dan pandemi COVID-19
3. Mayoritas portofolio berada pada kategori Low Risk
4. Materialized View terbukti memberikan akselerasi query tertinggi dibandingkan Index Scan maupun Sequential Scan

Kegunaan
Proyek ini dapat digunakan sebagai referensi implementasi Data Warehouse end-to-end, pembelajaran konsep ETL dan OLAP, serta dikembangkan lebih lanjut untuk sistem monitoring risiko portofolio pinjaman berbasis data historis.
