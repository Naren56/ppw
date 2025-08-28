# Pengantar Web Mining
Web Mining merupakan salah satu bidang kajian dalam ilmu komputer dan data science yang fokus pada proses penemuan pola dan pengetahuan dari data yang terdapat di World Wide Web. Secara konseptual, web mining adalah penerapan data mining pada lingkungan web yang sangat besar, dinamis, dan heterogen. Etzioni (1996) mendefinisikan web mining sebagai penggunaan algoritma penambangan data untuk secara otomatis menemukan dan mengekstrak informasi dari layanan web. Bing Liu (2007) menambahkan bahwa web mining berfungsi menemukan pola berharga dari tiga dimensi utama, yaitu struktur hyperlink, konten halaman web, dan perilaku pengguna.
Dalam konteks sistem informasi, web mining tidak hanya bersifat teoretis, melainkan juga aplikatif. Menurut Turban et al. (2011), web mining berperan penting dalam decision support systems dan business intelligence, misalnya untuk memahami tren pasar, perilaku konsumen, hingga pembuatan sistem rekomendasi. 

# Web Crawling
Web Crawling adalah tahap awal dalam proses web mining yang bertujuan untuk mengumpulkan data dari halaman web secara otomatis menggunakan agen perangkat lunak yang disebut crawler atau spider. Mesin pencari seperti Google menggunakan web crawler untuk mengindeks konten web sehingga dapat diakses pengguna.
Secara sistematis, web crawling melibatkan pengambilan dokumen melalui traversal hyperlink dari satu halaman ke halaman lainnya. Menurut Bizer et al. (2025), hasil crawling ini dapat berupa HTML, teks bebas, tabel, maupun metadata. Tantangan utama dalam crawling adalah skalabilitas (karena ukuran web yang sangat besar), efisiensi (penggunaan bandwidth dan penyimpanan), serta relevansi (menentukan halaman mana yang perlu diprioritaskan).

# Web Data Preprocessing
Data yang diambil dari web sering kali bersifat tidak terstruktur, kotor, dan tidak lengkap, sehingga memerlukan tahap preprocessing sebelum dianalisis. Tahapan ini meliputi pembersihan data (data cleaning), transformasi ke format yang sesuai, hingga reduksi dimensi.
-Turban et al. (2011) menegaskan bahwa 70–80% waktu proyek data mining dihabiskan pada tahap preprocessing. Proses ini mencakup:
-Pembersihan data: menghapus tag HTML, noise, dan duplikasi.
-Transformasi data: mengubah teks menjadi representasi numerik seperti vektor atau embeddings.
-Seleksi fitur: memilih atribut yang paling relevan.
-Integrasi data: menggabungkan berbagai sumber (misalnya log server, API, dan dokumen HTML).
Secara empiris, kualitas preprocessing sangat menentukan keberhasilan model machine learning yang dibangun. Tanpa preprocessing yang baik, model akan bias, overfitting, atau bahkan gagal memberikan insight yang valid.

# Pembelajaran Terawasi (Supervised Learning)
Supervised Learning adalah metode machine learning berbasis data berlabel, di mana model dilatih untuk mempelajari hubungan antara input dan output yang diketahui. Contoh aplikasinya adalah klasifikasi (misalnya deteksi spam email) dan regresi (prediksi harga rumah).
-Dalam konteks web mining, supervised learning digunakan untuk:
-Klasifikasi dokumen (seperti kategorisasi berita, analisis sentimen).
-Deteksi spam dalam layanan email maupun komentar sosial media.
-Prediksi perilaku pengguna berdasarkan histori kunjungan web.
Metode klasik seperti Naive Bayes dan Support Vector Machine (SVM) telah lama digunakan. Saat ini, penelitian mutakhir juga memanfaatkan Deep Neural Networks dan Transformer-based models (misalnya BERT, GPT) untuk meningkatkan akurasi klasifikasi dokumen web. Hal ini sejalan dengan teori NLP modern yang menyatakan bahwa representasi semantik berbasis embeddings jauh lebih efektif dibanding representasi tradisional berbasis bag-of-words.

