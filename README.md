# Laporan Proyek Machine Learning - Muh Farhan

## Domain Proyek

Dunia digital kini semakin mudah diakses oleh anak-anak, dengan aplikasi seluler memainkan peran yang signifikan dalam mendukung kebutuhan hiburan, pendidikan, serta interaksi sosial mereka. Namun, kemudahan akses ini juga menghadirkan tantangan serius, khususnya terkait dengan pengumpulan dan pemanfaatan data pribadi anak. Anak-anak, yang secara kognitif masih dalam tahap perkembangan, kerap kali belum memahami sepenuhnya risiko dari membagikan informasi pribadi seperti nama, alamat, atau nomor telepon. Akibatnya, mereka menjadi kelompok yang sangat rentan terhadap pelanggaran privasi serta penyalahgunaan data oleh pihak-pihak yang tidak bertanggung jawab (Widyaningsih dan Suryaningsih, 2022). Ancaman ini semakin meningkat karena data pribadi yang diperoleh melalui aplikasi dapat dimanfaatkan untuk tujuan yang tidak selalu etis—mulai dari penargetan iklan, manipulasi perilaku digital, hingga eksploitasi dan pencurian identitas (Fa’izi, 2024).

Penelitian sebelumnya menunjukkan bahwa, khususnya di Indonesia, belum terdapat regulasi khusus yang secara menyeluruh mengatur perlindungan data pribadi anak di ruang digital. Hal ini menyebabkan perlindungan hukum terhadap hak-hak privasi anak masih sangat terbatas dan kurang memadai (Widyaningsih dan Suryaningsih, 2022). Sebaliknya, di Amerika Serikat, Undang-Undang Perlindungan Privasi Online Anak (Children’s Online Privacy Protection Act atau COPPA) telah menjadi acuan penting yang mewajibkan pengembang aplikasi untuk memperoleh izin orang tua sebelum mengumpulkan data dari pengguna berusia di bawah 13 tahun. Regulasi serupa kini mulai diadopsi oleh berbagai negara sebagai bagian dari upaya global untuk memperkuat perlindungan anak di dunia maya. Pentingnya perlindungan ini semakin ditekankan oleh tingginya angka kasus pelanggaran privasi dan kejahatan daring yang menargetkan anak-anak, seperti cyberbullying, pelecehan seksual online, dan paparan terhadap konten berbahaya. Semua ini dapat membawa dampak serius terhadap perkembangan mental, emosional, dan sosial anak (Lyandra, 2025).

Mengingat berbagai ancaman tersebut, isu perlindungan data pribadi anak di era digital menjadi semakin mendesak untuk ditangani. Upaya perlindungan ini tidak hanya bertujuan untuk menjaga keamanan dan privasi anak-anak, tetapi juga untuk memastikan bahwa mereka dapat mengakses dan memanfaatkan teknologi secara sehat, aman, dan produktif, tanpa terpapar risiko yang mengancam kesejahteraan mereka secara jangka panjang (Tobing, 2022). Salah satu pendekatan yang potensial untuk mengatasi permasalahan ini adalah penerapan predictive analytics. Metode ini memungkinkan identifikasi karakteristik aplikasi digital yang berpotensi membahayakan anak, sehingga dapat digunakan sebagai dasar pengambilan keputusan untuk melakukan intervensi terhadap aplikasi-aplikasi yang tidak ramah anak.

Dalam konteks penelitian ini, penulis menerapkan tiga model pembelajaran mesin berbasis boosting, yaitu CatBoost, XGBoost, dan LightGBM. Model-model boosting dikenal memiliki keunggulan dalam menangani data yang kompleks, meningkatkan akurasi prediksi, serta mampu mengurangi bias dan variance secara efektif. Ketiga model ini dirancang untuk memperkuat performa klasifikasi dengan menggabungkan sejumlah weak learners menjadi satu strong learner, sehingga sangat cocok digunakan dalam konteks evaluasi risiko terhadap aplikasi digital. Dari ketiga model tersebut, akan dipilih satu model dengan performa terbaik, yang diharapkan mampu menghasilkan prediksi yang akurat. Hasil ini nantinya dapat menjadi landasan penting bagi para pemangku kepentingan, termasuk pemerintah, dalam mengambil kebijakan serta tindakan yang tepat untuk melindungi hak-hak anak di dunia digital.

## Business Understanding

Berdasarkan latar belakang yang diuraikan di atas, problem statements dari projek ini adalah sebagai berikut:

### Problem Statements

- Belum adanya regulasi komprehensif di Indonesia yang secara khusus melindungi data pribadi anak dalam aplikasi digital menyebabkan anak-anak rentan terhadap pelanggaran privasi dan penyalahgunaan data pribadi.
- Kurangnya kesadaran anak terhadap bahaya membagikan data pribadi secara daring meningkatkan risiko eksploitasi, namun belum banyak pendekatan berbasis teknologi yang digunakan untuk mengidentifikasi aplikasi digital yang berpotensi membahayakan mereka.
- Belum tersedia metode analitis yang mampu secara otomatis mengidentifikasi karakteristik aplikasi yang tidak ramah anak berdasarkan data yang tersedia, sehingga pihak berwenang kesulitan dalam melakukan pemantauan berbasis bukti.
- Masih minimnya pemanfaatan model pembelajaran mesin dalam konteks perlindungan anak secara preventif, khususnya dalam memetakan potensi risiko dari aplikasi seluler yang mudah diakses oleh anak-anak.

### Goals

Berdasarkan problem statements yang diuraikan di atas, goals dari pojek ini adalah sebagai berikut:
- Mengembangkan model prediktif berbasis pembelajaran mesin untuk mengidentifikasi aplikasi yang berpotensi tidak ramah anak berdasarkan karakteristik aplikasinya.
- Mengevaluasi dan membandingkan performa tiga algoritma boosting—CatBoost, XGBoost, dan LightGBM—dalam mengklasifikasikan aplikasi digital yang berisiko bagi anak-anak.
- Memberikan pendekatan berbasis data untuk mendukung pengambilan keputusan oleh pihak-pihak berwenang dalam rangka memperkuat perlindungan anak di ranah digital.
- Mengukur performa model menggunakan metrik evaluasi yang terstandar seperti akurasi, precision, recall, F1-score, AUC, dan balance accuracy guna memastikan keandalan hasil prediksi.

### Solution statements
- Menggunakan algoritma boosting (CatBoost, XGBoost, LightGBM) sebagai pendekatan utama dalam pengembangan model klasifikasi, karena kemampuannya dalam menangani data kompleks dan meningkatkan akurasi prediksi.
- Melatih dan menguji model menggunakan dataset aplikasi yang telah diberi label berdasarkan tingkat keamanan terhadap anak-anak, untuk memperoleh pemetaan risiko yang representatif.
- Melakukan evaluasi performa masing-masing model dengan metrik seperti akurasi, precision, recall, F1-score, dan AUC guna menentukan model dengan kinerja terbaik dan paling andal.
- Model dengan performa tertinggi akan dijadikan acuan untuk pengklasifikasian aplikasi digital yang aman atau tidak aman bagi anak, sehingga hasilnya dapat dimanfaatkan sebagai bahan pertimbangan dalam penyusunan regulasi atau kebijakan pengawasan aplikasi.

