# Laporan Proyek Machine Learning - Nadila Nur Sholekah

## Domain Proyek
### **Latar Belakang**
### Latar Belakang Prediksi Saham Apple (AAPL)
Memahami dan memprediksi harga saham Apple Inc. (AAPL) sangat penting karena beberapa alasan yang saling berkaitan dengan pengaruh ekonomi global, sentimen investor, indikator ekonomi, dan inovasi teknologi. Sebagai salah satu perusahaan dengan kapitalisasi pasar terbesar di dunia, kinerja saham Apple memberikan dampak signifikan pada indeks utama seperti S&P 500 dan Nasdaq 100. Prediksi yang akurat mengenai harga saham Apple membantu investor mengantisipasi tren pasar dan membuat keputusan yang lebih baik.

Investor sangat memperhatikan prediksi harga saham Apple karena mampu mempengaruhi sentimen dan perilaku pasar. Prediksi positif dapat menarik lebih banyak investasi, sementara prediksi negatif bisa mendorong kehati-hatian atau penjualan saham. Analis dari perusahaan-perusahaan ternama seperti Wedbush dan B of A Securities rutin memperbarui prediksi mereka, yang dipantau secara ketat oleh pasar.

Kinerja saham Apple sering kali mencerminkan kondisi ekonomi yang lebih luas. Misalnya, tren pendapatan dan laba Apple dapat menunjukkan pola pengeluaran konsumen, tingkat adopsi teknologi, dan kesehatan ekonomi di pasar utama seperti Amerika Serikat dan Tiongkok. Inovasi teknologi yang terus diperkenalkan oleh Apple, seperti iPhone 16 dan headset augmented reality Vision Pro, serta potensi integrasi AI, diharapkan dapat mendorong pertumbuhan yang signifikan. Analis memproyeksikan potensi peningkatan yang besar berkat inovasi-inovasi ini.

Untuk mengatasi tantangan ini, analisis kinerja historis saham Apple memberikan wawasan tentang ketahanan dan pola pertumbuhannya. Terlepas dari penurunan ekonomi, Apple secara konsisten berhasil bangkit kembali karena lini produk yang kuat dan basis pelanggan yang loyal. Riset pasar yang mendalam, termasuk analisis rantai pasokan dan studi perilaku konsumen, juga membantu dalam membuat prediksi yang akurat. Misalnya, indikator rantai pasokan positif di Taiwan menunjukkan penjualan produk Apple yang kuat dalam waktu dekat.

Selain itu, mempertimbangkan faktor makroekonomi seperti suku bunga, inflasi, dan kesehatan ekonomi global sangat penting. Suku bunga yang lebih rendah dan pemulihan ekonomi global dapat meningkatkan pengeluaran konsumen untuk produk premium seperti yang ditawarkan oleh Apple. Mengikuti tren teknologi dan pipeline inovasi Apple juga sangat penting. Fitur-fitur AI yang akan datang dan siklus produk baru diharapkan mendorong pertumbuhan yang signifikan, membuat prediksi berdasarkan faktor-faktor ini sangat relevan.