# Pembelajaran Tak Terawasi (Unsupervised Learning)
Unsupervised Learning berbeda dengan supervised karena tidak menggunakan data berlabel. Tujuan utamanya adalah menemukan pola, struktur, atau representasi laten dalam data.
-Dalam web mining, unsupervised learning umum digunakan untuk:
-Clustering konten: mengelompokkan artikel, postingan, atau produk yang mirip.
-Topic discovery: menemukan topik populer dalam forum, media sosial, atau berita online.
-Association analysis: menemukan keterkaitan antar item, misalnya pola belanja pengguna.
Metode yang banyak digunakan adalah K-Means, Hierarchical Clustering, serta pendekatan berbasis embeddings seperti Sentence-BERT. Menurut teori similarity measures, ukuran kemiripan yang sering dipakai meliputi Cosine Similarity, Jaccard Index, dan Similarity of Embeddings.
Pendekatan ini sangat penting dalam era big data, karena mayoritas data web tidak terlabel, sehingga hanya melalui unsupervised learning pola tersembunyi dapat dieksplorasi secara sistematis.

# Web Content Mining (Text Mining)
Web Content Mining atau text mining fokus pada pengekstrakan informasi dari konten halaman web. Karena sebagian besar data web berupa teks, metode ini menjadi pusat perhatian.
-Aplikasi content mining meliputi:
-Ekstraksi informasi dari artikel, review, dan komentar.
-Topic modeling menggunakan metode seperti LDA atau BERT.
-Sentiment analysis untuk memahami opini publik.
-Document summarization untuk merangkum artikel panjang.
Menurut Turban et al. (2011), content mining juga dapat diterapkan pada gambar, audio, dan video, meski fokus utama tetap pada teks. Penelitian modern mengintegrasikan transformer models untuk meningkatkan performa sentiment analysis dan klasifikasi dokumen.
Secara empiris, content mining memiliki dampak nyata pada e-commerce (analisis ulasan produk), politik (prediksi opini publik), dan keamanan siber (deteksi ujaran kebencian).

# Web Usage Mining
Web Usage Mining adalah proses menganalisis perilaku pengguna saat berinteraksi dengan situs web. Data yang digunakan biasanya berasal dari log server, cookie, data clickstream, maupun metadata kunjungan.
Aplikasi utamanya adalah:
-Product recommendation systems (misalnya di e-commerce).
-Personalized search, di mana hasil pencarian disesuaikan dengan profil pengguna.
-User profiling untuk memahami segmentasi pelanggan.
Secara teoritis, usage mining menggabungkan pendekatan pattern discovery dan behavioral analytics untuk membentuk representasi preferensi pengguna. Menurut Turban et al. (2011), analisis clickstream memungkinkan pengembang memahami jalur navigasi pengguna sehingga dapat meningkatkan desain website dan retensi pelanggan.

# Web Structure Mining (Graph Mining)
Web Structure Mining berfokus pada analisis struktur hyperlink antar halaman web, dengan memandang web sebagai graf besar yang terdiri atas node (halaman) dan edge (tautan).
-Penerapan teori graph mining dan social network analysis digunakan untuk:
-Menentukan halaman otoritatif (contohnya melalui algoritma PageRank Google).
-Mengidentifikasi influencer di media sosial.
-Menemukan komunitas online melalui metode seperti K-Cores atau Connected Components.
Secara empiris, struktur mining banyak digunakan pada analisis jejaring sosial untuk memahami penyebaran informasi, deteksi hoaks, dan identifikasi simpul penting dalam jaringan. Teori centrality (degree, betweenness, closeness) menjadi dasar dalam mengukur peran aktor dalam graf web.

# Deployment System
Tahap akhir dari web mining adalah deployment system, yaitu mengimplementasikan hasil analisis ke dalam sistem nyata agar dapat digunakan secara praktis. Contohnya:
-Sistem rekomendasi produk di e-commerce.
-Deteksi hoaks di platform media sosial.
-Personalisasi konten pada portal berita.
Deployment bukan hanya soal integrasi teknis, tetapi juga validasi empiris, pengujian sistematis, dan evaluasi berkelanjutan. Menurut kerangka CRISP-DM, deployment adalah tahap terakhir namun bersifat siklis karena model harus terus diperbarui sesuai dengan perubahan data web yang dinamis.