## Data Understanding
Dataset yang digunakan pada projek ini dapat diakses pada tautan berikut:

[Kaggle](https://www.kaggle.com/datasets/frhaan/coppa-risk-dataset)

Dataset ini berisi informasi yang diambil dari major app marketplace, bersama dengan fitur turunan yang terkait dengan privasi dan kepatuhan. Dataset ini mencakup campuran fitur kategorikal, numerik, dan boolean. Nilai yang hilang diwakili oleh string kosong.

Dataset ini terdiri dari 7000 observasi dan 17 fitur (5 fitur numerik, 1 fitur boolean yaitu fitur target, dan 11 fitur kategorikal) dengan rincian sebagai berikut:
![deskripsi-fitur](https://github.com/user-attachments/assets/99abd120-0c36-45fc-aaa5-22720d5a631e)


### Variabel-variabel pada dataset yang digunakan adalah sebagai berikut:
- **`developerCountry`**: Negara tempat developer aplikasi terdaftar. Ini bisa memberikan wawasan tentang kesadaran dan penerapan hukum privasi di wilayah tersebut. Nilai seperti "ADDRESS NOT LISTED IN PLAYSTORE" dan "CANNOT IDENTIFY COUNTRY" menunjukkan data yang hilang atau tidak dapat diambil.
- **`countryCode`**: Pasar atau wilayah target dari aplikasi (misalnya, GLOBAL, NA, EMEA, LATAM, APAC). NA kemungkinan berarti North America. GLOBAL adalah kategori umum, sedangkan yang lain lebih spesifik secara geografis.
- **`userRatingCount`**: Jumlah total rating yang diberikan pengguna terhadap aplikasi.
- **`primaryGenreName`**: Kategori utama tempat aplikasi tersebut terdaftar (misalnya, Games, Books & Reference, Education, dll.).
- **`Downloads`**: Perkiraan jumlah unduhan aplikasi dalam bentuk rentang (misalnya, "100000 - 500000").
- **`deviceType`**: Jenis perangkat yang kompatibel dengan aplikasi (misalnya, smartphone, tablet, connected-tv/ott, undetermined).
- **`hasPrivacyLink`**: Menunjukkan apakah daftar aplikasi mencantumkan tautan ke kebijakan privasi. Keberadaan tautan ini merupakan langkah awal dalam kepatuhan.
- **`hasTermsOfServiceLink`**: Menunjukkan apakah aplikasi menyediakan tautan ke Terms of Service.
- **`hasTermsOfServiceLinkRating`**: Rating (misalnya, "low", "medium", "high") yang kemungkinan menunjukkan kualitas atau kelengkapan dari Terms of Service tersebut.
- **`isCorporateEmailScore`**: Skor (kemungkinan antara 0 sampai 100) yang menunjukkan seberapa besar kemungkinan email developer merupakan email korporat dibandingkan email pribadi. Skor yang lebih tinggi bisa menunjukkan developer yang lebih profesional dan mungkin lebih patuh terhadap kebijakan privasi.
- **`adSpent`**: Jumlah uang yang dikeluarkan untuk iklan.
- **`appAge`**: Usia aplikasi dalam satuan hari (kemungkinan sejak aplikasi dirilis di app store). Aplikasi yang lebih tua mungkin lebih jarang diperbarui mengikuti praktik privasi terbaru.
- **`averageUserRating`**: Rata-rata rating pengguna terhadap aplikasi (misalnya, skala 1 sampai 5).
- **`appContentBrandSafetyRating`**: Rating (misalnya, "low", "medium", "high") yang mencerminkan kesesuaian konten aplikasi untuk audiens umum. Ini tidak langsung berkaitan dengan privasi, tetapi lebih ke moderasi konten.
- **`appDescriptionBrandSafetyRating`**: Rating kategorikal yang mirip dengan di atas, tetapi khusus mengevaluasi deskripsi aplikasi, bukan aplikasinya secara langsung.
- **`mfaRating`**: Rating kategorikal (misalnya, "low", "medium", "high") yang kemungkinan berhubungan dengan "Made for Advertising Apps" (aplikasi yang dirancang untuk tujuan iklan).
- **`coppaRisk`**: Variabel target yang menunjukkan apakah aplikasi ini berisiko tidak mematuhi aturan COPPA (Children’s Online Privacy Protection Act).

### Exploratory Data Analysis
Untuk memahami data yang digunakan pada projek ini, dilakukan exploratory data analysis sebagai berikut:

#### Distribusi Variabel Target (CoppaRisk)
![distribusi-target-copparisk](https://github.com/user-attachments/assets/db0a1d3c-bced-404e-a490-cd542bc7e039)

Berdasarkan visualisasi di atas, terlihat bahwa dataset yang dimiliki termasuk imbalance data.

#### Distirbusi Fitur Numerik
![distribusi fitur numerik](https://github.com/user-attachments/assets/acbfa756-da96-4b63-8da5-2ae7ab1cdd9b)

Berdasarkan visualisasi di atas, terlihat bahwa sebagian besar aplikasi memiliki jumlah rating pengguna yang sangat sedikit, dengan sedikit outlier yang sangat tinggi, menunjukkan ketimpangan popularitas aplikasi. Skor email korporat (`isCorporateEmailScore`) menunjukkan distribusi bimodal, yang mengindikasikan adanya dua kelompok developer yang dominan: individu (skor rendah) dan korporat (skor tinggi). Usia aplikasi (`appAge`) didominasi oleh aplikasi yang masih relatif baru, dengan tren penurunan jumlah aplikasi seiring bertambahnya usia. Rata-rata rating pengguna (`averageUserRating`) menunjukkan bahwa banyak aplikasi yang tidak memiliki rating sama sekali atau justru memiliki rating sangat tinggi, mencerminkan potensi bias dalam penilaian pengguna. Pola distribusi ini penting untuk dipertimbangkan dalam analisis lebih lanjut karena dapat memengaruhi hasil pemodelan dan interpretasi risiko COPPA.

#### Korelasi Linier Fitur Numerik
![analisis-korelasi-fitur-numerik](https://github.com/user-attachments/assets/ce3dcd56-ea85-4627-a95f-01b43ec37e71)

Berdasarkan heatmap korelasi fitur yang ditampilkan, terlihat bahwa tidak ada korelasi yang kuat antara fitur-fitur numerik yang dianalisis. Semua nilai korelasi berada dalam rentang yang sangat lemah (antara -0.11 hingga 0.12), menunjukkan bahwa masing-masing fitur cenderung saling independen. Misalnya, `userRatingCount`, `appAge`, dan `averageUserRating` hanya memiliki korelasi lemah satu sama lain, dan `isCorporateEmailScore` menunjukkan korelasi negatif lemah terhadap `averageUserRating`. Hal ini menunjukkan bahwa setiap fitur mungkin memberikan informasi unik dan tidak redundant, sehingga tetap relevan untuk dipertimbangkan secara individual dalam analisis lanjutan seperti pemodelan prediktif terhadap risiko COPPA.

#### Distribusi Fitur Kategorik Berdasarkan Variabel Target
##### Fitur `downloads_category_label`
![downloads_category_label](https://github.com/user-attachments/assets/6a763071-e533-4f93-97d3-5c8b01f488e0)

Berdasarkan visualisasi di atas, terlihat bahwa aplikasi dengan risiko COPPA (`coppaRisk = True`) tersebar di seluruh kategori unduhan, namun cenderung lebih banyak ditemukan pada kategori `Very High` dan `High`. Ini mengindikasikan bahwa aplikasi dengan jumlah unduhan tinggi lebih rentan memiliki risiko terhadap kepatuhan aturan COPPA, mungkin karena cakupan pengguna yang luas termasuk anak-anak. Sementara itu, sebagian besar aplikasi secara umum berada pada kategori `Very Low`, namun hanya sebagian kecil dari mereka yang berisiko COPPA. Temuan ini dapat menjadi indikasi bahwa popularitas aplikasi (berdasarkan jumlah unduhan) mungkin berperan dalam meningkatkan risiko terhadap regulasi privasi anak-anak.
##### Fitur `deviceType`
![deviceType](https://github.com/user-attachments/assets/6176eecf-e024-40f6-8976-6cb44ef3464a)

Berdasarkan visualisasi di atas, dapat disimpulkan bahwa sebagian besar aplikasi, baik yang berisiko COPPA maupun tidak, berada dalam kategori `GLOBAL`, yang kemungkinan menunjukkan aplikasi yang kompatibel lintas perangkat. Namun, secara proporsional, kategori `tablet` dan `smartphone` menunjukkan kehadiran yang relatif lebih tinggi dari aplikasi berisiko COPPA dibandingkan dengan kategori lainnya. Hal ini bisa mencerminkan bahwa perangkat yang lebih sering digunakan oleh anak-anak, seperti tablet dan smartphone, lebih rentan terhadap risiko pelanggaran aturan COPPA. Sementara itu, perangkat seperti `connected-tv/ott` dan `undetermined` hampir tidak memiliki representasi aplikasi dengan risiko COPPA.
##### Fitur `hasPrivacyLink`
![hasPrivacyLink](https://github.com/user-attachments/assets/1c16f95c-dc4d-4dd3-a893-1e9da76b29bb)

Berdasarkan visualisasi di atas, tampak bahwa sebagian besar aplikasi yang terdeteksi memiliki risiko COPPA (`coppaRisk=True`) justru memiliki tautan kebijakan privasi (`hasPrivacyLink=True`). Meskipun demikian, aplikasi yang tidak memiliki tautan kebijakan privasi (`hasPrivacyLink=False`) hampir seluruhnya tidak termasuk dalam kategori berisiko. Hal ini menunjukkan bahwa keberadaan tautan kebijakan privasi bukanlah jaminan bahwa aplikasi tersebut bebas dari risiko COPPA, dan kemungkinan besar hanya menjadi bagian dari formalitas kepatuhan tanpa implementasi nyata terhadap perlindungan data anak.
##### Fitur `appDescriptionBrandSafetyRating`
![appDescriptionBrandSafetyRating](https://github.com/user-attachments/assets/4d85839c-bec8-444e-98ad-46024007e921)

Berdasarkan visualisasi di atas, dapat disimpulkan bahwa sebagian besar aplikasi dengan risiko COPPA (`coppaRisk=True`) memiliki nilai brand safety yang rendah (`low`). Jumlah aplikasi berisiko dengan rating `medium` dan `high` sangat kecil, hampir tidak signifikan. Hal ini menunjukkan bahwa aplikasi dengan deskripsi yang dinilai kurang aman secara brand safety lebih berpotensi memiliki risiko terhadap kepatuhan COPPA. Dengan kata lain, rendahnya kualitas atau kehati-hatian dalam deskripsi aplikasi bisa menjadi indikator awal adanya risiko terhadap privasi anak. Ini dapat menjadi sinyal penting dalam proses penyaringan atau klasifikasi awal aplikasi untuk tujuan moderasi atau pengawasan.
##### Fitur `mfaRating`
![mfaRating](https://github.com/user-attachments/assets/5ce3fc73-9e66-45cd-b4db-eeb58ba2cea6)

Berdasarkan visualisasi di atas, dapat disimpulkan bahwa hampir semua aplikasi, baik yang memiliki risiko COPPA (`coppaRisk=True`) maupun tidak (`coppaRisk=False`), memiliki nilai `mfaRating` pada kategori *low*. Kategori `medium` dan `high` hampir tidak muncul dalam distribusi ini, menunjukkan bahwa mayoritas aplikasi yang dianalisis memiliki tingkat keamanan MFA (Multi-Factor Authentication) yang rendah. Hal ini mengindikasikan bahwa rendahnya tingkat keamanan otentikasi tidak serta-merta menjadi pembedaan signifikan terhadap risiko COPPA. Namun, tetap perlu dicatat bahwa semua aplikasi berisiko (`coppaRisk=True`) hanya berada di kategori `low`, yang bisa menunjukkan adanya potensi kontribusi dari faktor keamanan rendah terhadap risiko pelanggaran privasi anak.

## Data Preparation
Teknik data preparation yang diterapkan pada projek ini diuraikan sebagai berikut:
### Penyesuaian Nilai Fitur `developerCountry`
Ketika dilakukan inspeksi nilai pada setiap fitur yang ada pada dataset, didapati beberapa ketidaksesuaian. Misalnya, pada fitur  `developerCountry` yang seharusnya berisi nama-nama negara ternyata mengandung nilai yang tidak merujuk atau tidak merepresentasikan nama negara seperti 'ADDRESS NOT LISTED IN PLAYSTORE', 'CANNOT IDENTIFY COUNTRY', 'STATUTORY MASKING ENABLED', 'PERSONAL DATA, CAN NOT BE PUBLICLY DISCLOSED ACCORDING TO APPLICABLE LAWS.'. Oleh karena itu, penyesuaian dilakukan dengan mengubah nilai-nilai tersebut menjadi missing value dan akan diimputasi nantinya.
### Penyesuaian Nilai Fitur `downloads`
Nilai asli dari fitur `downloads` adalah range angka. Nmaun, range angka tersebut relatif tersebar secara acak (tidak baku) dan memiliki variasi yang sangat tinggi. Untuk dilakukan pengkategorian ulang agar diperoleh kategori yang lebih relevan dan sederhana. Nilai acuan yang digunakan untuk membentuk kategori baru tersebut adalah rata-rata dari nilai minimum dan nilai maksimum pada setiap rannge. Kemudian diterapkan penentuan kategori berdasarkan rules berikut ini:
- mean <= 100 -> very_low
- mean <= 1000 -> low
- mean <= 10000 -> moderate
- mean <= 100000 -> high
- mean > 100000 -> very_high
### Penyederhanaan Fitur `countryCode`
Nilai asli dari fitur `countryCode` adalah nama-nama negara dengan variasi yang sangat tinggi. Untuk itu, dilakukan penyederhanaan kategori dengan harapan model dapat lebih mudah menemukan pola dalam proses training nantinya. Proses penyederhanaan pola didasarkan pada nilai true ratio atau rasio jumlah observasi yang dikategorikan true pada fitur `coppaRisk` pada setiap country code dengan jumlah seluruh observasi pada tiap-tiap country code yang bersesuaian. Setelah penghitungan true ratio dilakuan, berikutnya dibuat visualisasi distribusi dari true ratio per country code yang hasilnya adalah sebagai berikut:
![true-ratio-per-country-code](https://github.com/user-attachments/assets/5ccd8785-bc4c-43c2-9afd-448f7efaf616)

Berdasarkan visualisasi di atas, berikutnya dapat disusun rules cutoff penyederhanaan kategori sebagai berikut:

if true_ratio > 33.33 and total > 11:
- high_risk_country

else if total < 2:
- rare_country

else:
- low_risk_country
### Penyederhanaan Fitur `primaryGenreName`
Penyederhanaan nilai fitur `primaryGenreName` dilakukan karena nilai asli dari fitur tersebut memiliki variasi yang sangat tinggi dan dikhawatirkan akan membuat model sulit untuk mengekstrak pola untuk keperluan klasifikasi nantinya. Proses penyederhanaan kategori untuk fitur ini persis sama dengan proses penyederhanaan kategori pada fitur `countryCode` sebelumnya. Namun, khusus untuk fitur `primaryGenreName` ini, diperoleh visualisasi distribusi frekuensi true ratio sebagai berikut:
![true-ratio-primary-genre-name](https://github.com/user-attachments/assets/1354319c-9bbd-4ba7-be86-c2b8777eb035)

Berdasarkan visualisasi di atas, berikutnya dapat disusun rules cutoff penyederhanaan kategori sebagai berikut:

if true_ratio > 2.48 and total > 191:
- high_risk_genre

else if total < 22:
- rare_genre

else:
- low_risk_genre
### Penyederhanaan Fitur `downloads_category_label`
Kategori asli pada fitur ini adalah very_low, very_high, moderate, low, dan high. Namun karena kategori moderate, low, dan high memiliki pola dan frekuensi yang relatif sama, ketiga kategori tersebut digabungkan untuk membentuk satu kategori baru bernama "mid".
### Penyederhanaan Fitur `deviceType`
Kategori asli pada fitur ini adalah smartphone, global, tablet, connected-tv/ott, dan undetermined. Kategori ini dirasa terlalu boros karena terdapat dua kategori berbeda yang memiliki karakteristik relatif sama yatu smartphone dan tablet, sehingga kedua kategori tersebut digabungkan untuk membentuk satu kategori baru yaitu "mobile". Di satu sisi, karena frekuensi kategori connected-tv/ott dan undetermined sangat sedikit jika dibandingkan dengan kategori lainnya maka kedua kategori tersebut digabungkan untuk membentuk satu kategori baru berupa "others".
### Splitting Data
Pada projek ini splitting data dilakukan dengan proporsi 80% untunk training dan 20% untuk testing. Kemudian proses splitting dilakukan secara stratified untuk memastikan keterwakilan tiap-tiap kelas pada training set dan testing set karena data yang dimiliki termasuk imbalance data.
### Treatment Missing Value
Pada projek ini, treatment missing value dilakukan dengan tiga cara, masing-masing diuraikan sebagai berikut:
1. Penghapusan fitur
   Penghapusan fitur dilakukan pada fitur-fitur yang memiliki missing value > 60%. Hal ini dilakukan karena fitur dengan missing value yang tinggi dalam prosesnya sulit untuk diimputasi atau dapat menghasilkan nilai hasil imputasi yang tidak relevan.
2. Penghapusan observasi missing
   Penghapusan observasi missing dilakukan pada fitur yang memiliki missing value < 1%. Hal ini dilakukan karena penghapusan observasi missing pada fitur yang memiliki missing value dengan jumlah rendah dianggap tidak akan memberikan perubahan yang signifikan pada proses pemodelan nantinya.
3. Imputasi
   Imputasi dilakukan pada fitur-fitur yang tidak masuk pada opsi pertama dan opsi kedua di atas. Dalam hal ini imputasi dilakukan menggunakan **iterative imputer** yang menggunakan semua fitur lainnya (yang tersedia) sebagai input untuk memprediksi nilai yang hilang tersebut, dengan model regresi seperti BayesianRidge. Proses tersebut dilakuan secara iteratif dengan memperbarui estimasi nilai hilang pada setiap iterasinya hingga konvergen atau mencapai jumlah iterasi maksimum. Metode ini lebih akurat dibanding imputasi sederhana karena mempertimbangkan hubungan antar fitur dan dapat menangani dataset dengan banyak missing value.
   Dalam menerapkan imputasi, fitur-fitur yang dimiliki terlebih dahulu dipisahkan menjadi tiga tipe: nominal, ordinal, dan numerik. Fitur ordinal diencoding menggunakan OrdinalEncoder dengan urutan kategori yang ditentukan secara eksplisit, fitur nominal diubah menggunakan OneHotEncoder, sedangkan fiturnumerik tetap dibiarkan dalam representasi numeriknya. Setelah semua fitur kategorikal dikonversi ke bentuk numerik, data digabungkan dan dilakukan imputasi nilai hilang menggunakan IterativeImputer (dilatih hanya pada data training untuk menghindari data leakage). Terakhir, hasil imputasi dikembalikan ke bentuk semula (inverse transform) untuk memastikan interpretabilitas dan konsistensi data sebelum digunakan dalam pelatihan model. **Sebagai catatan, encoding variabel kategorikal yang dilakukan pada tahap ini semata-mata hanya diperuntukkan untuk proses imputasi missing value. Karena proses imputasi missing value hanya bisa dilakukan ketika seluruh fitur berada dalam format numerik. Nantinya akan dilakukan encoding variabel kategorikal lagi dengan mekanisme yang sama khusus untuk proses pemodelan**.
### Encoding Variabel Kategorikal
Proses encoding fitur kategorikal dilakukan dengan memperhatikan jenis fitur kategorik itu sendiri. Fitur kategorikal yang bertipe nominal di-encode menggunakan One-Hot Encoder, sedangkan fitur kategorikal yang bertipe ordinal di-encode menggunakan Ordinal Encoder. Hal ini dilakukan agar model machine learning dapat memahami dan memproses data kategorikal dengan benar sesuai dengan sifat dan hubungan antar kategori yang dimilikinya, sehingga meningkatkan akurasi dan performa model secara keseluruhan.

## Modeling
Secara umum pada tahap pemodelan ini, langkah-langkah yang dilakukan adalah sebagai berikut:
- Menerapkan mekanisme cost-sensitive learning dengan menghitung bobot kelas (class weights) secara otomatis berdasarkan distribusi kelas pada label target y. Ini berguna terutama ketika data tidak seimbang (class imbalance), agar model machine learning tidak bias terhadap kelas mayoritas. Dalam hal ini, class weight dihitung menggunakan formula berikut ini:
![formula-class-weight](https://github.com/user-attachments/assets/4e9ba2bc-f769-4070-bfda-1447826726bc)
- Hyperparameter tuning menggunakan framework Optuna.

  Optuna adalah sebuah pustaka Python open-source yang digunakan untuk mengotomatisasi proses pencarian hyperparameter terbaik dalam pelatihan model machine learning. Cara kerja Optuna didasarkan pada pendekatan "define-by-run", yang memungkinkan pengguna untuk mendefinisikan pencarian hyperparameter secara dinamis dalam fungsi Python. Di dalam fungsi ini, pengguna menggunakan objek trial untuk menyarankan nilai-nilai hyperparameter (seperti learning rate, jumlah neuron, atau batch size), kemudian menjalankan pelatihan model dan mengembalikan metrik evaluasi seperti akurasi atau loss. Optuna kemudian melakukan proses optimasi secara iteratif dengan tujuan memaksimalkan atau meminimalkan nilai objektif tersebut, tergantung pada arah optimasi yang ditentukan.

  Secara internal, Optuna menggunakan algoritma optimasi berbasis probabilistik, yaitu Tree-structured Parzen Estimator (TPE), yang secara cerdas mengeksplorasi ruang pencarian dengan memanfaatkan hasil dari percobaan sebelumnya untuk memperkirakan kombinasi hyperparameter yang lebih menjanjikan. Pada tahap awal, beberapa percobaan dilakukan secara acak, kemudian hasilnya dianalisis untuk membedakan mana kombinasi yang menghasilkan performa baik dan yang buruk. Berdasarkan analisis tersebut, model probabilistik dibentuk untuk memandu pencarian pada iterasi berikutnya, sehingga proses pencarian menjadi lebih efisien dibandingkan metode konvensional seperti Grid Search atau Random Search.
- Evaluasi pada data validation.
- Feature selection berdasarkan feature importance.

Penjelasan mengenai algoritma yang digunakan diuraikan sebagai berikut:
### 1. CatBoost Classifier
CatBoostClassifier adalah model klasifikasi berbasis gradient boosting yang merupakan bagian dari framework CatBoost, dikembangkan oleh Yandex. Model ini dirancang khusus untuk menangani data dengan fitur kategorikal secara efisien tanpa perlu preprocessing seperti one-hot encoding atau label encoding manual. Dalam projek ini, hyperparameter yang digunakan untuk model CatBoost classifier adalah sebagai berikut:
- 'depth': trial.suggest_int('depth', 4, 10),
- 'learning_rate': trial.suggest_loguniform('learning_rate', 0.01, 0.3),
- 'n_estimators': trial.suggest_int('n_estimators', 1000, 3000),
- 'min_child_samples': trial.suggest_int("min_child_samples", 5, 20),
- 'subsample': trial.suggest_uniform("subsample", 0.5, 1.0),
- 'l2_leaf_reg': trial.suggest_loguniform('l2_leaf_reg', 1, 10),
- 'loss_function': 'Logloss',
- 'bootstrap_type': 'Bernoulli',
- 'class_weights': class_weights_dict,
- 'border_count': trial.suggest_int('border_count', 32, 255),
- 'random_strength': trial.suggest_float('random_strength', 1, 20),
- 'random_seed': 42,
- 'task_type': 'GPU',
- 'verbose': 0
Parameter-parameter di ataslah yang digunakan dalam proses hyperparameter tuning menggunakan Optuna.
#### Cara Kerja
CatBoostClassifier bekerja dengan prinsip dasar gradient boosting, yaitu membangun model prediktif secara bertahap dengan menggabungkan banyak pohon keputusan (decision trees), di mana setiap pohon baru dilatih untuk memperbaiki kesalahan prediksi dari model sebelumnya.
#### Kelebihan
Keunggulan utama CatBoostClassifier adalah penggunaan metode ordered boosting, yang dirancang untuk mengurangi overfitting dan mencegah target leakage. Ordered boosting membangun pohon keputusan menggunakan subset data yang tidak mengandung informasi masa depan dari target, sehingga menjaga integritas model selama proses pelatihan. Selain itu, CatBoost menggunakan oblivious trees, yaitu struktur pohon simetris di mana semua cabang pada tingkat yang sama menggunakan aturan pemisahan (split) yang sama. Ini membuat model lebih efisien dalam komputasi dan lebih stabil selama pelatihan.
#### Kekurangan
Meskipun CatBoostClassifier memiliki banyak keunggulan, model ini juga memiliki beberapa kekurangan yang perlu diperhatikan sebelum digunakan. Salah satu kekurangan utamanya adalah waktu pelatihan yang relatif lebih lama dibandingkan dengan framework lain seperti LightGBM, terutama pada dataset berukuran besar. Hal ini disebabkan oleh kompleksitas metode ordered boosting dan pengolahan fitur kategorikal yang lebih canggih. Selain itu, CatBoost dapat mengonsumsi memori dalam jumlah besar, yang bisa menjadi kendala pada perangkat dengan kapasitas sumber daya terbatas. Dalam kasus di mana data seluruhnya bersifat numerik tanpa fitur kategorikal, keunggulan CatBoost menjadi kurang menonjol, dan alternatif seperti XGBoost atau LightGBM mungkin lebih efisien. CatBoostClassifier juga menggunakan struktur pohon simetris (oblivious trees) yang meskipun cepat dan stabil, bisa kurang fleksibel dalam menangkap pola kompleks pada data dibanding pohon tidak simetris yang digunakan oleh model lain. Dari sisi komunitas dan ekosistem, CatBoost masih memiliki dokumentasi dan dukungan komunitas yang lebih kecil dibanding XGBoost, sehingga pengguna mungkin akan lebih kesulitan menemukan solusi atau referensi untuk masalah yang lebih spesifik. Terakhir, untuk keperluan deployment, format model CatBoost tidak sefleksibel model dari framework lain, dan integrasi ke dalam sistem produksi terkadang memerlukan konversi atau penyesuaian tambahan. Oleh karena itu, meskipun CatBoostClassifier sangat andal untuk data dengan banyak fitur kategorikal, penggunaannya tetap harus disesuaikan dengan konteks kebutuhan proyek dan sumber daya yang tersedia.
### 2. XGBoost Classifier
XGBoost (Extreme Gradient Boosting) adalah salah satu algoritma machine learning berbasis gradient boosting yang sangat populer dan banyak digunakan dalam berbagai kompetisi data science maupun proyek industri. Dikembangkan oleh Tianqi Chen, XGBoost dirancang untuk menghasilkan model yang akurat dengan efisiensi tinggi, baik dalam hal waktu pelatihan maupun penggunaan memori. Dalam projek ini, hyperparameter yang digunakan untuk model CatBoost Classifier adalah sebagai berikut:
- 'n_estimators': trial.suggest_int('n_estimators', 1000, 3000),
- 'max_depth': trial.suggest_int('max_depth', 4, 10),
- 'learning_rate': trial.suggest_loguniform('learning_rate', 0.01, 0.3),
- 'min_child_weight': trial.suggest_int("min_child_weight", 5, 15),
- 'subsample': trial.suggest_float('subsample', 0.5, 1.0),
- 'reg_lambda': trial.suggest_loguniform("reg_lambda", 1, 10),
- 'reg_alpha': trial.suggest_loguniform("reg_alpha", 1, 10),
- 'colsample_bytree': trial.suggest_float('colsample_bytree', 0.5, 1.0),
- 'scale_pos_weight': class_weights_dict[1] / class_weights_dict[0],
- 'use_label_encoder': False,
- 'objective': 'binary:logistic',
- 'eval_metric': 'auc',
- 'tree_method': 'gpu_hist',
- 'random_state': 42,
- 'verbosity': 0
Parameter-parameter di ataslah yang digunakan dalam proses hyperparameter tuning menggunakan Optuna.
#### Cara Kerja
XGBoostClassifier bekerja berdasarkan prinsip gradient boosting, yaitu sebuah teknik ansambel yang membangun model prediktif secara bertahap dengan cara menambahkan pohon keputusan (decision tree) satu per satu. Tujuan dari setiap pohon yang ditambahkan adalah untuk memperbaiki kesalahan prediksi yang dilakukan oleh gabungan pohon-pohon sebelumnya. Proses ini dimulai dengan model awal yang sederhana, biasanya berupa rata-rata nilai target, kemudian pada setiap iterasi, XGBoost menghitung residual atau kesalahan dari prediksi sebelumnya dan melatih pohon baru untuk memprediksi residual tersebut. Hasil dari pohon baru ini kemudian ditambahkan ke model sebelumnya dengan bobot tertentu yang diatur oleh learning rate. Model akhir adalah gabungan dari semua pohon yang telah dilatih secara bertahap.
#### Kelebihan
Keunggulan utama dari cara kerja XGBoost terletak pada efisiensinya. Ia menggunakan teknik pemangkasan pohon (pruning) secara cerdas, hanya melanjutkan percabangan jika memberikan keuntungan tertentu berdasarkan fungsi objektif. Selain itu, XGBoost melakukan pemilihan split berdasarkan skor gain tertinggi, yaitu seberapa besar perbaikan yang bisa dicapai jika sebuah fitur digunakan untuk membagi node. Untuk mencegah overfitting, XGBoost menambahkan komponen regularisasi ke dalam fungsi objektif, baik L1 (lasso) maupun L2 (ridge), yang membatasi kompleksitas model. Model ini juga sangat efisien dalam menangani data besar karena mendukung parallel processing dan tree boosting by blocks, serta mampu mengelola nilai yang hilang (missing values) secara otomatis. Secara keseluruhan, cara kerja XGBoostClassifier menjadikannya model yang sangat kuat untuk klasifikasi, khususnya dalam konteks data numerik atau setelah fitur kategorikal diubah melalui encoding.
#### Kekurangan
Meskipun XGBoostClassifier merupakan salah satu model klasifikasi yang sangat populer dan kuat dalam banyak kasus, model ini tetap memiliki sejumlah kekurangan yang perlu dipertimbangkan. Salah satu kelemahan utamanya adalah ketidakmampuannya dalam menangani fitur kategorikal secara langsung. XGBoost mengharuskan pengguna melakukan proses encoding seperti label encoding atau one-hot encoding terlebih dahulu, yang bisa meningkatkan kompleksitas preprocessing, terutama jika data memiliki banyak fitur kategorikal atau tingkat kategorinya tinggi. Kekurangan lain adalah risiko overfitting, terutama jika jumlah pohon terlalu banyak atau model terlalu dalam, meskipun hal ini dapat dikendalikan melalui regularisasi dan validasi silang. Selain itu, meskipun dokumentasi XGBoost cukup lengkap, struktur internal model bisa jadi relatif kompleks bagi pemula, sehingga mungkin tidak semudah dipahami dibanding algoritma yang lebih sederhana seperti logistic regression atau decision tree tunggal. Maka dari itu, meskipun XGBoost sangat powerful, penggunaannya ideal jika didukung dengan pemahaman yang baik tentang teknik boosting dan eksperimen yang hati-hati.
### 3. LightGBM Classifier
LightGBM Classifier adalah sebuah model machine learning berbasis algoritma Gradient Boosting Decision Tree (GBDT) yang diimplementasikan melalui framework LightGBM. Model ini digunakan untuk menyelesaikan masalah klasifikasi, baik biner maupun multikelas, dengan cara membangun serangkaian pohon keputusan (decision tree) secara bertahap. Setiap pohon baru yang ditambahkan bertujuan untuk memperbaiki kesalahan prediksi dari gabungan pohon-pohon sebelumnya. Dalam proses pelatihannya, LightGBM menggunakan teknik boosting, yaitu pendekatan ansambel yang menggabungkan banyak model lemah menjadi satu model yang kuat. Dalam projek ini, hyperparameter yang digunakan untuk model CatBoost classifier adalah sebagai berikut:
- 'n_estimators': trial.suggest_int('n_estimators', 1000, 3000),
- 'max_depth': trial.suggest_int('max_depth', 4, 12),
- 'learning_rate': trial.suggest_loguniform('learning_rate', 0.01, 0.3),
- 'num_leaves': trial.suggest_int('num_leaves', 20, 100),
- 'min_child_weight': trial.suggest_int("min_child_weight", 5, 15),
- 'subsample': trial.suggest_uniform("subsample", 0.5, 1.0),
- 'reg_lambda': trial.suggest_loguniform("reg_lambda", 1, 10),
- 'reg_alpha': trial.suggest_loguniform("reg_alpha", 1, 10),
- 'feature_fraction': trial.suggest_float('feature_fraction', 0.5, 1.0),
- 'bagging_fraction': trial.suggest_float('bagging_fraction', 0.5, 1.0),
- 'scale_pos_weight': class_weights_dict[1] / class_weights_dict[0],
- 'objective': 'binary',
- 'metric': 'auc',
- 'random_state': 42,
- 'device': "gpu",
- 'verbosity': 1
Parameter-parameter di ataslah yang digunakan dalam proses hyperparameter tuning menggunakan Optuna.
#### Cara Kerja
Cara kerja LightGBM Classifier dimulai dengan melatih pohon pertama berdasarkan data asli, kemudian menghitung error atau residual dari prediksi tersebut. Pohon berikutnya akan dilatih untuk memprediksi residual tersebut, bukan label aslinya, sehingga setiap pohon secara progresif berusaha meminimalkan kesalahan keseluruhan. Berbeda dari metode boosting tradisional, LightGBM mengoptimalkan proses ini dengan dua teknik utama: pertama, histogram-based binning, yang mengelompokkan nilai-nilai fitur menjadi interval atau “bin” agar proses split menjadi lebih cepat dan hemat memori; kedua, leaf-wise tree growth, yaitu strategi penumbuhan pohon berdasarkan leaf yang memberikan penurunan loss terbesar, sehingga model lebih cepat mencapai akurasi tinggi meskipun berpotensi overfitting jika tidak dikontrol.
#### Kelebihan
LightGBM Classifier memiliki sejumlah kelebihan yang membuatnya sangat populer dalam berbagai aplikasi machine learning, terutama yang melibatkan data tabular dalam skala besar. Salah satu keunggulan utamanya adalah kecepatan dan efisiensi komputasi yang tinggi. Hal ini dicapai melalui pendekatan histogram-based learning dan leaf-wise tree growth, yang membuat proses pelatihan jauh lebih cepat dan hemat memori dibandingkan metode boosting konvensional. LightGBM juga mampu menangani dataset berukuran besar dan berdimensi tinggi tanpa penurunan performa yang signifikan. Selain itu, model ini mendukung fitur kategorikal secara langsung tanpa perlu one-hot encoding, yang tidak hanya mempercepat pelatihan tetapi juga menjaga informasi kategorikal tetap utuh. Dalam banyak kasus, LightGBM menghasilkan akurasi yang tinggi dan mendukung pelatihan secara paralel, sehingga sangat cocok untuk penggunaan industri berskala besar maupun kompetisi data science.
#### Kekurangan
Salah satu kekurangan utama dari model LightGBM Classifier adalah kecenderungannya terhadap overfitting, terutama jika digunakan pada dataset kecil atau bising, karena strategi leaf-wise dapat menghasilkan pohon yang sangat dalam. Model ini juga cukup sensitif terhadap pemilihan hyperparameter, sehingga memerlukan proses tuning yang cermat agar dapat mencapai performa optimal. Selain itu, LightGBM memiliki interpretabilitas yang lebih rendah dibandingkan model linear atau pohon tunggal, sehingga tidak selalu mudah dijelaskan kepada pihak non-teknis. Terakhir, meskipun unggul pada data tabular, LightGBM kurang cocok untuk data non-struktural seperti gambar atau teks mentah tanpa proses prapemrosesan yang memadai. Oleh karena itu, meskipun sangat powerful, penggunaan LightGBM tetap harus disesuaikan dengan karakteristik data dan tujuan analisis.
### Catatan
Pada projek ini model terbaik merupakan CatBoost Classifier, model ini dipilih sebagai model terbaik karena memiliki performa yang lebih baik dibandingkan dengan model lainnya terutama pada metrik AUC yang merupakan metrik utama pada projek ini. Penjelasan lengkap mengenai proses evaluasi moodel pada projek ini diuraikan pada bagian **evaluation**.
## Hasil Model Development dengan Hyperparameter Tuning Menggunakan Optuna
Dari hasil hyperparameter tuning menggunakan Optuna yang dilakukan diperoleh kobinasi hyperparameter terbaik pada masing-masing model adalah sebagai berikut:
| Parameter             | CatBoost                                      | XGBoost                                         | LightGBM                                      |
|-----------------------|-----------------------------------------------|--------------------------------------------------|-----------------------------------------------|
| depth / max_depth     | 5                                             | 7                                                | 5                                             |
| learning_rate         | 0.020222696045590682                         | 0.010748684338336508                            | 0.03524277427146533                          |
| n_estimators          | 2730                                          | 2363                                             | 1577                                          |
| min_child_samples / weight | 8                                       | 8                                                | 6                                             |
| subsample             | 0.785442438128251                            | 0.9830600452086742                              | 0.9239690349553612                           |
| l2_leaf_reg / reg_lambda | 2.158146091666474                        | 2.0248504434648122                              | 2.756854418038015                            |
| reg_alpha             | -                                             | 1.4440848051268385                              | 8.115555620480569                            |
| colsample_bytree      | -                                             | 0.7528917686403951                              | -                                             |
| feature_fraction      | -                                             | -                                                | 0.5405850236090899                           |
| bagging_fraction      | -                                             | -                                                | 0.7496192462219053                           |
| class_weights / scale_pos_weight | {0: 0.5547, 1: 5.0702}             | 9.140350877192983                               | 9.140350877192983                            |
| loss_function / objective | Logloss                                 | binary:logistic                                  | binary                                        |
| eval_metric / metric  | -                                             | auc                                              | auc                                           |
| bootstrap_type        | Bernoulli                                     | -                                                | -                                             |
| border_count          | 127                                           | -                                                | -                                             |
| random_strength       | 4.854710359766653                            | -                                                | -                                             |
| use_label_encoder     | -                                             | False                                            | -                                             |
| tree_method           | -                                             | gpu_hist                                         | -                                             |
| random_seed / state   | 42                                            | 42                                               | 42                                            |
| task_type / device    | GPU                                           | -                                                | gpu                                           |
| verbose / verbosity   | 0                                             | 0                                                | 1                                             |

## Evaluation
Untuk proses evaluasi, projek ini menggunakan enam metrik evaluasi yaitu accuracy, precision, recall, F1-score, AUC, dan balance accuracy. Metrik evaluasi tersebut dipilih karena sesuai dengan tugas dari projek ini yang merupakan tugas klasifikasi. Kemudian, dari 5 metrik evaluasi tersebut, metrik evaluasi utama adalah AUC karena lebih relevan untuk kasus dengan data imbalance seperti pada projek ini. Penjelasan dari masing-masing metrik evaluasi diuraikan sebagai berikut:
### 1. Accuracy
Accuracy adalah metrik evaluasi yang mengukur proporsi prediksi yang benar (baik positif maupun negatif) dari seluruh jumlah prediksi yang dilakukan oleh model. Dengan kata lain, accuracy menunjukkan seberapa sering model membuat prediksi yang tepat. Formula dari metrik accuracy ini adalah sebagai berikut:

![metrik-accuracy](https://github.com/user-attachments/assets/16d8e0a4-f8fe-49a8-a4aa-666c8debf3c4)
#### Cara Kerja
1. Model melakukan prediksi terhadap data uji.
2. Hasil prediksi dibandingkan dengan label sebenarnya.
3. Dihitung berapa jumlah prediksi yang benar dan total prediksi.
4. Accuracy adalah persentase prediksi yang benar dari keseluruhan prediksi.
### 2. Precision
Precision adalah metrik yang mengukur seberapa banyak dari semua prediksi positif yang dibuat oleh model, benar-benar positif. Dengan kata lain, precision menunjukkan ketepatan model dalam memprediksi kelas positif. Formula dari metrik precision ini adalah sebagai berikut:

![metrik-precision](https://github.com/user-attachments/assets/4c96b09f-ab96-4002-88cf-8455538949ea)
#### Cara Kerja
1. Model melakukan prediksi dan mengklasifikasikan beberapa data sebagai positif.
2. Dari semua prediksi positif tersebut, dicek berapa yang benar (TP) dan berapa yang salah (FP).
3. Precision dihitung sebagai rasio prediksi positif yang benar terhadap semua prediksi positif.
### 3. Recall
Recall adalah metrik evaluasi yang mengukur seberapa banyak dari seluruh data positif yang benar-benar berhasil dideteksi oleh model sebagai positif. Dengan kata lain, recall menunjukkan kemampuan model dalam menemukan seluruh kasus positif yang sebenarnya. Formula dari metrik recall ini adalah sebagai berikut:

![metrik-recall](https://github.com/user-attachments/assets/ba2058dd-6940-425c-8fb6-21bdecf00ca2)
#### Cara Kerja
1. Dari semua data yang sebenarnya positif, dicek berapa yang berhasil diprediksi positif (TP), dan berapa yang terlewat (FN).
2. Recall adalah rasio antara positif yang ditemukan dan seluruh data yang memang positif.
### 4. F1-Score
F1-score adalah metrik evaluasi yang menggabungkan precision dan recall dalam satu angka menggunakan rata-rata harmonik. Metrik ini memberikan keseimbangan antara precision dan recall, terutama saat keduanya penting untuk diperhatikan. Formula dari metrik f1-score ini adalah sebagai berikut:

![metrik-f1-score](https://github.com/user-attachments/assets/8b8d1b36-d57a-4c56-abc2-96865ccd56cd)
#### Cara Kerja
1. Hitung precision dan recall dari hasil prediksi model.
2. Gunakan rumus rata-rata harmonik untuk menggabungkannya.
3. F1-score akan tinggi hanya jika precision dan recall sama-sama tinggi.
### 5. AUC
AUC adalah singkatan dari Area Under the Curve, yang biasanya merujuk pada AUC-ROC — yaitu luas di bawah kurva ROC (Receiver Operating Characteristic). AUC mengukur kemampuan model dalam membedakan antara kelas positif dan negatif di seluruh threshold klasifikasi yang mungkin. Formula dari metrik AUC ini adalah sebagai berikut:

![metrik-auc](https://github.com/user-attachments/assets/f65cc9c5-e74b-42ad-b94a-13a8440e7afb)
#### Cara Kerja
1. Model mengeluarkan skor probabilitas (bukan label langsung).
2. Untuk berbagai nilai threshold, dihitung nilai TPR dan FPR.
3. Titik-titik ini dipetakan ke dalam grafik ROC curve.
4. AUC adalah luas area di bawah kurva ROC tersebut.
### 6. Balance Accuracy
Balanced accuracy adalah metrik evaluasi yang mengukur rata-rata dari sensitivitas (recall untuk kelas positif) dan spesifisitas (recall untuk kelas negatif). Metrik ini berguna ketika data tidak seimbang, karena mempertimbangkan performa model terhadap kedua kelas secara adil. Formula dari metrik AUC ini adalah sebagai berikut:

![metrik-balance-accuracy](https://github.com/user-attachments/assets/1623290d-5569-4b46-917f-bc5ade948701)
#### Cara Kerja
1. Hitung recall untuk kelas positif.
2. Hitung recall untuk kelas negatif (spesifisitas).
3. Ambil rata-ratanya.
### Hasil Evaluasi Sebelum Feature Selection
Hasil evaluasi model pada data validation sebelum proses feaure selection dijalankan disajikan sebagai berikut:

![evaluation-1](https://github.com/user-attachments/assets/288be1d7-2ab4-43bc-83ad-ec2c01b662c8)

Berdasarkan tabel di atas, terlihat bahwa model CatBoost merupakan model terbaik karena unggul pada semua metrik evaluasi.
### Feature Selection dengan Feature Importance
Dari pembangunan model tahap pertama (sebelum feature selection) diperoleh feature importance dari model terbaik yaitu CatBoost sebagai berikut:

![feature-importance](https://github.com/user-attachments/assets/65a917bd-e2b9-4368-abb9-77d2074442fc)

Rincian informasi feature importance dalam bentuk tabel adalah sebagai berikut:

![feature-importance-table](https://github.com/user-attachments/assets/f772ea8f-a2e0-4191-815a-68e3f7e9decf)

Dalam projek ini,, fitur yang dipertahankan adalah fitur dengan nilai importance di atas 1.0. Sehingga dari 17 fitur yang digunakan sebelumnya, berubah menjadi hanya 9 fitur saja.
### Training Ulang Model Menggunakan Fitur Hasil Featrue Selection
Proses training ulang yang dijalankan setelah tahap feature selection diimpelementasikan persis sama dengan proses training model sebelum feature selection yang dijelaskan sebelumnya (menggunakan model **CatBoost, XGBoost, dan LightGBM** dengan hyperparameter tuning menggunakan Optuna). Kemudian dari hasil training ulang tersebut diperoleh kombinasi hyperparameter terbaik pada masing-masing model adalah sebagai berikut:
| Parameter               | CatBoost                                      | LightGBM                                      |
|-------------------------|-----------------------------------------------|-----------------------------------------------|
| depth / max_depth       | 6                                             | 9                                             |
| learning_rate           | 0.014316048234469615                         | 0.24530972917090857                          |
| n_estimators            | 1845                                          | 1871                                          |
| min_child_samples / weight | 6                                         | 10                                            |
| subsample               | 0.6822372595652207                            | 0.8107449289947282                           |
| l2_leaf_reg / reg_lambda | 1.2526655213890152                          | 3.6424940090312554                           |
| reg_alpha               | -                                             | 5.180751167571764                            |
| feature_fraction        | -                                             | 0.6307025538288416                           |
| bagging_fraction        | -                                             | 0.8582711085498285                           |
| class_weights / scale_pos_weight | {0: 0.5547, 1: 5.0702}              | 9.140350877192983                            |
| loss_function / objective | Logloss                                    | binary                                        |
| metric                  | -                                             | auc                                           |
| bootstrap_type          | Bernoulli                                     | -                                             |
| border_count            | 50                                            | -                                             |
| random_strength         | 3.453662960663551                            | -                                             |
| random_seed / state     | 42                                            | 42                                            |
| task_type / device      | GPU                                           | gpu                                           |
| verbose / verbosity     | 0                                             | 1                                             |

Sebagai catatan tambahan, evaluasi model XGBoost tidak ditampilkan setelah feature selection karena ketika proses pembangunan model ulang dilakukan (setelah feature selection) terdapat kesalahan atau error yang terhjadi pada model XGBoost sehingga tidak dapat digunakan pada proses evaluasi.
### Hasil Evaluasi Setelah Feature Selection
Hasil evaluasi model pada data validation setelah proses feaure selection dijalankan disajikan sebagai berikut:

![evaluation-2](https://github.com/user-attachments/assets/2ab0b462-1c24-4b68-a538-847093158565)

Berdasarkan tabel di atas, terlihat bahwa model CatBoost tetap menjadi model terbaik karena unggul pada semua metrik evaluasi. Namun, ternyata terdapat penurunan nilai pada recall, F1-score, dan balance accuracy, <strong><u>sehingga model yang akan digunakan adalah model CatBoost sebelum feature selection</u></strong>. 

## Daftar Pustaka
Widyaningsih, T., & Suryaningsi, S. (2022). Kajian Perlindungan Hukum Terhadap Data Pribadi Digital Anak Sebagai Hak Atas Privasi di Indonesia. Nomos : Jurnal Penelitian Ilmu Hukum, 2(3), 93–103. https://doi.org/10.56393/nomos.v1i5.582.

Fa'izi, M. Bachtiar. Dampak Data Harvesting: Manfaat dan Risiko Bagi Privasi Publik. Online at https://cyberhub.id/pengetahuan-dasar/dampak-data-harvesting, accessed 26 Mei 2025.

Lyandra, N. Ruang Digital Aman dan Sehat bagi Anak, Menakar Efektivitas PP Tunas. Online at https://kbr.id/artikel-podcast/ruang_publik/ruang-digital-aman-dan-sehat-bagi-anak-menakar-efektivitas-pp-tunas, accessed 26 Mei 2025.

Tobing, R.  Darurat Perlindungan Anak di Dunia Digital. Online at https://savethechildren.or.id/artikel/darurat-perlindungan-anak-di-dunia-digital, accessed 26 Mei 2025.
