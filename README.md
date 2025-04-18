# 1. Domain Proyek
Adapun proyek ini membahas tentang predictive analysis dalam membangun sistem klasifikasi kualitas apel yang termasuk pada domain pertanian atau perkebunan. 

## 1.1 Latar Belakang
![5033_20200725142102](https://github.com/user-attachments/assets/4f2c77a5-7a09-4cf4-b163-34783d9989c5)

Buah-buahan merupakan salah satu sumber nutrisi esensial yang sangat penting bagi kesehatan manusia. Di antara berbagai jenis buah, apel menjadi salah satu yang paling populer dan banyak dikonsumsi oleh masyarakat Indonesia. Hal ini disebabkan oleh tingginya kandungan gizi yang dimiliki, seperti serat, kalium, magnesium, fosfor, serta berbagai vitamin yang berperan penting dalam menjaga kesehatan tubuh [[1](http://dx.doi.org/10.31602/tji.v15i4.15945)]. Selain nilai gizinya, apel juga memiliki karakteristik organoleptik yang menarik, seperti rasa manis dan asam yang seimbang, tekstur renyah, serta kandungan air yang menyegarkan.

Berdasarkan data dari Badan Pusat Statistik (BPS), produksi apel di Indonesia masih terpusat di wilayah tertentu, dengan Kabupaten Malang, Jawa Timur, sebagai sentra utama. Namun, dalam beberapa tahun terakhir. Awalnya produksi apel tercata sebesar 224,27 ribu ton pada tahun 2021, menurun menjadi 198,99 ribu ton pada tahun 2022, dan anjlok hingga 95,35 ribu ton pada tahun 2023 [[2](https://radarmalang.jawapos.com/kabupaten-malang/815154084/produksi-apel-malang-terus-menurun)]. Penurunan ini dipengaruhi oleh berbagai faktor, di antaranya adalah dominasi pohon apel yang sudah berusia tua dan tidak lagi produktif, minimnya program peremajaan (replanting), serta peralihan minat petani ke komoditas hortikultura lain yang dinilai lebih menguntungkan secara ekonomi, seperti jeruk [[3](https://doi.org/10.47687/snppvp.v4i1.635 )].

Menyikapi hal tersebut, diperlukan adanya inovasi untuk meningkatkan daya saing apel lokal di pasar nasional. Salah satu strategi yang dapat diterapkan adalah pemanfaatan teknologi kecerdasan buatan (Artificial Intelligence/AI). Dengan pendekatan ini, dapat dikembangkan sistem klasifikasi kualitas apel yang mempertimbangkan variabel seperti jenis, tekstur, dan rasa. Implementasi teknologi ini diharapkan dapat membantu petani dan pelaku industri meningkatkan mutu produk, memperluas pasar, dan mendukung keberlanjutan sektor pertanian nasional [[4](https://doi.org/10.47065/bulletincsr.v3i3.251)].

# 2. Business Understanding
![1_nYVObp29l1_9hPNJKhQvGA-1](https://github.com/user-attachments/assets/bc3fc484-02be-40d6-8f9a-570f3d4d9fac)

Pengembangan model prediksi kualitas apel memiliki potensi besar dalam memberikan manfaat nyata bagi berbagai pemangku kepentingan dalam rantai pasok pertanian, khususnya pada komoditas apel. Penerapan sistem klasifikasi kualitas apel yang akurat dapat membantu petani dalam melakukan pemilahan buah secara lebih efisien berdasarkan variabel seperti jenis, tekstur, dan rasa.

Manfaat utama dari model ini adalah peningkatan mutu hasil panen dan optimalisasi proses pasca-panen, yang pada akhirnya berdampak pada peningkatan nilai jual apel di pasar. Dengan informasi prediktif yang dihasilkan dari model, petani dapat menentukan strategi harga jual yang lebih kompetitif dan berbasis data. Selain itu, distributor dan pedagang dapat menggunakan informasi ini untuk memastikan konsistensi kualitas produk yang mereka jual ke konsumen akhir. Tidak hanya berdampak pada aspek ekonomi, model ini juga dapat meningkatkan kepercayaan konsumen terhadap produk apel lokal. Dengan demikian, pengembangan sistem klasifikasi kualitas apel ini merupakan langkah strategis dalam mendukung modernisasi pertanian dan memperkuat daya saing produk nasional.

## 2.1 Problem Statements
Berdasarkan latar belakang yang telah dipaparkan, dapat dirumuskan beberapa permasalahan utama yang menjadi fokus dalam proyek ini, yaitu:
1. **Bagaimana membangun sebuah model machine learning** yang mampu melakukan klasifikasi kualitas apel berdasarkan atribut seperti jenis, tekstur, dan rasa secara akurat dan efisien.
2. **Apa saja metrik evaluasi yang tepat** untuk mengukur kinerja dari model klasifikasi kualitas apel, sehingga hasil prediksi dapat diandalkan dalam praktik di lapangan.
3. **Bagaimana model klasifikasi ini dapat memberikan manfaat nyata bagi sektor pertanian**, khususnya dalam membantu petani dalam proses pemilahan apel, penentuan harga jual, dan peningkatan daya saing produk lokal.

## 2.2 Goals
Tujuan dari pembuatan proyek ini adalah untuk:
1. **Mengembangkan model klasifikasi kualitas apel berbasis machine learning**, yang mampu mengenali karakteristik apel berdasarkan fitur-fitur yang relevan seperti jenis, tekstur, dan rasa.
2. **Mengevaluasi performa model menggunakan metrik yang sesuai**, seperti akurasi, precision, recall, dan f1-score, guna memastikan keandalan model dalam proses prediksi.
3. **Memberikan solusi berbasis data untuk meningkatkan efisiensi dan produktivitas sektor pertanian**, sehingga model ini dapat digunakan sebagai alat bantu dalam pengambilan keputusan di tingkat petani maupun distributor.

## 2.3 Solution Statements
Adapun solusi yang akan diterapkan untuk menyelesaikan proyek ini yaitu:
  1. Memahami data yang akan digunakan sebagai pelatihan model dengan melakukan eksplorasi data (Exploratory Data Analysis/EDA), baik secara univariat maupun multivariat, untuk melihat distribusi variabel serta hubungan antar fitur seperti jenis, rasa, dan tekstur terhadap kualitas apel.
  2. Melakukan proses pembersihan data (data cleaning), penanganan missing values, encoding data kategorikal, serta standarisasi atau normalisasi data dapat digunakan untuk pelatihan model machine learning.
  3. Mengembangkan beberapa variasi model machine learning untuk melakukan klasifikasi kualitas apel dan melakukan evaluasi terhadap performa masing-masing model. Adapun model yang digunakan meliputi:

     a. **Logistic Regression**: Merupakan model klasifikasi linier yang digunakan untuk memprediksi probabilitas dari dua atau lebih kelas. Model ini cocok digunakan ketika hubungan antar variabel input dan output bersifat linier. [[5](https://doi.org/10.62386/jised.v2i1.59 )].

     b. **K-Nearest Neighbors (KNN)**: Algoritma klasifikasi berbasis distance-based learning yang mengklasifikasikan data baru berdasarkan kedekatannya dengan data pelatihan. KNN efektif dalam mendeteksi pola berdasarkan kemiripan antar sampel, dan telah diaplikasikan dalam berbagai studi kualitas produk pertanian [[6](https://doi.org/10.30591/jpit.v4i1.1267)].

     c. **Support Vector Machine (SVM)**: SVM bekerja dengan mencari hyperplane optimal yang memisahkan kelas-kelas dalam ruang berdimensi tinggi. Algoritma ini terkenal efektif dalam menangani data dengan dimensi besar dan distribusi kompleks [[7](http://dx.doi.org/10.23960/jitet.v12i2.4010)].

     d. **Decision Tree**: Merupakan algoritma berbasis pohon keputusan yang memetakan data ke dalam struktur pohon, memudahkan interpretasi dan pengambilan keputusan. Model ini cocok untuk aplikasi pertanian karena transparan dan mudah diimplementasikan [[8](https://doi.org/10.26418/coding.v9i01.45907	)].

     e. **Random Forest**: Ensemble learning method yang membangun banyak decision tree dan menggabungkan hasilnya untuk meningkatkan akurasi prediksi dan mengurangi overfitting. Random Forest sering digunakan dalam klasifikasi produk pertanian karena ketahanannya terhadap noise dan kemampuan menangani variabel yang kompleks [[9](	https://doi.org/10.36040/jati.v9i2.12854 )].

4. Membangun model baseline dan melakukan optimasi hyperparameter menggunakan Grid Search untuk seluruh algoritma yang digunakan. Setiap model akan dibuat terlebih dahulu dalam bentuk baseline untuk melihat performa awalnya. Setelah itu, dilakukan tuning hyperparameter menggunakan teknik Grid Search guna meningkatkan akurasi dan kestabilan model. Hasil dari model-model yang telah dioptimasi ini kemudian akan dibandingkan berdasarkan **metrik evaluasi seperti akurasi, precision, recall, dan f1-score**, untuk menentukan model terbaik yang paling sesuai digunakan dalam klasifikasi kualitas apel.

# 3. Data Understanding
## 3.1 EDA - Deskripsi Variabel
**Informasi Datasets**
| Jenis | Keterangan |
| ------ | ------ |
| Title | _Apple Quality_ |
| Source | [Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/apple-quality/data) |
| Maintainer | [Nidula Elgiriyewithana ⚡](https://www.kaggle.com/nelgiriyewithana) |
| License | Other (specified in description) |
| Visibility | Publik |
| Tags | _Computer Science, Education, Food, Data Visualization, Classification, Exploratory Data Analysis_ |
| Usability | 10.00 |

Berikut informasi pada dataset: 

Data ini didapatkan dari perusahaan pertanian Amerika, yang disediakan secara publik di kaggle.

Tabel 1. Gambaran Data yang digunakan
| A_id | Size | Weight | Sweetness | Crunchiness | Juiciness | Ripeness | Acidity | Quality |
| ------ | ------ |------ | ------ | ------ | ------ |------ | ------ |------ |
| 0.0 | -3.970049 |-2.512336 | 5.346330 |-1.012009 | 1.844900 |0.329840	| -0.491590483  |good |
| 1.0 | -1.195217 |-2.839257 | 3.664059 |1.588232 | 0.853286 | 0.867530 | -0.722809367  |good |
| 2.0 | -0.292024 |	-1.351282 | -1.738429 | -0.342616 | 2.838636 |-0.038033	| 2.621636473  |bad |
| 3.0 | -0.657196 |-2.271627 | 1.324874 |-0.097875 | 3.637970 |-3.413761	| 0.790723217  |good |
| 4.0 | 1.364217 |-1.296612 | -0.384658 | -0.553006 | 3.030874 | -1.303849	| 0.501984036  |good |

- Dari Tabel 1 di atas terlihat bahwa ada 9 buah kolom/variabel yang digunakan:
  1. `A_id` : identifier unik untuk setiap buah
  1. `Size` : Ukuran buah
  1. `Weight` : Berat buah
  1. `Sweetness` : Tingkat kemanisan buah
  1. `Crunchiness` : Tekstur yang menunjukkan kerenyahan buah
  1.` Juiciness` : Tingkat kesegaran buah
  1. `Ripeness` : Tahap kematangan buah
  1. `Acidity` : Tingkat keasaman buah
  1. `Quality` : Kualitas buah secara keseluruhan (label/target)

Tabel 2. Informasi Umum dari Dataset 
| No | Kolom        | Non-Null Count | Dtype   |
|----|--------------|----------------|---------|
| 0  | Size         | 4000           | float64 |
| 1  | Weight       | 4000           | float64 |
| 2  | Sweetness    | 4000           | float64 |
| 3  | Crunchiness  | 4000           | float64 |
| 4  | Juiciness    | 4000           | float64 |
| 5  | Ripeness     | 4000           | float64 |
| 6  | Acidity      | 4000           | object  |
| 7  | Quality      | 4000           | object  |

Tipe data: float64 (6), object (2)  
Jumlah entri: 4000 (index dari 0 sampai 3999)

---

- Dari Tabel 2 juga dapat dilihat informasi umum dari dataset yang digunakan
  - Terdapat 6 kolom numerik dengan tipe data `float64`, yaitu: **Size, Weight, Sweetness, Crunchiness, Juiciness**, dan **Ripeness**.
  - Terdapat 2 kolom bertipe data `object`, yaitu: **Acidity** dan **Quality**.
  - Terdapat keanehan pada kolom `Acidity` yang bertipe `object`, padahal secara semantik kolom ini menunjukkan tingkat keasaman buah yang seharusnya bersifat numerik.
  - Oleh karena itu, kolom `Acidity` sebaiknya diubah ke tipe data `float64` agar dapat dianalisis secara kuantitatif dan digunakan dalam model machine learning.

Tabel 3 Informasi Statistik dari Dataset

| Feature      | Count  | Mean      | Std Dev   | Min       | 25%       | 50%       | 75%       | Max       |
|--------------|--------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| Size         | 4000.0 | -0.503015 | 1.928059  | -7.151703 | -1.816765 | -0.513703 | 0.805526  | 6.406367  |
| Weight       | 4000.0 | -0.989547 | 1.602507  | -7.149848 | -2.011770 | -0.984736 | 0.030976  | 5.790714  |
| Sweetness    | 4000.0 | -0.470479 | 1.943441  | -6.894485 | -1.738425 | -0.504758 | 0.801922  | 6.374916  |
| Crunchiness  | 4000.0 | 0.985478  | 1.402757  | -6.055058 | 0.062764  | 0.998249  | 1.894234  | 7.619852  |
| Juiciness    | 4000.0 | 0.512118  | 1.930286  | -5.961897 | -0.801286 | 0.534219  | 1.835976  | 7.364403  |
| Ripeness     | 4000.0 | 0.498277  | 1.874427  | -5.864599 | -0.771677 | 0.503445  | 1.766212  | 7.237837  |
| Acidity      | 4000.0 | 0.076877  | 2.110270  | -7.010538 | -1.377424 | 0.022609  | 1.510493  | 7.404736  |

- Berdasarkan informasi statistik yang tersedia, kemungkinan besar dataset ini telah mengalami proses standarisasi, karena nilai-nilai numeriknya berada dalam rentang yang sempit dan simetris, dari negatif ke positif.
- Jika kolom (variabel) tersebut merepresentasikan nilai asli (misalnya berat atau ukuran apel), maka kehadiran nilai negatif akan kurang masuk akal. Hal ini semakin menguatkan dugaan bahwa data telah distandarisasi.
- Penjelasan masing-masing kolom terdapat pada tabel 4 

Tabel 4 Penjelasan Informasi Statistik Dataset
| Kolom (Variabel)         | Masuk Akal? | Outlier? | Penjelasan                                                                                                 |
|---------------|-------------|----------|------------------------------------------------------------------------------------------------------------|
| **Size**      | ✅ Ya       | ⚠️ Ya     | Variasi ukuran apel secara alami terjadi. Namun, nilai ekstrem menunjukkan ada apel yang sangat besar atau sangat kecil. |
| **Weight**    | ✅ Ya       | ⚠️ Ya     | Berat apel cenderung sebanding dengan ukurannya. Nilai outlier mungkin berasal dari varietas unik atau kesalahan pencatatan. |
| **Sweetness** | ✅ Ya       | ⚠️ Ya     | Tingkat kemanisan bisa bervariasi antar jenis apel. Nilai sangat rendah atau tinggi bisa muncul dari jenis yang sangat spesifik. |
| **Crunchiness** | ✅ Ya     | ⚠️ Ya     | Kerennyan apel dapat berbeda-beda. Nilai ekstrem bisa mengindikasikan apel yang sangat renyah atau sangat lembek. |
| **Juiciness** | ✅ Ya       | ⚠️ Ya     | Beberapa apel memang lebih juicy dari yang lain. Nilai ekstrim bisa muncul dari perbedaan jenis apel. |
| **Ripeness**  | ✅ Ya       | ⚠️ Ya     | Tingkat kematangan bisa sangat bervariasi. Nilai ekstrem bisa muncul dari apel yang belum atau terlalu matang. |
| **Acidity**   | ✅ Ya       | ⚠️ Ya     | Tingkat keasaman berbeda antar jenis apel. Nilai tinggi atau rendah bukan hal aneh, tapi tetap bisa dianggap outlier secara statistik. |

## 3.2 EDA - Univariate Analysis
### 3.2.1 Categorical Column
- Karena hanya ada satu kolom yaitu Quality (label/target) sehingga analisis hanya ingin melihat keseimbangannya menggunakan barplot.
![image](https://github.com/user-attachments/assets/05cafb03-d789-471c-a063-b0882c5aa235)
Gambar 1 Barplot Perbandingan Kelas Kualitas Apel

- Insight yang didapatkan dari Gambar 1:
  - Dari grafik yang diberikan terlihat bahwa kolom quality yang mana menjadi label/target seimbang sehingga tidak perlu dilakukan penanganan imbalance data.
  - Menjaga keseimbangan pada data penting agar model tidak bias ke salah satu kelas.

### 3.2.2 Numerical Column
- Untuk kolom numerik dilakukan analisis persebaran data menggunakan histogram untuk melihat apakah datanya terdistribusi normal, skewed, ataupun disribusi lainnya.
![image](https://github.com/user-attachments/assets/5162140f-23bb-4272-89a2-fd6283ae5526)
Gambar 2 Histogram dari Persebaran Masing-Masing Data

- Insight yang didapatkan dari Gambar 2:
  - Berdasarkan visualisasi histogram untuk fitur numerik seperti Size, Weight, Sweetness, Crunchiness, Juiciness, Ripeness, dan Acidity, dapat disimpulkan bahwa semua fitur memiliki bentuk distribusi yang mendekati normal (bell-shaped curve). Hal ini ditunjukkan oleh pola simetris di sekitar nilai tengah, dengan jumlah data yang semakin sedikit pada nilai ekstrem kiri dan kanan.
 
## 3.3 EDA - Multivariate Analysis
### 3.3.1 Numeric Columns
- Pada tahap ini, dilakukan analisis multivariat untuk memahami hubungan antar fitur numerik dan keterkaitannya dengan label.
- Pertama, digunakan heatmap korelasi untuk melihat sejauh mana fitur-fitur numerik saling berkorelasi. Tujuannya adalah untuk mengidentifikasi kemungkinan adanya multikolinearitas, yaitu kondisi di mana dua atau lebih fitur memiliki korelasi yang sangat tinggi, yang dapat memengaruhi performa model prediktif.

![image](https://github.com/user-attachments/assets/5ddb582d-a9f9-400d-a002-218cf6a2ea5b)
Gambar 3 Heatmap Korelasi antar Fitur Numerik

- Insight yang didapatkan dari Gambar 3:
  - Nilai korelasi antar fitur sebagian besar berada di kisaran -0.3 hingga 0.3, yang menandakan hubungan yang lemah atau sangat lemah antar fitur numerik.
  - Hal ini mengindikasikan bahwa setiap fitur numerik memberikan informasi yang relatif independen, sehingga semuanya masih layak dipertimbangkan untuk modeling tanpa risiko multikolineritas data.

- Selanjutnya, dibuat barplot rata-rata setiap fitur numerik terhadap kelas 'quality'. Visualisasi ini membantu memahami pola hubungan antara karakteristik apel (seperti sweetness, crunchiness, dll.) dengan tingkat kualitasnya. Dengan demikian, kita bisa mengidentifikasi fitur mana yang paling berkontribusi dalam membedakan kualitas apel.

![image](https://github.com/user-attachments/assets/1d647ab0-6835-4701-9da8-12b6b94c4175)
Gambar 4 Barplot Hubungan Pengaruh Kualitas Apel dengan Rata-Rata Fitur Numerik

- Adapun insight yang didapatkan dari Gambar 4 dapat dilihat pada Tabel 4 dibawah:

Tabel 4 Insight Pengaruh Kualitas Apel dengan Rata-Rata Fitur Numerik

| Fitur         | Rata-rata pada Apel kualitas "Good" | Rata-rata pada Apel kualitas "Bad" | Insight                                                                 |
|---------------|-----------------------------|-----------------------------|-------------------------------------------------------------------------|
| **Size**      | -0.04                        | -0.97                        | Apel berkualitas bagus cenderung sedikit lebih besar dibanding apel jelek.     |
| **Weight**    | -0.99                        | -0.98                        | Berat apel hampir sama untuk keduanya sehingga fitur ini tidak terlalu berpengaruh.     |
| **Sweetness** | -0.01                        | -0.93                        | Apel berkualitas bagus cenderung lebih manis, sedangkan yang buruk kurang manis.       |
| **Crunchiness** | 0.98                       | 0.99                         | Keduanya renyah sehingga fitur crunchiness tidak terlalu mempengaruhi kualitas apel.  |
| **Juiciness** | 0.98                         | 0.04                         | Apel berkualitas bagus jauh lebih juicy dibanding yang kualitas buruk.     |
| **Ripeness**  | 0.05                         | 0.99                         | Aneh: apel buruk justru lebih matang — kemungkinan **overripe** (apel terlalu matang).       |
| **Acidity**   | 0.03                         | 0.08                         | Perbedaan kecil dimana apel berkualitas bagus cenderung tidak begitu asam dibandingkan apple kualitas buruk.     |

# 4. Data Preparation
- Pada tahap ini, dilakukan serangkaian proses untuk menyiapkan data mentah agar dapat digunakan dalam pembuatan model prediktif. Beberapa langkah penting yang dilakukan dalam proses Data Preparation meliputi:

- **Missing Value (Data yang Hilang)**:  Dilakukan pengecekan terhadap setiap kolom untuk mengetahui apakah terdapat nilai yang hilang.
- 
  - **Duplicated Data (Data Duplikat)**: Data duplikat dicek untuk memastikan tidak ada entri yang berulang yang dapat menyebabkan bias dalam pelatihan model. 

  - **Outlier (Nilai Pencilan)**:  Outlier adalah data yang secara signifikan berbeda dari mayoritas nilai lainnya. Outlier dapat mempengaruhi performa model, terutama pada model yang sensitif terhadap skala data seperti K-Nearest Neighbors (KNN) atau Linear Regression. Deteksi outlier akan dilakukan menggunakan metode statistik seperti:
    - Boxplot untuk visualisasi distribusi data.
    - Z-score/IQR (Interquartile Range) untuk identifikasi nilai ekstrem.  
    Jika ditemukan outlier, penanganan yang dapat dilakukan antara lain:
    - Menghapus data outlier jika jumlahnya sedikit dan tidak mempengaruhi distribusi utama.
    - Melakukan transformasi atau normalisasi untuk mengurangi dampak outlier.

## 4.1 Pengecekan dan Penganganan Missing Value dan Data Duplikat
- Salah satu tahap awal yang sangat penting adalah memastikan bahwa tidak ada nilai yang hilang (`missing value`) atau data yang berulang (`duplicated data`). Berikut adalah kode Python yang digunakan:

```python
# Cek kolom dengan data yang hilang
apple_df.isnull().sum()

# Cek jumlah data yang duplikat
print(f'Jumlah data yang duplikat : {apple_df.duplicated().sum()}')
```
- Hasilnya:
| A_id | Size | Weight | Sweetness | Crunchiness | Juiciness | Ripeness | Acidity | Quality |
| ------ | ------ |------ | ------ | ------ | ------ |------ | ------ |------ |
| NaN | NaN | NaN | NaN |NaN | NaN| NaN	| Created_by_Nidula_Elgiriyewithana  | NaN |

- Hasilnya ditemukan 1 data yang missing yang perlu ditangani dimana salah satu caranya dengan menghapus data tersebut.
 
## 4.2 Pengecekan dan Penanganan Outlier
- Adapun outlier ini akan dicek dengan menggunakan boxplot yang ditampilkan pada Gambar 5
![image](https://github.com/user-attachments/assets/0ebca202-26fe-4d4c-81fa-a7847634b7a2)
Gambar 5 Deteksi Outlier dengan Boxplot

- Insight yang didaptkan dari Gambar 5:
  - Berdasarkan grafik boxplot yang ditampilkan terlihat bahwa hanya semua fitur numerik yang memiliki outlier (ditandai dengan simbol bulat).
  - Adapun untuk outlier yang ditemukan akan dilakukan penanganan dengan dihapus menggunakan metode IQR. IQR dihitung dengan mengurangkan kuartil ketiga (Q3) dari kuartil pertama (Q1) sebagaimana rumus berikut.

$$IQR = Q_3 - Q_1$$

- Q1 adalah kuartil pertama 
- Q3 adalah kuartil ketiga.

- Setelah menangani outlier jumlah data berubah yang awalnya 4000 menjadi 3790.

## 4.3 Mengidentifikasi Fitur dan Label

Tahap selanjutnya adalah mengidentifikasi fitur dan label dari dataset. Fitur (*features*) adalah variabel yang digunakan sebagai input untuk memprediksi target, sedangkan label (*target*) adalah variabel yang ingin diprediksi.

Pada kasus ini:

- **Fitur**:  
  - `Size`  
  - `Weight`  
  - `Sweetness`  
  - `Crunchiness`  
  - `Juiciness`  
  - `Ripeness`  
  - `Acidity`

- **Label**:  
  - `Quality`, karena merupakan target klasifikasi kualitas apel (baik/buruk)

Namun sebelum data dibagi ke dalam data latih dan data uji, perlu dilakukan proses **encoding** terhadap kolom `Quality` karena tipe datanya masih berupa `object` (string), yaitu `"good"` dan `"bad"`. Model machine learning hanya dapat menerima input dalam bentuk numerik, sehingga perlu dilakukan konversi label ke bentuk bilangan bulat.

- Proses encoding:
  - `good` → `1`
  - `bad` → `0`

## 4.4 Membagi Data
Tahap berikutnya adalah membagi data menjadi data latih dan data uji dengan rasio 80:20. Pembagian ini penting untuk memastikan bahwa model tidak hanya belajar dari keseluruhan data tetapi juga diuji pada data yang belum pernah dilihat sebelumnya, sehingga performanya dapat dievaluasi secara objektif.

Jumlah data awal yang tersedia adalah 3790 baris. Setelah dilakukan pembagian data:
  - Data latih (train set): 3.032 data (80%)
- Data uji (test set): 758 data (20%)

## 4.5 Feature Scaling
Pada tahap ini dilakukan proses normalisasi data menggunakan Min-Max Scaling.  Normalisasi dilakukan dikarenakan proyek ini  akan menggunakan model berbasis jarak seperti K-Nearest Neighbors (KNN), Support Vector Machine (SVM), dan juga Logistic Regression, di mana performa model tersebut akan lebih optimal jika setiap fitur berada dalam rentang skala 0 hingga 1.
