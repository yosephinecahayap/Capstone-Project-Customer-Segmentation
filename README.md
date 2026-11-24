# Customer Segmentation Analysis Using K-Means Clustering

Proyek analisis data e-commerce untuk memahami perilaku pembelian pelanggan, mengidentifikasi pelanggan bernilai tinggi, serta menyusun strategi pemasaran yang lebih tepat sasaran menggunakan RFM Analysis dan K-Means Clustering.

## 1. Gambaran Umum Proyek

Proyek ini merupakan capstone project dari program **Asah led by Dicoding** yang berfokus pada analisis data e-commerce untuk memahami tren penjualan, perilaku pembelian, dan segmentasi pelanggan.

Permasalahan yang diangkat adalah perbedaan kontribusi setiap pelanggan terhadap bisnis, sementara strategi promosi sering kali diberikan secara seragam. Hal tersebut berpotensi menyebabkan penggunaan anggaran pemasaran yang kurang efektif dan hilangnya peluang untuk mempertahankan pelanggan bernilai tinggi.

Melalui proyek ini, dilakukan analisis untuk mengidentifikasi pelanggan berdasarkan aktivitas dan nilai transaksinya, mengetahui pelanggan yang berisiko churn, serta merancang strategi pemasaran yang sesuai dengan karakteristik setiap segmen.

## 2. Tujuan Proyek

- Menganalisis tren penjualan, performa produk, dan perilaku pembelian pelanggan.
- Mengelompokkan pelanggan berdasarkan aktivitas dan nilai transaksinya.
- Mengidentifikasi pelanggan bernilai tinggi dan pelanggan yang berisiko churn.
- Membandingkan Customer Lifetime Value (CLV) pada setiap segmen pelanggan.
- Menyusun rekomendasi strategi pemasaran berdasarkan karakteristik setiap segmen.

## 3. Dataset

Dataset yang digunakan merupakan dataset e-commerce dengan total **10.000 baris dan 20 fitur**.

Dataset mencakup beberapa informasi berikut:

- **Informasi Pelanggan:** Gender, kelompok usia, negara, dan tanggal pendaftaran.
- **Informasi Produk:** Nama produk dan kategori produk.
- **Informasi Transaksi:** Jumlah pembelian, harga, tanggal transaksi, status pesanan, dan metode pembayaran.
- **Ulasan Pelanggan:** Rating dan ulasan terhadap produk.

## 4. Tools dan Teknologi

| Tools | Penggunaan |
|---|---|
| Python | Pengolahan dan analisis data |
| Pandas | Manipulasi dan pembersihan data |
| NumPy | Pengolahan data numerik |
| Matplotlib & Seaborn | Visualisasi dan eksplorasi data |
| Scikit-learn | Penerapan K-Means Clustering |
| Tableau | Pembuatan dashboard interaktif |

## 5. Tahapan Analisis

### 5.1 Data Cleaning dan Preprocessing

Melakukan pemeriksaan struktur dan kualitas data, menangani missing values dan duplikasi, serta mempersiapkan data agar dapat digunakan untuk proses analisis.

### 5.2 Exploratory Data Analysis (EDA)

Melakukan eksplorasi data untuk memahami karakteristik bisnis melalui:

- Analisis tren penjualan.
- Analisis performa produk dan kategori.
- Analisis pola pembelian pelanggan.
- Analisis distribusi transaksi dan metode pembayaran.

### 5.3 RFM Analysis

Menerapkan analisis RFM untuk memahami perilaku pembelian pelanggan berdasarkan tiga metrik utama:

- **Recency:** Jumlah hari sejak transaksi terakhir pelanggan.
- **Frequency:** Jumlah transaksi yang dilakukan pelanggan.
- **Monetary:** Total nilai transaksi pelanggan.

Ketiga metrik tersebut digunakan sebagai dasar dalam proses segmentasi pelanggan.

### 5.4 K-Means Clustering

Menggunakan algoritma K-Means Clustering untuk mengelompokkan pelanggan berdasarkan karakteristik RFM. Hasil clustering kemudian dianalisis untuk mengetahui perbedaan perilaku pembelian dan kontribusi nilai setiap kelompok pelanggan.

### 5.5 Customer Lifetime Value (CLV) Analysis

Menganalisis dan membandingkan rata-rata Customer Lifetime Value (CLV) pada setiap segmen untuk mengidentifikasi kelompok pelanggan dengan kontribusi nilai tertinggi.

### 5.6 Dashboard Development

Membangun dashboard interaktif menggunakan Tableau untuk menyajikan KPI utama, distribusi pelanggan, karakteristik setiap cluster, serta perbandingan nilai RFM dan CLV.

## 6. Hasil Segmentasi Pelanggan

Hasil K-Means Clustering menghasilkan empat segmen pelanggan dengan total **4.327 pelanggan**.

| Cluster | Segmen | Jumlah Pelanggan | Recency (Hari) | Frequency | Monetary | Rata-rata CLV |
|---|---|---:|---:|---:|---:|---:|
| 0 | Mid Loyal | 1.145 | 216,55 | 3,63 | 1.730,66 | 150,39 |
| 1 | Dormant | 1.143 | 774,37 | 1,42 | 894,57 | 1,94 |
| 2 | New / Low Frequency | 1.439 | 240,54 | 1,59 | 859,83 | 24,41 |
| 3 | VIP | 600 | 269,80 | 3,21 | 5.348,94 | 359,22 |

