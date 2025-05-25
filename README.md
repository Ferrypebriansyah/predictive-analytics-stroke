# Predictive Analysis: Stroke Risk Prediction
- **Nama:** Ferry Pebriansyah
- **Email:** ferryfeb10@gmail.com
- **ID Dicoding:** ferrypebriansyah

## Domain Proyek
Stroke merupakan salah satu penyebab utama kematian dan kecacatan di Indonesia. Penyakit ini terjadi akibat gangguan aliran darah ke otak, yang menyebabkan kerusakan pada jaringan otak dan mengakibatkan gangguan fungsi tubuh, baik secara fisik, bicara, maupun kognitif. Dalam beberapa kasus, stroke bahkan dapat menyebabkan kematian secara tiba-tiba jika tidak segera mendapatkan penanganan.

Berdasarkan Data Riset Kesehatan Dasar (Riskesdas) 2018, prevalensi stroke di Indonesia mencapai 10,9 per 1.000 penduduk, dengan angka kejadian tertinggi terjadi di Provinsi Sulawesi Selatan. Angka ini mengalami peningkatan dibandingkan data sebelumnya pada tahun 2013 yang menunjukkan angka 7 per 1.000 penduduk. Hal ini menunjukkan bahwa stroke menjadi beban kesehatan yang makin besar bagi masyarakat Indonesia.

Faktor-faktor risiko utama seperti hipertensi, diabetes, merokok, obesitas, serta kurangnya aktivitas fisik menjadi pemicu utama meningkatnya angka kejadian stroke. Selain itu, tingkat edukasi masyarakat mengenai gejala awal stroke dan pentingnya pencegahan masih tergolong rendah, sehingga banyak kasus baru ditemukan saat sudah parah.

Oleh karena itu, pemahaman tentang faktor-faktor risiko yang memengaruhi stroke sangat penting sebagai langkah awal dalam upaya pencegahan dan pengendalian. Peningkatan kesadaran masyarakat dan dukungan sistem layanan kesehatan menjadi kunci utama dalam menekan angka kejadian stroke di Indonesia.

**Referensi**:
- Badan Penelitian dan Pengembangan Kesehatan. (2018). Laporan Nasional Riskesdas 2018. Kementerian Kesehatan RI.
- Kementerian Kesehatan RI. (2020). Situasi dan Analisis Lanjut Penyakit Stroke. Pusat Data dan Informasi Kemenkes RI.

## Business Understanding

### Problem Statements
1.   Faktor-faktor apa saja yang paling berkontribusi terhadap risiko seseorang mengalami stroke?
2.   Bagaimana model Machine Learning dapat memprediksi apakah seseorang berpotensi terkena stroke berdasarkan kondisi yang mereka input?

### Goals
1. Mengidentifikasi faktor-faktor utama yang berkontribusi terhadap risiko seseorang mengalami stroke, berdasarkan atribut seperti usia dan berbagai gejala klinis (contoh: nyeri dada, sesak napas, detak jantung tidak teratur, dan lainnya).
2. Mengetahui bagaimana cara model Machine Learning dapat memprediksi apakah seseorang berpotensi terkena stroke berdasarkan kondisi yang mereka input

### Solution statements
Untuk menjawab permasalahan yang telah dirumuskan, solusi yang diusulkan dalam proyek ini adalah melakukan analisis data berdasarkan riwayat kesehatan dan gejala yang dialami pasien. Langkah-langkah utama dalam solusi ini meliputi:

1. Eksplorasi data (Exploratory Data Analysis) untuk memahami distribusi variabel, mendeteksi pola-pola penting, dan mengidentifikasi hubungan awal antara gejala, kondisi kesehatan, serta faktor risiko dengan kemungkinan terjadinya stroke.
2. Menguji model Machine Learning yang mampu memprediksi risiko stroke seseorang secara akurat berdasarkan data input kondisi kesehatan (seperti tekanan darah, detak jantung, gejala nyeri dada, gaya hidup, dan faktor risiko lainnya), guna membantu deteksi dini dan pengambilan keputusan medis yang lebih cepat dan tepat.
 