Dalam keseluruhan, prediksi harga saham Apple adalah aktivitas penting yang memberikan wawasan berharga bagi berbagai pemangku kepentingan, termasuk investor individu, analis, dan manajemen perusahaan. Menggunakan kombinasi data kinerja historis, riset pasar, peramalan ekonomi, dan analisis tren teknologi, investor dan analis dapat membuat prediksi yang lebih informatif tentang pergerakan harga saham Apple.
**Referensi** :
1. [Apple Stock Price Prediction: Analyzing Historical Performance and Future Outlook](https://www.techopedia.com/apple-stock-price-prediction) - Techopedia, 2023.
2. [Apple Inc. (AAPL) Stock Price, News, Quote & History](https://www.stockanalysis.com/stocks/aapl/) - Stock Analysis, 2023.
3. [Apple Stock Price Prediction: 47% Upside on WWDC AI Day and iPhone 16](https://markets.businessinsider.com/news/stocks/apple-stock-price-prediction-47-upside-wwdc-ai-day-iphone-16-2024-5) - Markets Insider, 2024.

## Business Understanding

Proyek ini bertujuan untuk membantu investor dan perusahaan dalam memprediksi harga penutupan saham Apple Inc. (AAPL) menggunakan teknologi analisis prediktif, khususnya dengan memanfaatkan model Long Short-Term Memory (LSTM). Apple Inc. adalah perusahaan teknologi terkemuka yang memiliki pengaruh signifikan di pasar saham global. Berikut merupakan tujuan bisnisnya : 
1. Prediksi Harga Saham: Mengembangkan model prediktif menggunakan LSTM untuk memprediksi harga penutupan saham Apple Inc. Model ini membantu investor dalam membuat keputusan investasi yang lebih informasional dan memungkinkan perusahaan untuk merencanakan strategi keuangan yang lebih efektif.
2. Analisis Tren Pasar: Menganalisis tren historis harga penutupan, volume perdagangan, serta pola moving average untuk memahami dinamika pasar saham Apple Inc. Hal ini membantu dalam memperkirakan perilaku pasar di masa depan.
3. Optimasi Keputusan Investasi: Memberikan wawasan yang lebih dalam tentang faktor-faktor yang mempengaruhi harga saham, seperti volume perdagangan dan pola harga, untuk membantu investor mengambil keputusan investasi yang lebih baik dan merencanakan strategi perdagangan yang lebih efektif.

### Problem Statements
- Bagaimana kita dapat menggunakan analisis prediktif untuk meningkatkan keputusan investasi di pasar saham Apple Inc.?
- Apa faktor-faktor utama yang mempengaruhi perilaku harga saham Apple Inc. dan bagaimana kita dapat memanfaatkannya untuk keuntungan strategis?
- Bagaimana teknologi analisis data dapat digunakan untuk meningkatkan responsivitas terhadap perubahan harga saham Apple Inc. dan memperkuat posisi kompetitif di pasar?
- Bagaimana kita dapat memaksimalkan efisiensi dan produktivitas dalam analisis dan pengambilan keputusan di pasar saham Apple Inc.?
- Bagaimana model prediktif dapat membantu dalam merancang strategi investasi yang lebih adaptif dan efektif di pasar saham Apple Inc.?

### Goals
Proyek ini bertujuan untuk:
- Mengembangkan Model Prediktif: Tujuan utama proyek ini adalah mengembangkan model analisis prediktif yang dapat memperkirakan harga saham Apple Inc. dengan tingkat akurasi yang tinggi. Model ini akan memanfaatkan data historis dan teknik machine learning untuk memberikan prediksi yang lebih akurat dan dapat diandalkan.
- Meningkatkan Keputusan Investasi: Proyek ini bertujuan untuk meningkatkan keputusan investasi di pasar saham Apple Inc. dengan menyediakan analisis mendalam tentang faktor-faktor yang mempengaruhi perilaku harga saham. Dengan pemahaman yang lebih baik tentang pasar, investor dapat membuat keputusan investasi yang lebih informasional dan cerdas.
- Memperkuat Keunggulan Kompetitif: Dengan memanfaatkan teknologi analisis data, proyek ini bertujuan untuk memperkuat posisi kompetitif dalam industri keuangan. Dengan menggunakan model prediktif yang canggih, perusahaan dapat merespons perubahan pasar secara lebih cepat dan efektif, serta mengidentifikasi peluang investasi yang potensial.
- Mengoptimalkan Efisiensi Operasional: Proyek ini juga bertujuan untuk meningkatkan efisiensi dan produktivitas dalam proses analisis dan pengambilan keputusan di pasar saham Apple Inc. Dengan menggunakan teknologi terbaru, proses analisis dapat dipercepat dan diperbaiki, sehingga menghemat waktu dan sumber daya perusahaan.

Metrik evaluasi yang digunakan untuk mengukur keberhasilan mencapai setiap tujuan dapat mencakup akurasi prediksi harga saham, peningkatan dalam keputusan investasi yang menguntungkan, penguatan posisi pasar, dan peningkatan efisiensi operasional. Evaluasi ini akan membantu dalam menilai dampak positif proyek terhadap strategi bisnis perusahaan dan hasil investasi di pasar saham Apple Inc.

 

### Solution statements
Solusi yang disediakan untuk proyek ini melibatkan beberapa tahapan dan pendekatan teknis yang telah diimplementasikan berdasarkan data historis harga saham Apple Inc. Berikut adalah penjelasan yang lebih rinci mengenai solusi yang diberikan:
1. Eksplorasi Data (Exploratory Data Analysis - EDA):
Sebelum melatih model prediktif, dilakukan proses EDA untuk memahami karakteristik historis harga saham Apple Inc. EDA membantu dalam mengidentifikasi pola, tren, dan hubungan antar variabel yang signifikan. Analisis ini penting untuk mempersiapkan data sebelum digunakan dalam model prediktif, serta untuk mendapatkan wawasan yang diperlukan dalam memahami perilaku harga saham.
2. Algoritma LSTM (Long Short-Term Memory):
Algoritma LSTM dipilih sebagai metode machine learning yang optimal untuk memodelkan dan memprediksi data deret waktu, seperti harga saham. LSTM cocok digunakan untuk menangani data deret waktu yang kompleks dengan mempertahankan ingatan jangka panjang, yang penting dalam meramalkan perilaku harga saham yang cenderung fluktuatif.
3. Preprocessing Data:
Sebelum data dimasukkan ke dalam model LSTM, dilakukan proses preprocessing seperti penskalaan data menggunakan MinMaxScaler. Penskalaan ini mengubah data menjadi rentang yang lebih kecil (0 hingga 1), sehingga mempercepat konvergensi algoritma saat dilatih.
4. Pembentukan Model LSTM:
Model LSTM dibangun dengan arsitektur yang terdiri dari dua lapisan LSTM bertingkat, yang diakhiri dengan dua lapisan Dense untuk memprediksi harga penutupan saham. Arsitektur ini dirancang untuk memungkinkan pembelajaran pola yang kompleks dari data deret waktu harga saham.
5. Optimisasi dan Pelatihan Model:
Model LSTM dioptimalkan dengan menggunakan optimizer Adam dan fungsi loss Mean Squared Error (MSE). Proses pelatihan dilakukan dengan membagi data menjadi set pelatihan dan pengujian, di mana model dilatih menggunakan data historis sebelumnya untuk memprediksi harga penutupan saham di masa depan.
6. Evaluasi Kinerja:
Metrik evaluasi yang digunakan untuk mengukur kinerja model LSTM adalah Root Mean Squared Error (RMSE). RMSE memberikan gambaran tentang seberapa dekat prediksi harga saham dengan nilai sebenarnya. Semakin rendah nilai RMSE, semakin baik kualitas prediksi model.
7. Visualisasi Hasil Prediksi:
Setelah model dilatih, hasil prediksi harga penutupan saham Apple Inc. dievaluasi dan divisualisasikan menggunakan grafik untuk membandingkan prediksi dengan data aktual. Visualisasi ini membantu dalam memahami keakuratan dan keandalan model dalam meramalkan perilaku harga saham di masa depan.

Melalui pendekatan ini, diharapkan solusi yang disediakan mampu memberikan prediksi harga saham Apple Inc. yang lebih akurat dan dapat diandalkan. Dengan menggunakan LSTM dan metode preprocessing yang tepat, proyek ini bertujuan untuk meningkatkan kualitas keputusan investasi dan membantu pemangku kepentingan dalam membuat keputusan yang lebih informasional di pasar saham Apple Inc.

## Data Understanding
PAda proyek ini dataset yang digunakan berasal dari Yahoo Finance yang diambil dengan menggunakan code sebagai berkut :
`yf.pdr_override()`
`df = pdr.get_data_yahoo('AAPL', start='2012-01-01', end=datetime.now())`
### Variabel-variabel pada AAPL dataset adalah sebagai berikut:
- Open: Harga pembukaan saham pada awal hari perdagangan.
- High: Harga tertinggi yang dicapai oleh saham selama hari perdagangan.
- Low: Harga terendah yang dicapai oleh saham selama hari perdagangan.
- Close: Harga penutupan saham pada akhir hari perdagangan.
- Adj Close: Harga penutupan yang disesuaikan, memperhitungkan aksi korporasi seperti dividen, pemecahan saham (stock split), dan lainnya yang dapat mempengaruhi harga saham.
- Volume: Jumlah saham yang diperdagangkan selama hari tersebut.
company_name: Nama perusahaan, dalam hal ini "Apple Inc." (AAPL adalah simbol ticker untuk Apple Inc.).

### Pendalaman Data Understanding
1. Melakukan Eksplorasi Data (Exploratory Data Analysis - EDA) untuk memahami data sebelum membangun model prediktif
EDA meliputi mendeskripsikan variabel, mencari outliers, analisis univariate hingga multivariate, serta mengecek dan membersihkan missing values.
a. Mendeskripsikan Variabel
Langkah pertama adalah mendeskripsikan variabel dalam dataset. Ini dilakukan untuk mendapatkan gambaran umum tentang distribusi dan statistik dasar dari setiap variabel, seperti rata-rata, median, standar deviasi, nilai minimum, dan maksimum.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/Screenshot%202024-07-15%20052423.png)
b. Mencari Outliers
Outliers adalah data yang jauh dari nilai lainnya dalam dataset. Untuk mencari outliers, kita menggunakan boxplot yang membantu mengidentifikasi nilai yang tidak wajar dalam variabel.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/boxplot.png)
c. Analisis Univariate
Analisis Univariate: Ini dilakukan dengan melihat distribusi dari satu variabel menggunakan histogram. Histogram membantu memahami bagaimana data tersebar dalam variabel tersebut.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/g.png)
Pada proyek ini dilakukan analisis Moving Average (MA) membantu mengidentifikasi arah tren harga dalam jangka waktu tertentu. Misalnya, jika harga saham berada di atas moving average, itu menandakan tren naik, dan sebaliknya, jika di bawah, itu menandakan tren turun.Moving Average meratakan data harga dengan cara menghitung rata-rata harga dalam jangka waktu tertentu. Ini mengurangi noise atau fluktuasi acak dalam data harga, memberikan gambaran yang lebih jelas tentang tren pasar.
Misalnya, MA 50-hari akan memberikan pandangan yang lebih halus dari pergerakan harga dalam 50 hari terakhir dibandingkan dengan harga harian yang fluktuatif.
Moving Average dapat memberikan sinyal beli dan jual. Ketika harga menembus di atas moving average, ini bisa menjadi sinyal beli, dan ketika harga jatuh di bawah moving average, ini bisa menjadi sinyal jual.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/d.png)
Selain hal tersebut dilakukan pula analisis Dialy Return dimana mengukur persentase perubahan harga dari satu hari ke hari berikutnya. Ini memberikan wawasan tentang kinerja harian suatu aset atau portofolio. Misalnya, jika harga saham naik dari $100 menjadi $105 dalam satu hari, daily return-nya adalah 5%. Dengan menganalisis daily return, kita dapat menghitung volatilitas atau standar deviasi return harian. Volatilitas adalah ukuran risiko, menunjukkan seberapa besar harga dapat berfluktuasi dalam periode tertentu. Tingkat volatilitas yang tinggi menunjukkan risiko yang lebih tinggi, sementara tingkat yang rendah menunjukkan risiko yang lebih rendah.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/q.png)
d. Analisa Bivariat
Heatmap korelasi adalah alat visualisasi yang menunjukkan hubungan antara variabel-variabel dalam suatu dataset. Korelasi mengukur seberapa kuat hubungan linear antara dua variabel, dengan nilai berkisar dari -1 (korelasi negatif sempurna) hingga 1 (korelasi positif sempurna).
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/k.png)
Pada Heatmap korelasi dari proyek ini memberikan visualisasi hubungan linear antara variabel-variabel saham dalam dataset. Korelasi tinggi antara harga saham harian menunjukkan bahwa mereka bergerak seiring, sementara volume perdagangan tidak memiliki hubungan kuat dengan pergerakan harga. Informasi ini sangat berguna untuk analisis lebih lanjut dan pengembangan model prediktif dalam konteks perdagangan saham.
2. Mengecek Missing Values dan Membersihkan Data
Langkah selanjutnya adalah mengecek apakah ada missing values dalam dataset. Missing values dapat mempengaruhi hasil analisis dan model prediktif, sehingga perlu diidentifikasi dan dibersihkan. Pada dataset ini tidak ditemukan missing value sama sekali.

