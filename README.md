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
2.   Apakah terdapat hubungan antara gejala (seperti nyeri dada, sesak napas, detak jantung tidak teratur, kelelahan, dan lainnya) dengan risiko stroke pada pasien?

### Goals
1. Mengidentifikasi faktor-faktor utama yang berkontribusi terhadap risiko seseorang mengalami stroke, berdasarkan atribut seperti usia dan berbagai gejala klinis (contoh: nyeri dada, sesak napas, detak jantung tidak teratur, dan lainnya).
2. Menganalisis hubungan antara gejala yang dialami pasien dengan kemungkinan risiko stroke.

### Solution statements
Untuk menjawab permasalahan yang telah dirumuskan, solusi yang diusulkan dalam proyek ini adalah melakukan analisis data berdasarkan riwayat kesehatan dan gejala yang dialami pasien. Langkah-langkah utama dalam solusi ini meliputi:

1. Eksplorasi data (Exploratory Data Analysis) untuk memahami distribusi variabel, mendeteksi pola-pola penting, dan mengidentifikasi hubungan awal antara gejala, kondisi kesehatan, serta faktor risiko dengan kemungkinan terjadinya stroke.
2. Penerapan inference untuk menentukan gejala dan faktor mana yang paling signifikan dalam mempengaruhi risiko stroke.

## Data Understanding
Tahap ini merupakan proses analisis data yang bertujuan untuk memperoleh pemahaman yang menyeluruh mengenai dataset sebelum melanjutkan ke tahap analisis lebih lanjut.

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
| At Risk                     | int64     | Status risiko stroke (1 = berisiko, 0 = tidak)              |
| Stroke Risk (%)             | Float      | Estimasi probabilitas terjadinya stroke dalam persen (0 - 100%) |


### Exploratory Data Analysis - Univariate Analysis
<p align="center">
  <img src="https://github.com/user-attachments/assets/9bf9d843-192a-4859-a59e-c26b4542adb4" width="1000"/>
</p>
