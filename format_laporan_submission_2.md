# Laporan Proyek Machine Learning - Nadila Nur Sholekah

## Project Overview
Dalam proyek ini, melakukan analisis data dari Zomato untuk menciptakan sistem rekomendasi berbasis konten. Sistem rekomendasi adalah jenis sistem penyaringan informasi yang meningkatkan kualitas hasil pencarian dengan memberikan item yang lebih relevan berdasarkan minat pengguna atau riwayat pencariannya.

Dalam proyek ini, menggunakan metode Content Based Filtering. Metode ini hanya menggunakan informasi tentang deskripsi dan atribut dari item yang telah dikonsumsi pengguna sebelumnya untuk memodelkan preferensi pengguna. Algoritma ini mencoba merekomendasikan item yang mirip dengan yang disukai pengguna di masa lalu. Kandidat item dibandingkan dengan item yang sebelumnya diberi nilai oleh pengguna, dan item yang paling cocok akan direkomendasikan.
### Latar Belakang
Restoran merupakan bagian penting dari kehidupan sosial dan ekonomi sebuah kota. Mereka tidak hanya menyediakan makanan, tetapi juga menciptakan ruang bagi orang-orang untuk berkumpul, bersosialisasi, dan merayakan berbagai momen penting dalam hidup mereka. Di kota-kota besar seperti Bengaluru, restoran juga berfungsi sebagai cermin dari keragaman budaya yang ada, dengan menawarkan berbagai jenis masakan dari seluruh dunia.

Bengaluru, sebuah kota metropolitan yang dikenal sebagai pusat teknologi di India, juga menawarkan beragam budaya kuliner. Dari restoran yang menyajikan masakan dari seluruh dunia hingga warung makan lokal, kota ini adalah surga bagi para pecinta kuliner. Menurut laporan dari National Restaurant Association of India (NRAI), sektor layanan makanan di India diperkirakan akan tumbuh dengan CAGR sebesar 8.1% dari 2024 hingga 2028, dengan sektor terorganisir tumbuh sebesar 13.2%. Industri ini bernilai ₹ 5.69 lakh crore dan diproyeksikan tumbuh menjadi ₹ 7.76 lakh crore pada tahun 2028. Hal ini menjadikan India sebagai pasar layanan makanan terbesar ketiga di dunia pada tahun 2028​ (NRAI)​. Dengan lebih dari 12,000 restoran yang tersebar di seluruh kota, industri kuliner di Bengaluru terus berkembang pesat. Meski begitu, membuka restoran baru tetap menantang karena persaingan yang ketat dan berbagai isu seperti biaya properti yang tinggi, meningkatnya biaya bahan makanan, kekurangan tenaga kerja berkualitas, rantai pasokan yang terfragmentasi, dan perizinan yang rumit.

Data dari Zomato berpotensi memberikan wawasan berharga bagi restoran baru untuk menentukan tema, menu, masakan, dan harga yang sesuai dengan lokasi tertentu. Selain itu, data ulasan yang tersedia dapat membantu dalam menentukan peringkat keseluruhan suatu tempat, memberikan gambaran lebih jelas tentang preferensi dan kepuasan pelanggan.