## Data Understanding
[Stroke Risk Prediction Dataset Based on Symptoms](https://www.kaggle.com/datasets/mahatiratusher/stroke-risk-prediction-dataset)


Dataset yang digunakan untuk memprediksi risiko stroke pada seseorang diperoleh dari platform open source Kaggle dan dipublikasikan oleh mahatiratusher. Dataset ini dirancang untuk memperkirakan kemungkinan seseorang mengalami stroke berdasarkan berbagai gejala klinis dan faktor risiko kesehatan lainnya. Data mencakup informasi dari berbagai individu yang dilengkapi dengan 18 fitur serta label risiko stroke.

Fitur-fitur dalam dataset mencakup gejala umum seperti nyeri dada, sesak napas, kelelahan, detak jantung tidak teratur, tekanan darah tinggi, serta faktor tambahan seperti usia. Selain itu, terdapat dua fitur target, yakni persentase risiko stroke dan status risiko stroke dalam bentuk biner (berisiko atau tidak).

Secara keseluruhan, dataset ini memuat 70.000 data, yang masing-masing dapat digunakan untuk membangun model prediktif guna membantu diagnosis awal dan pengambilan keputusan dalam bidang kesehatan, khususnya dalam pendeteksi gejala awal stroke.

### Variabel-variabel pada dataset:

| Variabel                     | Tipe Data  | Deskripsi                                                  |
|------------------------------|------------|------------------------------------------------------------|
| Chest Pain                   | int64     | Adanya rasa nyeri dada (1 = ya, 0 = tidak)                 |
| Shortness of Breath          | int64     | Mengalami sesak napas (1 = ya, 0 = tidak)                  |
| Irregular Heartbeat          | int64     | Irama jantung tidak teratur (1 = ya, 0 = tidak)            |
| Fatigue & Weakness           | int64     | Merasa lelah dan lemah (1 = ya, 0 = tidak)                 |
| Dizziness                   | int64     | Merasa pusing atau kepala berputar (1 = ya, 0 = tidak)     |
| Swelling (Edema)            | int64     | Pembengkakan pada tubuh (1 = ya, 0 = tidak)                 |
| Pain in Neck/Jaw/Shoulder/Back | int64  | Nyeri pada leher, rahang, bahu, atau punggung (1 = ya, 0 = tidak) |
| Excessive Sweating          | int64     | Berkeringat berlebihan (1 = ya, 0 = tidak)                  |
| Persistent Cough            | int64     | Batuk terus menerus (1 = ya, 0 = tidak)                     |
| Nausea/Vomiting             | int64     | Mual atau muntah (1 = ya, 0 = tidak)                        |
| High Blood Pressure         | int64     | Tekanan darah tinggi (1 = ya, 0 = tidak)                    |
| Chest Discomfort (Activity) | int64     | Ketidaknyamanan dada saat aktivitas (1 = ya, 0 = tidak)    |
| Cold Hands/Feet             | int64     | Tangan atau kaki terasa dingin (1 = ya, 0 = tidak)          |
| Snoring/Sleep Apnea         | int64     | Mendengkur atau apnea tidur (1 = ya, 0 = tidak)             |
| Anxiety/Feeling of Doom     | int64     | Merasa cemas atau takut (1 = ya, 0 = tidak)                 |
| Age                         | int64     | Umur pada pasien/responden                                  |
| Stroke Risk (%)             | Float      | Estimasi probabilitas terjadinya stroke dalam persen (0 - 100%) |
| At Risk                     | int64     | Status risiko stroke (1 = berisiko, 0 = tidak)              |



### Exploratory Data Analysis - Univariate Analysis
<p align="center">
  <img src="https://github.com/user-attachments/assets/9bf9d843-192a-4859-a59e-c26b4542adb4" width="1000"/>
</p>

Gambar di atas dapat diinterpretasikan sebagai berikut:
1. Chest Pain: Jumlah responden yang mengalami dan tidak mengalami nyeri dada relatif seimbang.
2. Shortness of Breath: Responden yang mengalami sesak napas dan yang tidak mengalaminya hampir seimbang.
3.Irregular Heartbeat: Proporsi antara yang mengalami detak jantung tidak teratur dan yang tidak juga cukup seimbang.
4.Fatigue & Weakness: Tingkat kelelahan dan kelemahan hampir merata di antara responden.
5.Dizziness: Responden yang mengalami pusing dan tidak mengalami menunjukkan jumlah yang sebanding.
6.Swelling (Edema): Pembengkakan (edema) juga terjadi pada proporsi yang hampir sama antara kedua kelompok.
7. Pain in Neck/Jaw/Shoulder/Back: Jumlah responden yang merasakan nyeri di bagian tersebut relatif seimbang dengan yang tidak merasakan.
8. Excessive Sweating: Responden yang mengalami keringat berlebihan hampir setara dengan yang tidak.
9. Persistent Cough: Jumlah responden dengan dan tanpa batuk berkepanjangan hampir setara.
10. Nausea/Vomiting: Tidak ada perbedaan mencolok antara responden yang mengalami dan yang tidak.
11. High Blood Pressure: Tekanan darah tinggi dialami dan tidak dialami oleh responden dalam jumlah yang hampir sama.
12. Chest Discomfort (Activity): Jumlah responden yang mengalami ketidaknyamanan dada saat aktivitas hampir seimbang.
13. Cold Hands/Feet: Responden dengan dan tanpa gejala tangan/kaki dingin hampir setara jumlahnya.
14. Snoring/Sleep Apnea: Proporsi antara yang mengalami dan tidak mengalami mendengkur/sleep apnea cukup seimbang.
15. Anxiety/Feeling of Doom: Kecemasan atau firasat buruk dialami oleh hampir setengah dari responden.
16. Age: Distribusi usia cukup merata, tidak condong ke kelompok usia tertentu.
17. Stroke Risk (%): Distribusi risiko stroke mengikuti pola normal, dengan mayoritas berada di risiko sedang.
18. At Risk (Binary): Proporsi responden yang tergolong berisiko dan tidak berisiko relatif seimbang.

### Exploratory Data Analysis - Multivariate Analysis
#### 1. Membandingkan hubungan **usia** dan risiko stroke
<p align="center">
  <img src="https://github.com/user-attachments/assets/7d6224c9-fbd3-4739-bd02-3f55c9abb956" width="500"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/31550419-c551-4eac-836a-8ca4ad76ea66" width="500"/>
</p>

> **insight:**
> Pasien yang mengalami stroke memiliki rata-rata usia jauh lebih tinggi dibandingkan yang tidak mengalami stroke. Rata-rata usia penderita > stroke berada di atas 60 tahun. Sementara itu, rata-rata usia pasien yang tidak mengalami stroke berada di bawah 40 tahun.

#### 2. Hubungan Gejala dengan Risiko Stroke (Multivariate Countplot)
<p align="center">
  <img src="https://github.com/user-attachments/assets/68572ed8-80ef-4fbc-b556-9cf04ba53675" width="700"/>
</p>

> **insight:**
> Usia dan tekanan darah tinggi merupakan faktor risiko yang cukup kuat terhadap stroke. Gejala seperti sesak napas, kelelahan,
> detak jantung tidak teratur, dan nyeri dada juga ikut berkontribusi, meskipun dalam tingkat korelasi yang lebih lemah.

### Data Quality Verification
#### Melihat dan menampilkan baris data duplikat
<p align="center">
  <img src="https://github.com/user-attachments/assets/af9194d6-6bdb-4bfc-99b4-a855a8498fa3" width="1000"/>
</p>

> **insight:**
> Ditemukan sebanyak **1021** data duplikat dalam dataset ini. Oleh karena itu, selanjutnya akan dilakukan proses pembersihan data (data cleaning) sangat penting untuk memastikan bahwa dataset yang digunakan bebas dari redundansi, sehingga hasil prediksi menjadi lebih akurat dan dapat diandalkan.

#### Memeriksa Missing Value
<p align="center">
  <img src="https://github.com/user-attachments/assets/9c19d7de-637b-47a2-a39a-98abbf3e1eb1" width="400"/>
</p>

> **insight:** Tidak ditemukan missing value pada dataframe diatas


#### Memeriksa Outlier
<p align="center">
  <img src="https://github.com/user-attachments/assets/c46f3774-c76e-48b6-ab57-386ef7fea6e2" width="600"/>
</p>



<p align="center">
  <img src="https://github.com/user-attachments/assets/c1369876-6b80-419e-a12a-c9bc067b2c1b" width="600"/>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f31e5273-462c-4e5e-9c6e-7ffeb8f93432" width="600"/>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/a81edf5e-1840-46fe-9a24-c9e8750ab540" width="600"/>
</p>

> **Hasil Visualisasi Boxplotnya yaitu:** 
<p align="center">
  <img src="https://github.com/user-attachments/assets/bd3684b9-1fe8-4cd6-b77d-1e9033c94bbe" width="800"/>
</p>

> **Insight**:
> Fitur-fitur biner contohnya seperti Chest Pain, Shortness of Breath, dan Irregular Heartbeat tidak memiliki outlier,
> karena memang hanya memiliki dua nilai yang valid (0 dan 1).
> Oleh karena itu, tidak perlu dilakukan deteksi atau penanganan outlier untuk fitur-fitur ini.

## Data Preparation

### Data Cleaning
#### 1. Menghapus data duplikat
<p align="center">
  <img src="https://github.com/user-attachments/assets/eec69b39-1b89-42de-bb1b-eb5cecf5b25e" width="800"/>
</p>

hasil drop data duplikat:
<p align="center">
  <img src="https://github.com/user-attachments/assets/924ff3a4-b393-4dc2-80d3-e3400ed97646" width="800"/>
</p>

### Data Splitting
<p align="center">
  <img src="https://github.com/user-attachments/assets/eba32abc-2387-46bd-a480-124f43734f27" width="800"/>
</p>
Target pada dataset ini adalah variabel `At Risk (Binary)`. Untuk itu kedua target bawaan dataset seperti `At Risk (Binary)` dan `Stroke Risk (%)` perlu dihapus dahulu sebelum membuat model baru nantinya. Selain itu, melakukan split data dengan skema data training sebesar 80% untuk melatih model dan 20% untuk menguji model.

### Standarisasi
<p align="center">
  <img src="https://github.com/user-attachments/assets/88c495a4-0cd3-4b61-9bd9-5357faf77b9c" width="800"/>
</p>
Agar algoritma machine learning dapat bekerja secara optimal dan mencapai konvergensi lebih cepat, sangat disarankan untuk menggunakan data yang memiliki skala seragam dan distribusi mendekati normal. Proses standarisasi seperti yang dilakukan oleh StandardScaler membantu mengubah fitur data menjadi rentang yang konsisten dengan rata-rata nol dan standar deviasi satu. Hal ini sangat penting terutama ketika fitur memiliki satuan atau skala yang berbeda-beda, sehingga algoritma dapat memproses setiap fitur secara adil tanpa dipengaruhi oleh perbedaan skala.

## Modeling
### 1. XGBoost
XGBoost (Extreme Gradient Boosting) adalah salah satu algoritma yang sangat populer dan andal dalam dunia machine learning, khususnya untuk tugas klasifikasi dan regresi. XGBoost bekerja dengan membangun sejumlah decision tree secara berurutan, di mana setiap pohon baru dibentuk untuk memperbaiki kesalahan dari model sebelumnya melalui pendekatan gradient boosting. Pada implementasi model di atas, proses tuning hyperparameter dilakukan dengan menggunakan Optuna untuk memperoleh performa terbaik. Berikut penjelasan parameter utama yang digunakan dalam model akhir:

- `max_depth = 13`
Menentukan kedalaman maksimum setiap pohon keputusan. Semakin besar nilai ini, semakin kompleks pola yang dapat ditangkap oleh model, namun juga meningkatkan risiko overfitting. Nilai 13 merupakan hasil optimasi yang memberikan keseimbangan antara akurasi dan generalisasi.

- `n_estimators = 52`
Merupakan jumlah total pohon keputusan yang dibangun dalam proses boosting. Jumlah ini dikompromikan untuk menjaga performa prediksi sekaligus efisiensi waktu pelatihan. Dengan 52 estimators, model dinilai cukup dalam menangkap pola data tanpa menyebabkan overfitting.

- `learning_rate = 0.035`
Mengatur kontribusi masing-masing pohon terhadap prediksi akhir. Nilai ini termasuk rendah, yang artinya model belajar secara bertahap untuk menghindari perubahan prediksi yang drastis dan menjaga stabilitas proses pelatihan. Nilai ini dipilih dari rentang logaritmik antara 0.0001 hingga 0.1 melalui proses tuning.

- `random_state = 9`
Digunakan untuk memastikan hasil pelatihan yang konsisten dan dapat direproduksi. Dengan nilai ini, setiap proses pelatihan ulang akan menghasilkan model yang identik.

- `n_jobs = -1`
Menandakan bahwa semua core CPU yang tersedia akan digunakan selama proses pelatihan, sehingga mempercepat waktu komputasi secara signifikan.

> Model yang dihasilkan dengan kombinasi parameter ini mampu mencapai akurasi 93.57%, menunjukkan performa klasifikasi yang > sangat baik dalam mendeteksi risiko stroke berdasarkan fitur yang tersedia.

### 2. Random Forest
Random Forest adalah algoritma ensemble yang terdiri dari kumpulan pohon keputusan (decision trees), dan bertujuan untuk meningkatkan akurasi serta kestabilan prediksi dengan menggabungkan hasil dari banyak pohon. Model ini cocok digunakan untuk tugas klasifikasi dan regresi karena mampu menangani data yang kompleks serta mengurangi risiko overfitting yang biasa terjadi pada satu pohon keputusan tunggal. Berikut penjelasan dari parameter yang digunakan pada model:

- `n_estimators=100`
Parameter ini menunjukkan bahwa model akan membentuk sebanyak 100 pohon keputusan. Setiap pohon dilatih pada subset data yang berbeda, dan hasil prediksi akhir akan diperoleh melalui voting mayoritas (untuk klasifikasi). Menambahkan jumlah pohon umumnya akan meningkatkan akurasi dan stabilitas model, meskipun waktu pelatihan juga akan bertambah.

- `criterion="entropy"`
Digunakan sebagai dasar untuk membagi node dalam setiap pohon. Kriteria ini mengacu pada information gain, yaitu ukuran penurunan ketidakpastian setelah pemisahan data dilakukan. Pemilihan "entropy" sebagai kriteria pembagi bertujuan untuk membangun pohon yang lebih informatif, meskipun prosesnya sedikit lebih berat dibandingkan "gini".

- `max_depth=10`
Menetapkan batas maksimal kedalaman tiap pohon keputusan. Pembatasan ini penting untuk mencegah pohon menjadi terlalu dalam dan terlalu cocok terhadap data latih (overfitting). Dengan kedalaman maksimal 10, model diharapkan mampu menangkap pola-pola penting tanpa kehilangan kemampuan generalisasi terhadap data baru.

- `random_state=50`
Parameter ini berfungsi untuk menjaga konsistensi hasil setiap kali model dijalankan ulang. Dengan menetapkan nilai tetap, semua proses acak dalam model (seperti pemilihan subset fitur atau data) akan menggunakan seed yang sama, sehingga hasil eksperimen dapat direproduksi.

### 3. SVM
Support Vector Machine (SVM) merupakan salah satu metode supervised learning yang sering digunakan dalam tugas klasifikasi maupun regresi. Prinsip utamanya adalah menemukan hyperplane optimal yang memisahkan kelas-kelas data dengan jarak maksimum antara titik data terdekat dari masing-masing kelas terhadap garis pemisah tersebut. SVM sangat efektif untuk menangani data berdimensi tinggi dan kompleksitas yang tinggi. Pada model SVM yang digunakan ini, terdapat beberapa parameter penting:

- `kernel='rbf'`
Kernel Radial Basis Function (RBF) digunakan untuk mengubah data input ke dalam ruang berdimensi lebih tinggi sehingga memungkinkan pemisahan kelas yang tidak linear. Kernel ini sangat fleksibel dalam menangani kasus di mana batas antar kelas tidak dapat dipisahkan secara garis lurus dalam ruang aslinya.

- `random_state=42`
Parameter ini menetapkan nilai seed untuk pengacakan proses internal SVM, seperti pemilihan subset data saat pelatihan. Tujuannya adalah agar proses pelatihan model dapat menghasilkan hasil yang konsisten dan dapat diulang kembali dalam eksperimen yang sama.

### Evaluasi Hasil Perbandingan Algoritma
<p align="center">
  <img src="https://github.com/user-attachments/assets/a76c9058-c172-4285-b5c1-1001b988a7cc" width="300"/>
</p>


| **Algoritma**                    | **Kelebihan**                                                                                                                    | **Kekurangan**                                                                                   |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| **XGBoost Classifier**           | - Tingkat akurasi sangat tinggi<br>- Dilengkapi regularisasi untuk cegah overfitting<br>- Tangguh untuk data yang tidak seimbang | - Waktu pelatihan cenderung lebih lama<br>- Perlu penyesuaian parameter yang kompleks            |
| **Random Forest**                | - Dapat mengolah data non-linear dan banyak fitur<br>- Lebih tahan terhadap overfitting dibanding pohon tunggal                  | - Model sulit dijelaskan secara intuitif<br>- Butuh sumber daya komputasi besar (memori & waktu) |
| **Support Vector Machine (SVM)** | - Sangat cocok untuk data berdimensi tinggi<br>- Ideal untuk dataset kecil dengan pemisahan kelas yang jelas                     | - Tidak optimal untuk dataset besar<br>- Sensitif terhadap pilihan kernel dan parameter          |

## Evaluasi
Saya memilih model XGBoost karena proses inferensinya efisien, hasil prediksinya akurat, dan model ini lebih stabil untuk analisis prediktif. Saya menghindari SVM meskipun akurasinya mencapai lebih dari 99%, karena khawatir model tersebut mengalami overfitting.

### Confusion Matrix
Confusion matrix adalah sebuah tabel evaluasi yang digunakan untuk mengukur kinerja model klasifikasi dengan membandingkan antara nilai prediksi dan nilai aktual. Tabel ini terdiri dari empat komponen utama: True Positive (TP), True Negative (TN), False Positive (FP), dan False Negative (FN), yang membantu dalam menghitung metrik evaluasi seperti akurasi, presisi, recall, dan F1-score. Dengan melihat confusion matrix, kita dapat mengetahui jenis kesalahan yang sering dilakukan oleh model dan memperbaiki strategi klasifikasinya.

<p align="center">
  <img src="https://github.com/user-attachments/assets/6037ec0f-0c5d-4357-a02d-332f98955ee9" width="600"/>
</p>

Istilah dalam confusion matrix beserta rumus evaluasinya:
- True Positive (TP): Jumlah kasus positif yang berhasil diprediksi dengan benar sebagai positif oleh model.
- False Positive (FP): Jumlah kasus yang sebenarnya negatif, namun secara keliru diklasifikasikan sebagai positif (juga dikenal sebagai kesalahan Tipe I).
- True Negative (TN): Jumlah kasus negatif yang tepat diprediksi sebagai negatif.
- False Negative (FN): Jumlah kasus positif yang salah diklasifikasikan sebagai negatif (disebut juga kesalahan Tipe II).

Berdasarkan keempat komponen tersebut, berikut metrik evaluasi yang bisa dihitung:
- Akurasi = (TP + TN) / (TP + TN + FP + FN) → Menunjukkan seberapa besar proporsi prediksi yang tepat dibandingkan dengan keseluruhan prediksi.
- Presisi (Precision) = TP / (TP + FP) → Mengukur tingkat ketepatan model saat menyatakan suatu data termasuk dalam kelas positif.
- Recall (Sensitivitas) = TP / (TP + FN) → Menggambarkan sejauh mana model mampu menemukan semua data yang benar-benar positif.
- F1 Score = 2 × (Precision × Recall) / (Precision + Recall) → Menyediakan rata-rata harmonis antara presisi dan recall, terutama berguna dalam kasus ketidakseimbangan kelas.

Contoh Kasus:
1. XGBoost
<p align="center">
  <img src="https://github.com/user-attachments/assets/155a8c62-6b6f-4a1f-8d78-a3996832024e" width="500"/>
</p>

**Insight**:

- True Negatives (TN): 8672 — model dengan benar mengenali orang yang tidak berisiko stroke.
- True Positives (TP): 4237 — model dengan benar mengenali orang yang berisiko stroke.
- False Negatives (FN): 285 — orang yang seharusnya berisiko stroke tapi model tidak mengenalinya → ini paling krusial karena bisa fatal.
- False Positives (FP): 602 — orang yang tidak berisiko stroke tapi dikira berisiko → lebih dapat diterima dibanding FN

3. Random Forest
<p align="center">
  <img src="https://github.com/user-attachments/assets/fe564f87-a2d5-4936-8962-9d856067ff0a" width="500"/>
</p>

**Insight:**
- False Positives (FP): 677 — orang yang tidak berisiko stroke tapi model menganggap mereka berisiko.
- False Negatives (FN): 431 — orang yang sebenarnya berisiko stroke tapi tidak terdeteksi (lebih berbahaya secara medis).
- True Positives (TP): 4126 dan True Negatives (TN): 8526 menunjukkan model cukup baik menangani kedua kelas.

5. SVM
<p align="center">
  <img src="https://github.com/user-attachments/assets/a7dabb41-dab6-4d33-a348-29d03725d8e5" width="500"/>
</p>

**Insight:**
- False Positive (78): Sebanyak 78 orang yang sebenarnya tidak berisiko diprediksi berisiko. Ini bisa berdampak ke over-treatment, tapi relatif tidak berbahaya.
- False Negative (56): Sebanyak 56 orang yang sebenarnya berisiko diprediksi tidak berisiko. Ini adalah kesalahan yang lebih serius karena bisa menyebabkan keterlambatan penanganan.
- True Negative (TN): Sebanyak 8901 orang yang
Artinya orang tersebut memang tidak berisiko terkena stroke, dan model benar memprediksi mereka sebagai tidak berisiko.
- True Positive (TP): Sebanyak 4761 orang yang memang berisiko terkena stroke, dan model berhasil mengklasifikasikan mereka dengan benar.

## Kesimpulan 
### 1. Faktor-faktor apa saja yang paling berkontribusi terhadap risiko seseorang mengalami stroke?
<p align="center">
  <img src="https://github.com/user-attachments/assets/0ade5f97-ae3d-4c1e-9f07-ce39049fb9f4" width="600"/>
</p>

**Insight:** Faktor yang paling berkontribusi seseorang mengalami Stroke adalah Faktor `Umur`(Age).

### 2. Bagaimana model Machine Learning dapat memprediksi apakah seseorang berpotensi terkena stroke berdasarkan kondisi yang mereka input?
<p align="center">
  <img src="https://github.com/user-attachments/assets/58aca2fe-d508-4197-be3a-792b5ec71df7" width="600"/>
</p>

 Selanjutnya yaitu mencoba model inference dari XGBoost

<p align="center">
  <img src="https://github.com/user-attachments/assets/f5e9941a-4d69-42a5-acad-f80d8c32b266" width="600"/>
</p>


**Insight:**
Berdasarkan data yang sduah saya coba inputkan, model memprediksi bahwa Anda berisiko mengalami stroke. Prediksi ini didasarkan pada beberapa gejala yang dilaporkan, antara lain nyeri dada, sesak napas, kelelahan, pusing, nyeri di leher, rahang, bahu, atau punggung, keringat berlebih, batuk terus-menerus, tekanan darah tinggi, ketidaknyamanan di dada saat beraktivitas, sleep apnea, dan kecemasan berlebihan. 

Gejala-gejala tersebut merupakan indikator umum yang sering dikaitkan dengan peningkatan risiko stroke dan kondisi kardiovaskular lainnya. Meskipun model ini telah dilatih dengan data klinis dan menunjukkan akurasi prediksi diaatas 90%, hasil ini bukanlah diagnosis medis. Oleh karena itu, sangat disarankan untuk segera berkonsultasi dengan tenaga medis profesional guna mendapatkan pemeriksaan lebih lanjut dan penanganan yang tepat. Deteksi dan intervensi dini sangat penting untuk mencegah komplikasi lebih lanjut yang dapat membahayakan kesehatan Anda.














