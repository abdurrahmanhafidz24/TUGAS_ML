# MACHINE LEARNING
## Prediksi Total Penjualan pada Dataset Retail Sales

## 1. Deskripsi Proyek
Proyek ini membahas penerapan Machine Learning untuk memprediksi total nilai transaksi penjualan berdasarkan dataset Retail Sales. Proses analisis dilakukan mulai dari memahami data, melakukan preprocessing, membangun model regresi, hingga mengevaluasi hasil prediksi.

Tujuan proyek ini adalah membandingkan performa beberapa algoritma regresi untuk mengetahui algoritma yang memberikan hasil prediksi terbaik berdasarkan data pengujian.

## 2. Dataset
Dataset yang digunakan adalah `sales.csv`, yang berisi data transaksi penjualan dengan 1.000 baris dan 9 kolom.

Kolom dalam dataset meliputi:
- `Transaction ID`: Identitas transaksi.
- `Date`: Tanggal transaksi.
- `Customer ID`: Identitas pelanggan.
- `Gender`: Jenis kelamin pelanggan.
- `Age`: Usia pelanggan.
- `Product Category`: Kategori produk.
- `Quantity`: Jumlah barang yang dibeli.
- `Price per Unit`: Harga setiap unit barang.
- `Total Amount`: Total nilai transaksi.

Variabel target yang digunakan adalah `Total Amount`, sedangkan fitur prediksi berasal dari informasi transaksi dan karakteristik pelanggan yang relevan.

## 3. Metode
Proyek ini menggunakan metode **Supervised Learning** dengan pendekatan **Regression**. Metode ini dipilih karena tujuan analisis adalah memperkirakan nilai numerik berupa total transaksi penjualan.

Algoritma yang dibandingkan:
1. **Linear Regression** : memodelkan hubungan linear antara fitur dan target.
2. **LARS (Least Angle Regression)** : metode regresi yang membangun model melalui proses pemilihan fitur secara bertahap.
3. **Gradient Boosting Regressor** : membangun model secara bertahap dengan menggabungkan sejumlah model prediksi untuk memperbaiki kesalahan sebelumnya.

Dataset dibagi menjadi 80% data training dan 20% data testing untuk pelatihan dan evaluasi model.

## 4. Tools dan Library
Tools yang digunakan:
- Python
- Jupyter Notebook
- Visual Studio Code (opsional)
- Git dan GitHub (untuk pengelolaan kode dan dokumentasi)

Library Python:
- **Pandas** : membaca dan mengolah dataset.
- **NumPy** : melakukan perhitungan numerik.
- **Matplotlib** : membuat visualisasi data.
- **Seaborn** : membuat grafik statistik.
- **Scikit-learn** : preprocessing, pelatihan model, pembagian dataset, dan evaluasi.

## 5. Instalasi
Pastikan Python dan Jupyter Notebook sudah tersedia. Library yang diperlukan dapat dipasang melalui terminal atau sel notebook menggunakan perintah berikut:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

Setelah instalasi selesai, pastikan dataset `sales.csv` dan notebook `data_sales.ipynb` berada di folder yang sama.

## 6. Cara Menjalankan
1. Buka terminal atau Command Prompt.
2. Masuk ke folder proyek.
3. Jalankan Jupyter Notebook dengan perintah:

   ```bash
   jupyter notebook
   ```

4. Buka file `ML_Retail_Sales.ipynb`.
5. Pastikan file `sales.csv` berada di lokasi yang sesuai dengan kode pembacaan dataset.
6. Jalankan setiap sel notebook secara berurutan dari atas ke bawah.
7. Periksa hasil visualisasi, evaluasi, dan kesimpulan setelah seluruh proses selesai.

## 7. Tahapan Analisis
Tahapan analisis dalam proyek ini meliputi:

1. **Import Library** : memanggil library yang dibutuhkan.
2. **Membaca Dataset** : memuat file CSV ke dalam DataFrame.
3. **Memahami Data** : memeriksa struktur, tipe data, dan statistik deskriptif.
4. **Data Cleaning** : memeriksa nilai kosong, data duplikat, dan format tanggal.
5. **Feature Engineering** : membentuk fitur bulan, tanggal, dan hari dalam minggu dari kolom tanggal.
6. **Exploratory Data Analysis (EDA)** : menganalisis distribusi total penjualan, kategori produk, dan korelasi fitur numerik.
7. **Menentukan Fitur dan Target** : menggunakan `Total Amount` sebagai target prediksi.
8. **Pembagian Dataset** : membagi data menjadi data training dan testing.
9. **Preprocessing** : menangani nilai kosong, melakukan standardisasi fitur numerik, dan mengubah fitur kategorikal menggunakan One-Hot Encoding.
10. **Pelatihan Model** : melatih Linear Regression, LARS, dan Gradient Boosting Regressor.
11. **Evaluasi dan Perbandingan** : membandingkan performa ketiga model.
12. **Visualisasi Hasil** : membandingkan nilai aktual dan nilai prediksi.

## 8. Evaluasi
Evaluasi model dilakukan menggunakan beberapa metrik berikut:

- **MAE (Mean Absolute Error):** mengukur rata-rata selisih absolut antara nilai aktual dan prediksi.
- **MSE (Mean Squared Error):** menghitung rata-rata kuadrat kesalahan prediksi.
- **RMSE (Root Mean Squared Error):** menunjukkan besarnya kesalahan prediksi dalam satuan yang sama dengan target.
- **R² (Coefficient of Determination):** menunjukkan seberapa baik model menjelaskan variasi nilai target.

Model dibandingkan berdasarkan hasil pengujian. Nilai MAE, MSE, dan RMSE yang lebih rendah umumnya menunjukkan kesalahan yang lebih kecil, sedangkan nilai R² yang lebih tinggi umumnya menunjukkan kemampuan penjelasan yang lebih baik.

Model dengan RMSE terendah dapat dipilih sebagai model terbaik berdasarkan kriteria utama tersebut. Kesimpulan akhir ditentukan setelah hasil pengujian diperoleh.

## 9. Batasan
Proyek ini memiliki beberapa batasan:

1. Dataset hanya berisi informasi transaksi penjualan yang tersedia dan belum tentu mewakili seluruh kondisi bisnis.
2. Jumlah data yang digunakan terbatas pada 1.000 transaksi.
3. `Total Amount` memiliki hubungan perhitungan langsung dengan `Quantity` dan `Price per Unit`. Penggunaan kedua fitur tersebut dapat membuat prediksi terlihat sangat akurat tanpa menunjukkan kemampuan memprediksi perilaku penjualan secara lebih luas.
4. Pembagian training dan testing dari dataset yang sama belum cukup untuk memastikan kemampuan model dalam memprediksi transaksi pada periode mendatang.
5. Hasil evaluasi dipengaruhi oleh karakteristik dataset, fitur yang dipilih, dan algoritma yang digunakan.

## 10. Kesimpulan
Proyek ini menerapkan pendekatan regresi untuk memprediksi total nilai transaksi penjualan menggunakan tiga algoritma Machine Learning, yaitu Linear Regression, LARS, dan Gradient Boosting Regressor.

Performa setiap model dibandingkan menggunakan MAE, MSE, RMSE, dan R². Model dengan hasil evaluasi terbaik dipilih berdasarkan metrik pengujian yang digunakan.

Hasil akhir harus disesuaikan dengan nilai evaluasi yang benar-benar diperoleh saat notebook dijalankan. Karena target `Total Amount` berkaitan langsung dengan jumlah barang dan harga per unit, hasil prediksi juga perlu ditafsirkan secara hati-hati.
