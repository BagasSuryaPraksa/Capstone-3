# 1. INTRODUCTION
## 1.1. Background
Daegu adalah wilayah metropolitan terbesar ke-4 di Korea Selatan. Data terbaru dari Kementerian Pertanahan, Infrastruktur, Transportasi, dan Pariwisata Korea menunjukkan peningkatan signifikan dalam transaksi perumahan di kota-kota seperti Daegu, Ulsan, dan Daejeon. Pada bulan Juli 2023, Daegu mencatat 1.890 transaksi apartemen, meningkat 111% dari 895 unit pada bulan Januari.

Apartemen adalah salah satu jawaban untuk kebutuhan perumahan masyarakat modern karena keterbatasan lahan tempat tinggal dan aktivitas bisnis yang padat di daerah perkotaan. Oleh karena itu, akan sangat menarik untuk mengkaji harga apartemen yang dipengaruhi oleh berbagai faktor internal dan eksternal.

Individu atau perusahaan biasanya membuat penawaran unit apartemen. Penawar dapat menjual unit di platform dengan menentukan harga apartemen mereka. Cara tersebut cukup sulit bagi pemilik apartemen untuk menyesuaikan dengan harga pasar. Jika harga terlalu tinggi dibandingkan dengan harga pasar, tentu akan sulit untuk melakukan penjualan. Sebaliknya, jika terlalu rendah, pemilik akan kesulitan mendapatkan keuntungan maksimal.

Sources:

CEIC Data

## 1.2. STAKEHOLDER
Pemilik Apartemen, mereka adalah individu atau perusahaan yang memiliki unit apartemen dan ingin menjual atau menyewakan unit tersebut dengan harga yang menguntungkan. Agen Real Estate, mereka adalah profesional yang membantu pemilik dan pembeli dalam transaksi properti. Mereka membutuhkan informasi tentang tren harga dan faktor-faktor yang mempengaruhi harga untuk memberikan saran yang tepat kepada klien mereka.

## 1.3. Problem Statement
Agen real estate dan pemilik properti sering kesulitan menentukan harga yang optimal untuk apartemen karena banyaknya faktor yang mempengaruhi penetapan harga, seperti lokasi, nilai tanah, dan pengembangan. Penetapan harga yang akurat sangat penting untuk menyeimbangkan keuntungan dan daya tarik pasar.

## 1.4. Goals
Proyek ini bertujuan untuk mengembangkan model prediktif menggunakan Machine Learning untuk menentukan harga apartemen yang sesuai berdasarkan berbagai karakteristik (luas lahan, jarak ke stasiun, tahun dibangun, dll.). Model ini akan membantu para pemangku kepentingan dalam membuat keputusan yang terinformasi tentang penetapan harga, investasi, dan pengembangan properti.

## 1.5. Analytical Approach
Studi ini akan menganalisis hubungan antara fitur apartemen dan harga menggunakan analisis regresi. Prediktor akan mencakup berbagai karakteristik apartemen untuk memperkirakan harga jual.

## 1.6. Evaluation Metrics
The model will be evaluated using:

## Evaluation Metrics
Kami akan mengevaluasi model menggunakan R^2, RMSE, MAE, dan MAPE. Semakin kecil nilai metrik-metrik ini, semakin akurat model dalam memprediksi nilai Target berdasarkan fitur yang digunakan.

R^2 (R-squared)
R^2 (R-squared) adalah metrik evaluasi yang mengukur seberapa baik model regresi cocok dengan data. Nilai R^2 berkisar dari 0 hingga 1, di mana 1 menunjukkan bahwa model sepenuhnya cocok dengan data. Semakin tinggi nilai R^2, semakin baik model dapat menjelaskan variasi dalam data.

RMSE (Root Mean Square Error)
RMSE mengukur sejauh mana perbedaan antara nilai prediksi dari model dan nilai sebenarnya dari data. Metriks ini mengukur deviasi rata-rata antara nilai prediksi dan nilai sebenarnya dengan mengkuadratkan selisihnya, menjumlahkan, dan kemudian mengambil akar kuadrat dari rata-rata tersebut. Rumus RMSE adalah sebagai berikut:
𝑅𝑀𝑆𝐸=∑𝑛𝑖=1(𝑌𝑖−𝑌𝑖ˆ)2𝑛⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯√
𝑅𝑜𝑜𝑡𝑀𝑒𝑎𝑛𝑆𝑞𝑢𝑎𝑟𝑒𝑑𝐸𝑟𝑟𝑜𝑟
∑ adalah sigma (penjumlahan dari suatu urutan atau fungsi)
ŷi adalah nilai prediksi data ke i
yi adalah nilai aktual data ke i
n adalah jumlah data
MAE (Mean Absolute Error)
MAE mengukur kesalahan rata-rata absolut antara prediksi dan nilai sebenarnya. Metrik ini tidak sensitif terhadap outlier dan cocok untuk prediksi nilai CLV karena memberikan bobot yang seragam untuk semua perbedaan. Rumus MAE adalah sebagai berikut:
𝑀𝐴𝐸=∑𝑛𝑖=1|𝑌𝑖−𝑌𝑖ˆ|𝑛
𝑀𝑒𝑎𝑛𝐴𝑏𝑠𝑜𝑙𝑢𝑡𝑒𝐸𝑟𝑟𝑜𝑟
∑ adalah sigma (penjumlahan dari suatu urutan atau fungsi)
ŷi adalah nilai prediksi data ke i
yi adalah nilai aktual data ke i
n adalah jumlah data
MAPE (Mean Absolute Percentage Error)
MAPE mengukur kesalahan dalam bentuk persentase dari nilai sebenarnya, memberikan gambaran tentang akurasi model dalam persentase. Rumus MAPE adalah sebagai berikut:
𝑀𝐴𝑃𝐸=1𝑛∑𝑖=1𝑛|𝑌𝑖−𝑌𝑖ˆ𝑌𝑖|
𝑀𝑒𝑎𝑛𝐴𝑏𝑠𝑜𝑙𝑢𝑡𝑒𝑃𝑒𝑟𝑐𝑒𝑛𝑡𝑎𝑔𝑒𝐸𝑟𝑟𝑜𝑟
∑ adalah sigma (penjumlahan dari suatu urutan atau fungsi)
ŷi adalah nilai prediksi data ke i
yi adalah nilai aktual data ke i
n adalah jumlah data
## Keterbatasan :

Model ini spesifik untuk Daegu dan tidak dapat diterapkan di daerah > lain.
Tidak dapat meramalkan harga masa depan karena hanya menggunakan > > data saat ini.
Hanya mempertimbangkan fitur dataset, mengabaikan faktor eksternal seperti sosial, budaya, dan pengaruh pemerintah.