**Referensi**
[NRAI’ released the India Food Services Report 2024](https://nrai.org/nrai-released-the-india-food-services-report-2024/) 

## Business Understanding
Proyek ini bertujuan untuk membantu restoran di Bengaluru bersaing dalam industri kuliner yang sangat kompetitif dengan menggunakan sistem rekomendasi berbasis konten. Bengaluru adalah salah satu kota dengan pertumbuhan restoran tertinggi di India, namun, tantangan seperti biaya properti yang tinggi dan kekurangan tenaga kerja berkualitas sering kali menghambat pertumbuhan restoran baru.
### Problem Statements
- Bagaimana sistem rekomendasi Content Based Filtering dapat digunakan untuk memberikan rekomendasi restoran yang mirip dengan restoran yang disukai pengguna berdasarkan ulasan dan peringkat?
- Bagaimana sistem rekomendasi dapat akurat dalam memberikan insight yang relevan dan meningkatkan daya tarik mereka, restoran baru perlu memanfaatkan data ulasan dan atribut restoran?
### Goals
- Mengembangkan sistem rekomendasi berbasis Content-Based Filtering yang dapat memberikan rekomendasi restoran mirip dengan restoran yang disukai pengguna berdasarkan ulasan dan peringkat, serta memastikan rekomendasi yang diberikan relevan dan berkualitas tinggi.
- Memanfaatkan data ulasan dan atribut restoran untuk memberikan insight yang akurat kepada restoran baru, sehingga mereka dapat membuat keputusan strategis yang efektif untuk meningkatkan daya tarik dan daya saing mereka di pasar.

### Solution statements
Menggunakan kode berikut untuk mencapai tujuan tersebut:
- Menghitung Kesamaan Cosine: Menggunakan nilai kesamaan cosine untuk menentukan restoran yang paling mirip dengan restoran yang diinputkan.
- Menampilkan Restoran Serupa: Menyaring dan mengurutkan restoran berdasarkan kesamaan dan peringkat ulasan.
- Menghindari Duplikasi dan Memprioritaskan Peringkat: Menghilangkan restoran duplikat dan memilih 10 restoran dengan peringkat tertinggi untuk rekomendasi.

## Data Understanding
Dataset yang digunakan dalam sistem rekomendasi ini adalah kumpulan data restoran di Bengaluru yang dikumpulkan dari platform Zomato. Dataset ini berfokus pada restoran di Bengaluru, kota yang dikenal dengan keberagaman budaya makanan dan jumlah restoran yang terus berkembang. Bengaluru merupakan tempat bagi berbagai jenis masakan dari seluruh dunia dan merupakan destinasi utama bagi para pecinta makanan. Dengan sekitar 12.000 restoran yang ada, tantangan bagi restoran baru adalah bersaing dengan yang sudah mapan, terutama mengingat biaya real estat yang tinggi, kenaikan biaya makanan, kekurangan tenaga kerja berkualitas, rantai pasokan yang terfragmentasi, dan perizinan yang berlebihan. Pada proyek ini data yang digunakan adalah dataset dari Kaggle
sebagai berikut :
[Zomato Bangalore Restaurants](https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants)
Berikut adalah rincian variabel dari dataset:
1. url: URL halaman web restoran.
2. address: Alamat lengkap restoran.
3. name: Nama restoran.
4. online_order: Informasi apakah restoran menerima pesanan online.
5. book_table: Informasi apakah restoran memungkinkan pemesanan meja.
6. rate: Peringkat restoran.
7. votes: Jumlah suara atau ulasan yang diberikan kepada restoran.
8. phone: Nomor telepon restoran.
9. location: Lokasi atau area geografis restoran.
10. rest_type: Jenis restoran seperti fine dining atau casual dining.
11. dish_liked: Hidangan yang disukai oleh pengunjung.
12. cuisines: Jenis masakan yang ditawarkan restoran.
13. approx_cost(for two people): Estimasi biaya makan untuk dua orang.
14. reviews_list: Daftar ulasan untuk restoran.
15. menu_item: Daftar item menu yang tersedia di restoran.
16. listed_in(type): Kategori restoran dalam daftar seperti "dining" atau "pubs."
17. listed_in(city): Nama kota tempat restoran terdaftar.

### Exploratory Data Analysis (EDA)
#### Univariate Analysis
Analisis Univariat adalah teknik untuk menganalisis setiap variabel secara terpisah untuk memahami distribusi, frekuensi, dan karakteristik individu dari masing-masing variabel. Pada analisis univariate didapatkan analisis pada data vote sebagai berikut :
    ![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/des1.png)
Selain itu terdapat beberapa analisis lain seperti berikut : 
1. Variabel Kategorikal: Distribusi frekuensi dari setiap kategori akan menunjukkan kategori mana yang paling umum atau langka, serta pola-pola yang mungkin ada dalam data.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/yaaa.png)
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/fafa.png)
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/frfr.png)
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/ththt.png)
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/ththt.png)
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/yjyjyj.png)
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/opopo.png)
2.Variabel Numerik: Histogram membantu dalam memahami bagaimana nilai-nilai numerik tersebar, termasuk keberadaan outlier atau distribusi data yang miring.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/nunu.png)
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/freq.png)
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/dis.png)