## Data Preparation
Proses pembagian dataset menjadi data training dan data testing penting dalam pengembangan model machine learning. Ini dilakukan untuk mengevaluasi performa model pada data yang belum pernah dilihat sebelumnya dan untuk menghindari overfitting.
Data training digunakan untuk melatih model, sedangkan data testing digunakan untuk menguji seberapa baik model yang dilatih dapat melakukan prediksi pada data yang belum pernah dilihat sebelumnya. Dengan memisahkan data training dan data testing, kita dapat mengukur sejauh mana model dapat mengeneralisasi dan memprediksi dengan akurat pada data baru.
Rasio 80:20 sering digunakan sebagai perbandingan pembagian data training dan data testing. Data training sebesar 95% digunakan untuk melatih model, sementara data testing sebesar 5% digunakan untuk menguji performa model. Rasio ini merupakan aturan praktis umum yang memberikan keseimbangan antara memiliki jumlah data yang cukup untuk melatih model dan menyediakan data yang cukup untuk menguji performa model. Namun, rasio ini dapat bervariasi tergantung pada karakteristik dataset dan kebutuhan proyek tertentu.
Selain hal tersebut dilakukan pula standarisasi data  menggunakan MinMaxScaler dari pustaka sklearn.preprocessing. Proses ini mengubah data menjadi skala antara 0 dan 1 sebelum model dilatih.Sehinggan seluruh dataset 'Close' yang awalnya mungkin memiliki nilai beragam, kini diubah menjadi nilai antara 0 dan 1 agar lebih mudah dan efektif untuk dilatih oleh model LSTM. Ini membantu model dalam konvergensi dan stabilitas selama pelatihan.

