# Analisis Harga Rumah Berdasarkan Fasilitas dengan Metode Klasifikasi Fuzzy Naive Bayes
Proyek ini mengklasifikasikan rumah ke dalam tiga kategori harga menggunakan algoritma Fuzzy Naive Bayes. Fitur numerik diubah menjadi derajat keanggotaan fuzzy sebelum dihitung probabilitasnya. Fitur kategorik dihitung menggunakan pendekatan Naive Bayes standar.
 
## Dataset
Dataset yang digunakan adalah <a href="https://www.kaggle.com/datasets/yasserh/housing-prices-dataset">Housing Prices Dataset</a> dari Kaggle. Dataset ini berisi 545 baris data rumah dengan 13 kolom. Tidak ada nilai kosong pada seluruh kolom.
Fitur yang digunakan terbagi dua jenis. Fitur kontinu meliputi area, jumlah kamar tidur, jumlah kamar mandi, jumlah lantai, dan jumlah parkir. Fitur kategorik meliputi akses jalan utama, ruang tamu, basement, pemanas air, pendingin ruangan, area preferensi, dan status furnitur.
Target klasifikasi dibentuk dari kolom harga. Harga dibagi menjadi tiga kategori menggunakan metode quantile, yaitu Rendah, Sedang, dan Tinggi. Pembagian ini menghasilkan jumlah data yang cukup seimbang antar kelas, yaitu 186 data Rendah, 177 data Sedang, dan 182 data Tinggi.
 
## Eksplorasi Data
Pengecekan outlier dilakukan menggunakan metode IQR pada setiap fitur numerik. Hasilnya menunjukkan persentase outlier yang rendah pada sebagian besar fitur. Fitur stories memiliki persentase outlier tertinggi, yaitu 7.52 persen dari total data.
Heatmap korelasi antar fitur digunakan untuk melihat hubungan antar variabel setelah proses encoding. Fitur kategorik diubah menjadi angka menggunakan Label Encoder sebelum dihitung korelasinya.
 
## Hasil
| Kelas | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| Rendah | 0.80 | 0.76 | 0.78 | 37 |
| Sedang | 0.64 | 0.64 | 0.64 | 36 |
| Tinggi | 0.79 | 0.83 | 0.81 | 36 |
| **Akurasi** | | | **0.74** | 109 |
| Macro Avg. | 0.74 | 0.74 | 0.74 | 109 |
| Weighted Avg. | 0.74 | 0.74 | 0.74 | 109 |