#### Bivariat Analysis
Analisis Bivariat bertujuan untuk mengevaluasi hubungan antara dua variabel atau lebih dalam dataset untuk memahami bagaimana variabel-variabel tersebut saling terkait.
1. Scatter Plot: Menunjukkan hubungan antara biaya dan rating, membantu dalam memahami apakah ada pola dalam biaya yang mempengaruhi rating.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/rating.png)
2. Box Plot (Rating & Location): Menyediakan wawasan tentang variasi rating berdasarkan jenis masakan dan lokasi, serta membantu dalam mengidentifikasi kategori atau area yang mungkin memiliki rating lebih tinggi atau lebih rendah.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/rl.png)
3. Box Plot (Cost vs Cuisines): Menunjukkan perbedaan biaya berdasarkan jenis masakan, memungkinkan analisis tentang seberapa mahal jenis masakan tertentu.
Heatmap: Menunjukkan kekuatan dan arah hubungan antara variabel numerik, membantu dalam memahami hubungan antara rating, biaya, dan jumlah suara.
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/CC.png)

## Data Preparation
Pada data preparation ini terdapat dua jenis yakni data preparation dan text preparation. Berikut penjelasan dalam poin mengenai proses data preparation yang digunakan :
1. Menghapus Kolom yang Tidak Digunakan: Dimensionality Reduction digunakan untuk mengurangi kompleksitas data dengan menghapus kolom yang tidak relevan atau tidak diperlukan untuk analisis.
2. Menghapus Data Duplikat: Data Cleaning digunakan untuk memastikan keunikan data untuk menghindari distorsi yang disebabkan oleh entri yang sama muncul lebih dari sekali.
3. Menghapus Nilai NaN: Handling Missing Values digunakan untuk menangani nilai yang hilang dengan menghapus baris yang tidak lengkap untuk menjaga integritas data dalam analisis.
4. Mengubah Nama Kolom: Data Cleaning digunakan untuk menyederhanakan nama kolom untuk meningkatkan keterbacaan dan konsistensi dalam pengolahan data.
5. Konversi dan Pembersihan Data Numerik: Data Transformation digunakan untuk mengonversi data ke format numerik dan membersihkan nilai untuk mempermudah analisis dan pemodelan.
6. Menghapus Simbol Tidak Perlu dari Data: Data Cleaning and Transformation digunakan untuk menghapus simbol atau format yang tidak diperlukan dari data untuk memastikan konsistensi dan akurasi.
7. Menyesuaikan Format Nama dan Nilai Kategorikal: Data Normalization and Encoding digunakan untuk menyesuaikan format data untuk konsistensi dan mengubah nilai kategorikal menjadi format yang dapat digunakan dalam analisis.
8. Menghitung dan Menormalisasi Rating Rata-rata: Aggregation and Normalization digunakan untuk menghitung nilai agregat seperti rating rata-rata dan menormalisasi data untuk memastikan konsistensi dalam analisis.

Berikut penjelasan mengenai proses text preparation :
1. Mengubah Teks Menjadi Lower Case: Normalization yakni mengubah semua teks menjadi huruf kecil untuk memastikan konsistensi dalam analisis teks dan menghindari perbedaan antara huruf besar dan kecil.
2. Menghapus Tanda Baca: Text Cleaning yakni menghilangkan tanda baca dari teks untuk mengurangi noise dan memastikan bahwa analisis fokus pada kata-kata dan konten semantik.
3. Menghapus Stopwords:Text Filtering yakni menghapus kata-kata umum yang sering muncul namun tidak menambah makna signifikan dalam teks, seperti "the", "is", "and", untuk meningkatkan relevansi analisis kata-kata penting.
4. Menghapus URL: Text Cleaning yakni menghapus tautan atau URL dari teks untuk memastikan bahwa informasi yang dianalisis bersih dari elemen-elemen yang tidak relevan.
5. Ekstraksi Kata-Kata Teratas: Feature Extraction yakni menggunakan teknik seperti CountVectorizer untuk mengekstrak kata-kata atau n-gram (misalnya, unigram, bigram) yang paling sering muncul dalam teks, untuk memfokuskan analisis pada kata-kata yang memiliki frekuensi tinggi dan relevansi.
6. Pengambilan Sampel Data: Sampling yakni engambil sampel acak dari dataset untuk mengurangi ukuran data dan mempercepat pemrosesan, sambil tetap mempertahankan representasi yang cukup dari keseluruhan dataset.

