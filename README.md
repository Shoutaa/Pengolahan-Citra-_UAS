# Analisis efektivitas metode canny dan sobel edge detection untuk face recognition

Dhika Restu Fauzi `2206046`
<br> Muhamad Hamzah `2206081`
<br> 

## 1. Pendahuluan
Pengolahan gambar adalah bidang ilmu yang bertujuan untuk menganalisis, memanipulasi, dan mengekstrak informasi dari gambar digital [1](https//example.com). Proses deteksi otomatis dengan kecerdasan buatan bermanfaat dalam berbagai bidang, seperti deteksi plat nomor kendaraan untuk identifikasi pelanggaran dan face detection [2]. Manusia memiliki bentuk wajah yang berbeda-beda, yang berperan sebagai salah satu ciri khas atau identitas unik setiap individu [3]. Seiring dengan berkembangnya zaman, kebutuhan akan sistem cerdas yang dapat mengidentifikasi wajah semakin penting, terutama di bidang keamanan rumah untuk mengenali pencuri atau orang tak dikenal menggunakan kamera CCTV.

Dalam penelitian ini [4], metode Canny digunakan untuk mendeteksi tepi wajah, diikuti oleh pengenalan pola wajah. Dari 40 gambar wajah yang diuji, metode ini menunjukkan persentase keberhasilan sebesar 80%. Berdasarkan hasil perhitungan pada penelitian ini [5] terhadap 10 sampel, nilai MSE pada deteksi tepi Canny dengan penambahan kontras (koefisien 5, 7.5, dan 10) menunjukkan perbedaan tipis, dengan nilai terbesar mencapai 3428.28 (koefisien 10) dan terkecil 1145.38 (koefisien 5). Pada penelitian ini [6], hasil pengujian menunjukkan bahwa Canny memiliki nilai Mean Squared Error (MSE) sebesar 3542,02 dan Peak Signal-to-Noise Ratio (PSNR) sebesar 12,92 . Dalam penelitian ini [7], metode Sobel untuk deteksi tepi wajah menunjukkan akurasi sebesar 76.4% dalam mendeteksi bentuk wajah dan 80.8% dalam ketajaman tepi gambar. Penelitian lainnya [8], menggunakan metode Canny untuk mendeteksi tepi pada citra dengan 10 wajah, dengan hasil rata-rata akurasi sebesar 89,46%. 

xxxx
xxxx

## 2. Metode Penelitian
Penelitian ini menggunakan kerangka penelitian untuk pengenalan pola wajah dengan menggunakan edge detection dan menentukan akurasi pencocokan pola wajah asli dengan pasangan pola wajah yang ditentukan. Gambar 1 menunjukkan kerangka kerja penelitian ini:
[gambar]

### 2.1 pengumpulan Dataset
Penelitian ini menggunakan 10 gambar face recognition dataset dari Kaggle, Dataset dapat diakses melalui website [9]. Dataset yang berfungsi untuk mendeteksi tepi pengenalan wajah. Tabel 1 menunjukkan contoh citra yang digunakan.

### 2.2	Citra Grayscale
Grayscale adalah teknik untuk mengatur kecerahan dan kontras gambar dengan memodifikasi gambar grayscale asli menggunakan algoritma atau perangkat lunak pengolahan gambar  [10].

### 2.3	Edge Detection
Deteksi tepi (edge detection) adalah proses untuk menemukan batas antara dua wilayah citra yang memiliki perbedaan tingkat kecerahan. Proses ini bertujuan untuk mengidentifikasi garis tepi objek dalam citra, yang membantu menyoroti detail penting, terutama pada citra yang buram akibat kesalahan atau efek akuisisi [12].

#### A Sobel
Operator Sobel adalah salah satu algoritma deteksi tepi yang menggabungkan pemfilteran Gaussian dan diferensiasi untuk menghitung nilai gradien dari fungsi kecerahan gambar. Metode utamanya adalah dengan menghitung selisih berbobot antara nilai keabuan piksel target dengan nilai dari area di sekitarnya, yaitu atas, bawah, kiri, dan kanan, kemudian melakukan proses penghalusan gambar. Semakin besar bobot yang diberikan pada piksel yang dekat dengan target, semakin besar pengaruhnya dalam proses konvolusi [13]. Langkah-langkah yang dilakukan oleh operator Sobel untuk menentukan tepi dalam gambar adalah sebagai berikut:
1) Konvolusi gambar skala abu-abu dengan kernel Sobel horizontal dan vertikal
2)	Hitung ukuran gradien menggunakan rumus
3)	Gambar yang dicetak merupakan hasil gradasi besar (G)

#### B Canny

Algoritma Canny adalah metode deteksi tepi yang menggunakan operasi konvolusi dengan filter Gaussian untuk mengurangi noise dalam gambar. Tujuan utama dari algoritma ini adalah meningkatkan akurasi deteksi tepi dengan memaksimalkan rasio sinyal terhadap noise dan memastikan bahwa tepi yang terdeteksi sesuai dengan tepi asli. Proses yang dilakukan oleh operator Canny [6], yaitu:
1) Menghaluskan gambar untuk mengurangi noise, Pemulusan citra dilakukan dengan menerapkan persamaan berikut.
2) proses untuk menentukan resistansi tepi. Tepi harus ditandai pada gambar dengan gradien besar. Operator gradien digunakan dan pencarian dilakukan secara horizontal dan vertikal
3) Menghitung gradien untuk menemukan perubahan intensitas piksel yang signifikan

