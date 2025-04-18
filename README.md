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