Selain itu juga melakukan preparation dengan menggunakan TF-IDF sebagai berikut : 
TF-IDF Vectorizer adalah alat yang digunakan dalam pemrosesan teks untuk mengubah dokumen teks menjadi representasi numerik yang dapat diproses oleh algoritma pembelajaran mesin. Model ini mengukur pentingnya kata dalam dokumen relatif terhadap keseluruhan kumpulan dokumen (korpus). Berikut adalah penjelasan rinci mengenai komponen dan prinsip kerja dari TF-IDF Vectorizer:
1. Term Frequency (TF) digunakan untuk engukur frekuensi kata dalam sebuah dokumen.
Rumus:
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/tfidf.png)
Semakin sering sebuah kata muncul dalam dokumen, semakin tinggi nilai TF-nya. Namun, TF sendiri tidak cukup untuk menilai pentingnya kata secara keseluruhan tanpa mempertimbangkan konteks korpus.
2. Inverse Document Frequency (IDF) digunakan untuk mengukur seberapa penting kata dalam seluruh korpus dokumen.
Rumus:
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/idf.png)
Kata yang muncul di banyak dokumen (seperti "dan", "adalah") dianggap kurang penting, sehingga IDF-nya rendah. Kata yang muncul hanya di beberapa dokumen dianggap lebih informatif, sehingga IDF-nya lebih tinggi.
3. Term Frequency-Inverse Document Frequency (TF-IDF)
Definisi: Kombinasi dari TF dan IDF untuk menilai pentingnya kata dalam dokumen relatif terhadap korpus.
Rumus:
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/tfidf%20(2).png)
Menggabungkan frekuensi kata dalam dokumen dengan kepentingan kata dalam seluruh korpus. Kata yang sering muncul dalam dokumen tetapi jarang di dokumen lain akan memiliki skor TF-IDF tinggi, menandakan kata tersebut relevan dan spesifik untuk dokumen tersebut.

**Parameter-parameter Kunci:**
- analyzer: Menentukan unit analisis, seperti kata-kata (unigrams), pasangan kata (bigrams), atau karakter.
- ngram_range: Mengatur ukuran n-gram yang digunakan. Misalnya, (1, 2) mencakup unigram dan bigram.
- min_df: Menentukan batas frekuensi minimal untuk kata-kata yang dimasukkan dalam model. Kata yang muncul kurang dari batas ini akan diabaikan.
- stop_words: Menentukan kata-kata umum yang diabaikan dalam proses, seperti "the", "and", yang tidak memberikan informasi penting.

**Kegunaan dari TF-IDF adalah sebagai berikut :**
1. Pencarian Informasi: Meningkatkan hasil pencarian dengan memprioritaskan dokumen yang relevan berdasarkan kata kunci.
2. Klasifikasi Teks: Digunakan sebagai fitur dalam algoritma klasifikasi teks untuk menentukan kategori dokumen.
3. Analisis Teks: Membantu dalam menemukan kata-kata penting dan pola dalam kumpulan teks besar.

**Keuntungan dan Keterbatasan:**
Keuntungan:
1. Menangkap konteks kata dalam dokumen dengan mempertimbangkan frekuensi dan kepentingan relatif.
2. Sederhana dan efektif untuk banyak aplikasi teks.
Keterbatasan:
1. Tidak mempertimbangkan urutan kata atau konteks semantik yang lebih dalam.
2. Dapat menghasilkan representasi yang sangat besar dan jarang dari teks, mempengaruhi kinerja.

Secara keseluruhan, TF-IDF Vectorizer adalah teknik yang penting dalam pemrosesan teks yang membantu mengubah teks mentah menjadi format yang dapat digunakan untuk analisis lebih lanjut dan pembelajaran mesin.

## Modeling
**Content-Based Filtering** adalah metode dalam sistem rekomendasi yang mengandalkan analisis fitur dari item yang direkomendasikan. Dalam konteks rekomendasi restoran, pendekatan ini fokus pada analisis atribut restoran seperti ulasan, jenis masakan, dan lokasi untuk memberikan rekomendasi yang relevan berdasarkan preferensi pengguna.

**Kelebihan Content-Based Filtering:**
- **Personalisasi Tinggi:** Rekomendasi disesuaikan dengan preferensi pengguna berdasarkan analisis fitur spesifik restoran, menghasilkan hasil yang relevan bagi individu.
- **Independensi Data Pengguna Lain:** Tidak memerlukan data dari pengguna lain, sehingga rekomendasi tidak bergantung pada data kolaboratif atau historis pengguna lain.
- **Fokus pada Preferensi Unik:** Menghitung preferensi spesifik pengguna tanpa terpengaruh oleh tren atau preferensi umum, memberikan rekomendasi yang lebih sesuai dengan kebutuhan pribadi.