### 2.4	Pengukuran akurasi

Memberikan informasi tentang tingkat kesamaan antara dua gambar yang sesuai dalam bentuk persentase(%) dan dianggap paling akurat ketika memiliki persentase tingkat akurasi yang mendekati 100% [14] .

### 2.5	Analisis Perbandingan

Pada tahap analisis hasil ini dilakukan perbandingan antara hasil deteksi tepi menggunakan algoritma Canny Edge Detection dengan hasil deteksi tepi menggunakan algoritma Sobel. Berdasarkan nilai akurasi.

## Hasil dan Pembahasan


## Kesimpulan


## Referensi  

> [1]	T. Radillah, O. Veza, and S. Sumijan, “COMPARATIVE ANALYSIS OF CANNY, SOBEL, PREWITT AND ROBERTS EDGE DETECTION OPERATORS ON EYE IRIS IMAGES,” JITK (Jurnal Ilmu Pengetahuan dan Teknologi Komputer), vol. 10, no. 1, pp. 83–90, Jul. 2024, doi: 10.33480/jitk.v10i1.5062.
<br> [2]	I. W. R. Pinastawa, M. G. Pradana, and K. Khoironi, “Edge Detection Model Performance Using Canny, Prewitt and Sobel in Face Detection,” Sinkron, vol. 8, no. 2, pp. 623–631, Mar. 2024, doi: 10.33395/sinkron.v8i2.13497.
<br> [3]	M. S. Hidayatulloh, A. Y. Permana, and W. H. Kristanto, “Pengenalan Wajah dengan Algoritma Support Vector Machine dan Sobel Edge Detection Berbasis Computer Vision dan Caffe Framework,” Jurnal Ilmiah Komputasi, vol. 19, no. 4, Dec. 2020, doi: 10.32409/jikstik.19.4.372.
<br> [4]	W. Zunita and M. T. Chulkamdi, “Detection Of Someone’s Character Based On Face Shape Using The Canny Method,” JOSAR (Journal of Students Academics Research), vol. 6, no. 1, pp. 2503–1155, 2021, doi: 10.35457/josar.v6i1.1445.
<br> [5]	A. M. Prahastiwi, E. S. Wijaya, J. K. H. Ahmad, and D. Purwokerto, “Analisis Deteksi Tepi Pada Kasus Tulisan Tangan Menggunakan Metode Canny Dengan Meningkatkan Nilai Kontras,” Jurnal Media Pratama, vol. 17, no. 1, pp. 25–31, 2023.
<br> [6]	L. Maximillian, Y. Finsensia Riti, M. Anugraha, and Y. J. Palis, “Perbandingan Algoritma Sobel Dan Canny Untuk Deteksi Tepi Citra Daun Lidah Buaya,” KOMPUTA : Jurnal Ilmiah Komputer dan Informatika, vol. 12, no. 2, 2023.
<br> [7]	L. Widiawati and N. Wulandari, “Akurasi Deteksi Tepi Wajah dengan Metode Robert, Metode Prewitt Dan Metode Sobel,” 2019.
<br> [8]	R. Devita and S. Sumijan, “CANNY EDGE DETECTION AND IMAGE SEGMENTATION FOR PRECISION FACE RECOGNITION SYSTEM,” JURTEKSI (Jurnal Teknologi dan Sistem Informasi), vol. 10, no. 2, pp. 347–354, Mar. 2024, doi: 10.33330/jurteksi.v10i2.3059.
<br> [9]	S. Singh, “Face Recognition Dataset.” Accessed: Jan. 16, 2025. [Online]. Available: https://www.kaggle.com/datasets/cybersimar08/face-recognition-dataset
<br> [10]	R. Pramudiya, C. Asyraq, A. Kadafi, and R. P. Sardika, “Analisis Gambar Menggunakan Metode Grayscale Dan Hsv (Hue, Saturation, Value),” 2024.
<br> [11]	E. Fernando Ade Pratama and J. Jumadi, “Implementasi Metode K-Means Clustering Pada Segmentasi Citra Digital,” Jurnal Media Infotama, vol. 18, no. 2, p. 341139, 2022.
<br> [12]	G. T. Piran, H. Alfan, and M. Yunita, “Patterns Recognition (Maumere Sarong) Using Edge Detection With Prewitt, Sobel, Laplacian Of Gaussian (Log), And Canny Methods,” vol. 5, no. 4, pp. 1–10, 2024, doi: 10.52436/1.jutif.2024.5.4.1972.
<br> [13]	W. Kong, J. Chen, Y. Song, Z. Fang, X. Yang, and H. Zhang, “Sobel Edge Detection Algorithm with Adaptive Threshold based on Improved Genetic Algorithm for Image Processing,” 2023. [Online]. Available: www.ijacsa.thesai.org
<br> [14]	I. N. Arini, “Analisis Akurasi Model–Model Prediksi Financial Distress,” 2021.