## Modeling
Dalam pengembangan model prediksi harga saham, kami membangun model Long Short-Term Memory (LSTM) menggunakan Sequential API dari Keras. Model ini terdiri dari dua lapisan LSTM dengan 128 unit pada lapisan pertama dan 64 unit pada lapisan kedua. Lapisan pertama diatur dengan `return_sequences=True` untuk memastikan keluaran dari setiap langkah waktu dikembalikan sebagai urutan penuh. Bentuk input data didefinisikan oleh `input_shape=(x_train.shape[1], 1)`. Setelah lapisan LSTM, dua lapisan Dense ditambahkan, yaitu dengan 25 unit dan 1 unit, yang terakhir digunakan untuk membuat prediksi akhir.
Model ini kemudian dikompilasi menggunakan optimizer Adam dan fungsi kerugian Mean Squared Error (MSE) untuk meminimalkan kesalahan prediksi. Proses pelatihan model dilakukan dengan menggunakan data pelatihan (`x_train` dan `y_train`), dengan ukuran batch yang sangat kecil (1) dan jumlah epoch sebanyak 25. 
Pada pengujian lain, model juga dilatih dengan ukuran batch yang lebih besar (32) dan menggunakan data validasi (`X_test` dan `y_test`) untuk memantau kinerja model selama pelatihan. Pada data validasi ini menggunakan metriks evaluasi menggunakan Root Mean Squared Error (RMSE). Root Mean Squared Error (RMSE) adalah metrik yang digunakan untuk mengukur rata-rata kesalahan kuadrat dari prediksi model. 