**Kekurangan Content-Based Filtering:**
- **Terbatas pada Fitur Teramati:** Rekomendasi bergantung pada fitur yang dapat dianalisis dalam konten restoran, sehingga mungkin kurang bervariasi jika fitur-fitur yang signifikan tidak teridentifikasi.
- **Kurang Adaptasi terhadap Preferensi Baru:** Tidak menyesuaikan secara otomatis dengan perubahan preferensi pengguna. Jika preferensi berubah, rekomendasi mungkin tetap berdasarkan preferensi lama.

**Teknik Perhitungan Similarity:**
- **Cosine Similarity:** Mengukur kesamaan antara dua vektor dengan menghitung sudut kosinus antara vektor representasi fitur restoran. Dalam sistem rekomendasi ini, Cosine Similarity digunakan untuk menilai seberapa mirip dua restoran berdasarkan fitur seperti ulasan atau jenis masakan. Nilai Cosine Similarity berkisar antara 0 hingga 1, di mana nilai 1 menunjukkan kesamaan yang sangat tinggi dan nilai 0 menunjukkan tidak ada kesamaan.

Proses atau tahapannya adalah sebagai berikut :
1. **Data Input:**
   - Nama restoran yang menjadi basis untuk rekomendasi.
   - Matriks cosine similarity yang mengukur kemiripan antara semua restoran dalam dataset.
2. **Proses Rekomendasi:**
   - **Mengidentifikasi Indeks Restoran:** Model mencari indeks dari restoran yang diinputkan dalam daftar indeks restoran.
   - **Menghitung Kemiripan:** Dengan menggunakan indeks yang ditemukan, model mengekstrak nilai cosine similarity dari restoran tersebut terhadap semua restoran lain dan mengurutkannya dari nilai tertinggi ke terendah.
   - **Ekstraksi Restoran Teratas:** Model mengekstrak 30 restoran teratas berdasarkan nilai cosine similarity yang paling mirip.
   - **Membuat DataFrame Baru:** Dari 30 restoran teratas, model membuat DataFrame baru yang berisi jenis masakan, rating rata-rata, dan biaya dari setiap restoran.
   - **Menghapus Duplikat dan Mengurutkan:** Model menghapus restoran yang memiliki atribut yang sama dan mengurutkan 10 restoran teratas berdasarkan rating tertinggi.
3. **Output:**
   - Daftar 10 restoran teratas yang mirip dengan restoran yang diinputkan, beserta atribut seperti jenis masakan, rating rata-rata, dan biaya.

#### Implementasi Kode
Berikut adalah implementasi kode untuk model ini:

```python
def recommend(name, cosine_similarities=cosine_similarities):

    # Buat daftar untuk menempatkan restoran teratas
    recommend_restaurant = []

    # Temukan indeks restoran yang dimasukkan
    idx = indices[indices == name].index[0]

    # Temukan restoran dengan nilai cosine-sim yang serupa dan urutkan dari jumlah terbesar
    score_series = pd.Series(cosine_similarities[idx]).sort_values(ascending=False)

    # Ekstrak 30 indeks restoran teratas dengan nilai cosine-sim yang serupa
    top30_indexes = list(score_series.iloc[0:31].index)

    # Nama top 30 restoran
    for each in top30_indexes:
        recommend_restaurant.append(list(df_percent.index)[each])

    # Buat kumpulan data baru untuk menampilkan restoran serupa
    df_new = pd.DataFrame(columns=['cuisines', 'Mean Rating', 'cost'])

    # Buat 30 restoran serupa teratas dengan beberapa kolomnya
    for each in recommend_restaurant:
        df_new = pd.concat([df_new, df_percent[['cuisines','Mean Rating', 'cost']][df_percent.index == each].sample()])

    # Hapus restoran dengan nama yang sama dan urutkan hanya 10 teratas berdasarkan peringkat tertinggi
    df_new = df_new.drop_duplicates(subset=['cuisines','Mean Rating', 'cost'], keep=False)
    df_new = df_new.sort_values(by='Mean Rating', ascending=False).head(10)

    print('TOP %s RESTAURANTS LIKE %s WITH SIMILAR REVIEWS: ' % (str(len(df_new)), name))

    return df_new

# Contoh penggunaan
recommend('Jalsa')
```
Selain itu pada proyek ini model yang digunakan juga melibatkan Natural Language Processing (NLP) dalam beberapa tahapannya, terutama dalam pembersihan teks, transformasi, dan sistem rekomendasi berbasis teks. Berikut adalah penjelasan detail mengenai model dan penggunaan NLP:

1. **Pembersihan dan Persiapan Data Teks**:
   - **Normalization**: Mengubah semua teks ulasan menjadi huruf kecil untuk memastikan konsistensi.
   - **Text Cleaning**: Menghapus tanda baca, URL, dan simbol yang tidak diperlukan dari teks ulasan.
   - **Text Filtering**: Menghapus kata-kata umum (stopwords) yang sering muncul tetapi tidak menambah makna signifikan dalam teks.

2. **Ekstraksi Fitur Teks**:
   - **CountVectorizer**: Digunakan untuk mengekstrak kata-kata atau n-gram (misalnya, unigram, bigram) yang paling sering muncul dalam teks ulasan. Ini membantu dalam memahami pola dan frekuensi kata dalam ulasan.

3. **Transformasi Teks dengan TF-IDF**:
   - **TF-IDF (Term Frequency-Inverse Document Frequency)**: Digunakan untuk mengubah teks ulasan menjadi vektor numerik. TF-IDF membantu dalam mengukur pentingnya sebuah kata dalam dokumen tertentu relatif terhadap seluruh korpus, yang penting untuk menangkap makna semantik dari teks ulasan.

4. **Menghitung Kesamaan Kosinus**:
   - **Cosine Similarity**: Digunakan untuk mengukur kesamaan antara vektor TF-IDF dari ulasan restoran yang berbeda. Kesamaan kosinus mengukur sudut antara dua vektor dalam ruang fitur, yang membantu dalam mengidentifikasi ulasan yang mirip.

5. **Sistem Rekomendasi Berbasis Teks**:
   - Sistem rekomendasi ini menggunakan kesamaan kosinus antara vektor TF-IDF dari ulasan untuk merekomendasikan restoran yang memiliki ulasan serupa. Proses ini melibatkan beberapa langkah:
     - Membuat matriks TF-IDF dari teks ulasan.
     - Menghitung kesamaan kosinus antara vektor TF-IDF.
     - Merekomendasikan restoran berdasarkan kesamaan ulasan.

Dengan menggunakan NLP untuk pembersihan, transformasi, dan analisis teks, sistem ini dapat memberikan rekomendasi restoran yang lebih relevan berdasarkan kesamaan ulasan pelanggan.

## Evaluation
**Cosine Similarity** adalah teknik untuk mengukur kesamaan antara dua vektor dengan menghitung sudut kosinus di antara keduanya. Dalam konteks analisis teks, Cosine Similarity digunakan untuk menentukan seberapa mirip dua item berdasarkan representasi numerik mereka, seperti matriks TF-IDF. Fungsi linear_kernel digunakan untuk menghitung nilai Cosine Similarity antar item dengan mengalikan matriks TF-IDF dengan dirinya sendiri. Hasilnya adalah matriks simetri di mana setiap elemen menunjukkan tingkat kesamaan antara item yang bersangkutan.

## Kesimpulan
Proyek ini bertujuan untuk membantu restoran di Bengaluru bersaing dalam industri kuliner yang kompetitif dengan menggunakan sistem rekomendasi berbasis konten. Sistem ini menggunakan metode Content-Based Filtering untuk memberikan rekomendasi restoran yang mirip dengan restoran yang disukai pengguna berdasarkan ulasan dan peringkat. Dengan menghitung kesamaan cosine antara restoran, sistem ini dapat menyaring dan mengurutkan restoran berdasarkan kemiripan dan peringkat ulasan, menghilangkan duplikasi, serta memilih 10 restoran dengan peringkat tertinggi untuk rekomendasi. Hasilnya, restoran baru dapat memanfaatkan data ulasan dan atribut restoran untuk membuat keputusan strategis yang efektif, meningkatkan daya tarik, dan daya saing mereka di pasar.

Berikut merupakan hasil dari recommendation yang tercipta :
![image](https://raw.githubusercontent.com/NadilaNurSholekah/MLTerapan/main/recom.png)