### Karakteristik Setiap Segmen

- **Cluster 0 – Mid Loyal:** Memiliki frekuensi pembelian tertinggi sebesar 3,63 dan Monetary sebesar 1.730,66. Segmen ini menunjukkan aktivitas pembelian yang relatif konsisten dengan rata-rata CLV sebesar 150,39.

- **Cluster 1 – Dormant:** Memiliki Recency tertinggi sebesar 774,37 hari, frekuensi pembelian 1,42, dan CLV terendah sebesar 1,94. Segmen ini menunjukkan risiko churn yang paling tinggi.

- **Cluster 2 – New / Low Frequency:** Merupakan segmen terbesar dengan 1.439 pelanggan. Memiliki Recency sebesar 240,54 hari, tetapi frekuensi pembelian masih rendah sebesar 1,59 dan CLV sebesar 24,41.

- **Cluster 3 – VIP:** Memiliki Monetary tertinggi sebesar 5.348,94 dan CLV tertinggi sebesar 359,22. Meskipun jumlah pelanggannya hanya 600, segmen ini memberikan kontribusi nilai pelanggan yang signifikan.

## 7. Insight Bisnis

Berdasarkan hasil analisis dan segmentasi, diperoleh beberapa insight utama:

1. **Konsentrasi Nilai Pelanggan:** Segmen VIP yang mencakup sekitar 14% pelanggan berkontribusi sekitar 50,71% dari total CLV. Hal ini menunjukkan bahwa sebagian besar nilai pelanggan terkonsentrasi pada segmen yang relatif kecil.

2. **Prioritas Retensi Pelanggan:** Segmen VIP dan Mid Loyal secara keseluruhan mencakup sekitar 40% pelanggan dan menyumbang sekitar 91,22% total CLV. Oleh karena itu, mempertahankan kedua segmen ini menjadi prioritas bisnis.

3. **Risiko Churn:** Segmen Dormant memiliki rata-rata Recency sebesar 774,37 hari dan CLV sebesar 1,94, yang menunjukkan penurunan aktivitas transaksi dan tingginya risiko churn.

4. **Peluang Konversi:** Segmen New / Low Frequency masih memiliki aktivitas pembelian yang relatif baru sehingga berpotensi dikembangkan menjadi pelanggan dengan frekuensi transaksi lebih tinggi.

## 8. Rekomendasi Strategi Pemasaran

Berdasarkan karakteristik setiap segmen, berikut rekomendasi strategi pemasaran yang dapat diterapkan:

| Segmen | Rekomendasi Strategi |
|---|---|
| Mid Loyal | Meningkatkan frekuensi dan nilai transaksi melalui upselling, bundling produk, dan program poin loyalitas. |
| Dormant | Melakukan kampanye win-back melalui penawaran personal, email reaktivasi, dan voucher diskon khusus. |
| New / Low Frequency | Mendorong pembelian kedua melalui onboarding, edukasi produk, dan diskon untuk transaksi berikutnya. |
| VIP | Mempertahankan loyalitas melalui program premium, akses awal produk, dan layanan pelanggan prioritas. |

## 9. Dashboard Tableau

Hasil analisis disajikan melalui dashboard interaktif menggunakan Tableau yang menampilkan:

**Key Performance Indicators (KPI):**

- Total Pelanggan: 4.327
- Jumlah Segmen: 4
- Rata-rata CLV: 98,24
- Churn Rate: 67,74%

**Visualisasi Dashboard:**

- Distribusi pelanggan berdasarkan segmen.
- Scatter plot Recency vs. Monetary.
- Perbandingan rata-rata metrik RFM pada setiap cluster.
- Perbandingan CLV antarsegmen.
- Ringkasan karakteristik dan insight setiap segmen.

### Dashboard Preview

<!-- Tambahkan screenshot dashboard di sini -->

<!-- Contoh: ![Customer Segmentation Dashboard](images/dashboard-overview.png) -->

**File Dashboard:** `Customer Segmentation Dashboard.twbx`

## 10. Struktur Repository

| File | Deskripsi |
|---|---|
| `Customer Segmentation Clustering.ipynb` | Notebook Python berisi proses pengolahan data, eksplorasi, analisis RFM, dan clustering. |
| `Customer Segmentation Dashboard.twbx` | File dashboard interaktif Tableau. |
| `ecommerce_dataset_10000.csv` | Dataset yang digunakan dalam proyek. |

## 11. Cara Menjalankan Proyek

1. Clone repository:

   ```bash
   git clone https://github.com/yosephinecahayap/Capstone-Project-Customer-Segmentation.git
   ```

2. Masuk ke direktori proyek.

3. Install library Python yang dibutuhkan:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```

4. Buka file `Customer Segmentation Clustering.ipynb` menggunakan Jupyter Notebook atau Google Colab.

5. Jalankan setiap cell secara berurutan untuk melihat proses pengolahan dan analisis data.

6. Buka file `Customer Segmentation Dashboard.twbx` menggunakan Tableau Desktop untuk melihat dashboard interaktif.

## 12. Informasi Proyek

- **Program:** Asah led by Dicoding
- **Jenis Proyek:** Capstone Project
- **Fokus:** E-Commerce Data Analysis & Customer Segmentation
- **Metode:** Exploratory Data Analysis, RFM Analysis, K-Means Clustering, dan CLV Analysis
- **Tools:** Python dan Tableau
