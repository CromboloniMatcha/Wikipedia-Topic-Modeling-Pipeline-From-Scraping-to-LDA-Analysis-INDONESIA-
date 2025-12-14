# Wikipedia-Topic-Modeling-Pipeline-From-Scraping-to-LDA-Analysis-INDONESIA-
Proyek ini menyajikan pipeline end-to-end otomatis untuk menganalisis topik tersembunyi dalam data tekstual Indonesia. Dimulai dari pengumpulan data mentah (Crawling/Scraping) hingga penemuan klaster topik yang koheren menggunakan algoritma Latent Dirichlet Allocation (LDA) dan evaluasi menggunakan Coherence Score.

Fitur Utama (Key Features)
100% Otomatis: Otomasi penuh dari pengumpulan data (Wikipedia) hingga output hasil pemodelan. Tidak memerlukan pelabelan data manual (unsupervised).

Target Spesifik: Mengumpulkan konten informatif dari artikel-artikel Wikipedia Bahasa Indonesia (fokus pada topik Geografi dan Ekonomi).

Topic Discovery: Menggunakan model LDA untuk mengidentifikasi dan memvisualisasikan kata kunci yang mendefinisikan setiap tema yang tersembunyi dalam korpus.

Metrik Pengukuran (Evaluasi): Evaluasi kuantitatif kualitas topik yang ditemukan menggunakan Coherence Score (C_v).

Inferensi Model: Menyediakan testing cell untuk mengklasifikasikan dokumen baru secara otomatis ke dalam topik dominan yang sudah dilatih.

Teknologi yang Digunakan
Bahasa: Python

Scraping/Crawling: requests dan BeautifulSoup

Preprocessing: re (Regex) dan Custom Stop Word List Bahasa Indonesia

Topic Modeling: scikit-learn (LDA), gensim (Coherence Score)

Data Handling: pandas dan json

Struktur Pipeline (Cara Kerja)
Proyek ini terdiri dari 6 tahapan utama yang dapat dijalankan secara berurutan dalam Jupyter Notebook (topic_modeling.ipynb):

Input URL: Menyediakan daftar judul artikel Wikipedia target (fokus Geografi dan Ekonomi).

Scraping Otomatis: Kode mengambil konten teks murni (paragraf panjang) dari setiap URL, menghindari elemen HTML yang tidak perlu.

Preprocessing: Data dibersihkan (lower-casing, penghapusan stop words Indonesia, penghapusan angka/simbol).

Modeling (LDA): Teks divetorisasi menggunakan TF-IDF, lalu model LDA dilatih untuk menemukan N jumlah topik (misalnya, 5 topik).

Evaluasi Matriks: Menghitung Coherence Score (C_v) untuk memvalidasi kualitas topik secara statistik.

Inferensi/Testing: Menguji model dengan teks input baru dan menampilkan probabilitas topik yang paling dominan.
