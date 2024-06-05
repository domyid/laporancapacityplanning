# Perbandingan Performansi Layanan Cloud pada Back-End

## BAB I Pendahuluan

### 1.1. Latar Belakang
Penggunaan layanan cloud dalam pengembangan aplikasi back-end semakin populer karena kemudahan dan efisiensi yang ditawarkannya. Berbagai bahasa pemrograman dan framework digunakan untuk membangun back-end aplikasi, seperti Golang, Python, Node.js, PHP Laravel, dan PHP CodeIgniter (CI). Namun, performansi layanan cloud untuk masing-masing back-end ini belum banyak diteliti secara mendalam. Penelitian ini bertujuan untuk membandingkan performansi layanan cloud pada back-end yang dibangun menggunakan lima teknologi tersebut dengan menggunakan platform Google Cloud Functions (GCF).

### 1.2. Identifikasi Masalah
1. Bagaimana performansi masing-masing back-end (Golang, Python, Node.js, PHP Laravel, dan PHP CI) ketika diimplementasikan di layanan cloud yang sama (GCF)?
2. Apa saja faktor yang mempengaruhi performansi back-end tersebut di GCF?
3. Bagaimana hasil analisis clustering performansi back-end menggunakan machine learning?

### 1.3. Tujuan dan Manfaat
Tujuan dari penelitian ini adalah:
1. Membandingkan performansi lima teknologi back-end (Golang, Python, Node.js, PHP Laravel, dan PHP CI) pada platform GCF.
2. Mengidentifikasi faktor-faktor yang mempengaruhi performansi dari masing-masing back-end.
3. Melakukan analisis clustering menggunakan machine learning untuk memberikan gambaran yang lebih jelas tentang perbedaan performansi tersebut.

Manfaat dari penelitian ini adalah memberikan panduan bagi para pengembang dalam memilih teknologi back-end yang sesuai dengan kebutuhan performansi di layanan cloud.

### 1.4. Ruang Lingkup
Penelitian ini meliputi:
1. Pengembangan lima aplikasi back-end menggunakan Golang, Python, Node.js, PHP Laravel, dan PHP CI.
2. Implementasi dan pengujian performansi aplikasi back-end tersebut pada platform GCF.
3. Pengumpulan data performansi dan analisis clustering menggunakan machine learning.
4. Penyajian hasil analisis dan kesimpulan dari perbandingan performansi back-end di GCF.

## BAB II Landasan Teori

### 2.1. Deskripsi Topik Yang Sama
Pada bagian ini, akan dijelaskan tentang topik yang berkaitan dengan performansi layanan cloud pada back-end. Berbagai bahasa pemrograman dan framework yang digunakan untuk membangun aplikasi back-end, seperti Golang, Python, Node.js, PHP Laravel, dan PHP CodeIgniter (CI), memiliki karakteristik dan performansi yang berbeda-beda. 

#### 2.1.1 Golang
Golang, atau Go, adalah bahasa pemrograman yang dikembangkan oleh Google. Bahasa ini dikenal dengan efisiensinya dalam penggunaan resource dan performansi yang tinggi. Golang sangat cocok digunakan untuk aplikasi yang membutuhkan pengolahan data dalam jumlah besar dan concurrency. Keunggulan lainnya adalah waktu kompilasi yang cepat dan runtime yang efisien, yang membuatnya ideal untuk layanan cloud yang membutuhkan performansi tinggi.

#### 2.1.2 Python
Python adalah bahasa pemrograman yang sangat populer karena kemudahan penggunaannya dan kekayaan pustaka yang tersedia. Python banyak digunakan dalam berbagai aplikasi, termasuk pengembangan back-end. Namun, performansi Python mungkin kurang optimal dibandingkan dengan Golang atau Node.js, terutama dalam aplikasi dengan beban kerja yang tinggi. Python tetap menjadi pilihan utama untuk pengembangan cepat dan prototyping, serta untuk aplikasi yang memanfaatkan kecerdasan buatan dan analisis data.

#### 2.1.3 Node.js
Node.js adalah lingkungan runtime untuk JavaScript yang dibangun di atas mesin V8 milik Google. Node.js menawarkan model I/O non-blocking yang membuatnya sangat efisien dan cocok untuk aplikasi yang membutuhkan waktu respons cepat dan skalabilitas tinggi. Node.js sering digunakan dalam pengembangan aplikasi real-time seperti chat applications dan streaming services. Performansinya yang tinggi dalam menangani banyak koneksi secara simultan menjadikannya pilihan populer untuk layanan cloud.

#### 2.1.4 PHP Laravel
Laravel adalah salah satu framework PHP yang paling populer untuk pengembangan web. Laravel menyediakan banyak fitur siap pakai yang memudahkan pengembangan aplikasi, seperti routing, middleware, dan ORM (Object-Relational Mapping). Meskipun memiliki overhead yang lebih besar dibandingkan dengan framework lain, Laravel tetap menjadi pilihan utama untuk pengembangan aplikasi web yang membutuhkan fitur lengkap dan kecepatan pengembangan yang tinggi.

#### 2.1.5 PHP CI
CodeIgniter (CI) adalah framework PHP yang ringan dan mudah digunakan. CodeIgniter dirancang untuk pengembangan aplikasi web dengan performansi yang baik dan footprint yang kecil. Framework ini cocok untuk aplikasi sederhana dengan kebutuhan performansi moderat. Keunggulan CodeIgniter terletak pada kemudahan penggunaannya dan dokumentasi yang lengkap, yang membuatnya ideal untuk pengembang yang membutuhkan solusi cepat dan efisien.

#### 2.1.6 Google Cloud Functions
Google Cloud Functions (GCF) adalah layanan komputasi serverless yang disediakan oleh Google Cloud Platform. GCF memungkinkan pengembang untuk menulis dan menjalankan fungsi kecil yang merespons peristiwa cloud tanpa harus mengelola infrastruktur server.

Dalam penelitian ini, GCF digunakan untuk menguji performansi lima back-end yang berbeda: Golang, Python, Node.js, PHP Laravel, dan PHP CI. Setiap back-end diimplementasikan sebagai fungsi di GCF dan diuji dengan beban kerja yang sama untuk mendapatkan data performansi yang konsisten.

Keunggulan penggunaan GCF untuk pengujian ini meliputi:
- *Skalabilitas Otomatis*: GCF secara otomatis menyesuaikan skala dengan jumlah permintaan yang diterima, memastikan bahwa fungsi selalu tersedia.
- *Manajemen Infrastruktur yang Mudah*: Pengembang tidak perlu khawatir tentang pengelolaan server atau infrastruktur karena semua dikelola oleh Google.
- *Biaya Efektif*: Pengguna hanya membayar untuk waktu eksekusi fungsi, sehingga dapat mengurangi biaya dibandingkan dengan menjalankan server secara terus-menerus.
- *Integrasi yang Kuat*: GCF terintegrasi dengan baik dengan layanan Google Cloud lainnya, seperti Cloud Storage, Pub/Sub, dan Firestore, yang dapat digunakan untuk mengelola data dan peristiwa dalam pengujian.

Pengujian performansi dilakukan dengan mengirimkan sejumlah permintaan ke setiap fungsi back-end di GCF dan mengukur parameter-parameter seperti waktu respons, throughput, dan penggunaan resource. Data yang dikumpulkan kemudian dianalisis untuk membandingkan performansi masing-masing back-end dan memberikan rekomendasi tentang teknologi yang paling efisien untuk digunakan dalam lingkungan cloud.