## Evaluation
Dalam proyek ini, metrik utama yang digunakan untuk mengevaluasi performa model adalah Mean Squared Error (MSE). MSE adalah metrik yang umum digunakan dalam masalah regresi untuk mengukur rata-rata kuadrat selisih antara nilai yang diprediksi oleh model dan nilai aktual. Secara matematis, MSE didefinisikan sebagai:

![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/Screenshot%202024-07-15%20135515.png)

MSE memberikan gambaran seberapa jauh nilai yang diprediksi oleh model dari nilai sebenarnya. Nilai MSE yang lebih rendah menunjukkan bahwa model memiliki performa yang lebih baik dalam hal akurasi prediksi. Pada proyek ini terdapat eval.
Pada dataset validasi menggunakan metriks evaluasi Root Mean Square Error (RMSE) dihitung dengan cara mengkuadratkan selisih antara nilai yang diprediksi dan nilai sebenarnya, menghitung rata-rata dari selisih kuadrat tersebut, dan kemudian mengambil akar kuadrat dari rata-rata tersebut. Formula RMSE adalah sebagai berikut: 

![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/Screenshot%202024-07-15%20142910.png)

## Kesimpulan
Proyek ini bertujuan untuk membantu investor dan perusahaan dalam memprediksi harga penutupan saham Apple Inc. (AAPL) menggunakan model Long Short-Term Memory (LSTM). Evaluasi model menunjukkan bahwa metrik utama, Mean Squared Error (MSE) sebesar 1.1593e-04 dan Root Mean Square Error (RMSE) sebesar 4.1550, mengindikasikan tingkat akurasi yang tinggi dalam prediksi harga saham. 
**Pencapaian Tujuan :**
1. Mengembangkan Model Prediktif: Model LSTM yang dikembangkan berhasil memberikan prediksi harga saham dengan akurasi yang tinggi, dibuktikan dengan nilai MSE dan RMSE yang rendah.
2. Meningkatkan Keputusan Investasi: Model ini menyediakan analisis mendalam tentang faktor-faktor yang mempengaruhi harga saham, memungkinkan investor untuk membuat keputusan investasi yang lebih informasional dan cerdas.
3. Memperkuat Keunggulan Kompetitif: Dengan menggunakan teknologi analisis data yang canggih, perusahaan dapat merespons perubahan pasar dengan cepat dan efektif, serta mengidentifikasi peluang investasi potensial.
4. Mengoptimalkan Efisiensi Operasional: Proses analisis dan pengambilan keputusan menjadi lebih efisien dan produktif, menghemat waktu dan sumber daya perusahaan.

**Manfaat Analisis**
1. Analisis Prediktif: Model LSTM membantu meningkatkan keputusan investasi di pasar saham Apple Inc. dengan memberikan prediksi harga yang akurat.
2. Identifikasi Faktor-faktor Utama: Analisis tren historis dan pola moving average memberikan wawasan tambahan tentang faktor-faktor yang mempengaruhi harga saham.
3. Teknologi Analisis Data: Teknologi ini meningkatkan responsivitas terhadap perubahan harga saham dan memperkuat posisi kompetitif di pasar.
4. Efisiensi dan Produktivitas: Proyek ini memaksimalkan efisiensi dan produktivitas dalam analisis dan pengambilan keputusan di pasar saham Apple Inc.
5. Strategi Investasi Adaptif: Model prediktif membantu merancang strategi investasi yang lebih adaptif dan efektif.
Secara keseluruhan, proyek ini berhasil menjawab problem statement, mencapai tujuan yang diharapkan, dan memberikan solusi yang berdampak positif terhadap business understanding, meningkatkan keputusan investasi, memperkuat keunggulan kompetitif, dan mengoptimalkan efisiensi operasional di pasar saham Apple Inc.
Untuk hasil prediksi didapatkan gambar grafik sebagai berikut : 
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/pred.png)
