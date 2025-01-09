# Pengolahan-Citra-Digital

## Sobel Edge Detection
### Proses Deteksi Tepi
Sebelum mendeteksi tepi pada gambar target, dilakukan beberapa proses pendahuluan.

- Pertama, gambar diubah menjadi **citra abu-abu**, sebagaimana ditunjukkan pada Gambar **Grayscale Image**
- Citra abu-abu ini dihasilkan dari pengolahan gambar asli pada Gambar **Original Image**
- Untuk mensimulasikan noise acak yang sering terjadi dalam proses akuisisi gambar, ditambahkan **noise salt-and-pepper** pada citra abu-abu. Hasilnya ditampilkan dalam bentuk citra pada Gambar **Nioisy Image**.
- Setelah persiapan tersebut selesai, nilai threshold yang telah dihitung untuk digunakan dalam proses deteksi tepi dengan **operator Sobel**. Proses ini menghasilkan citra dengan efek deteksi tepi seperti yang ditunjukkan pada Gambar **Edge Detection**.
  
![Contoh Gambar](hasil/Edge_Detection_Process.jpg "Ini adalah contoh gambar")

> Seperti yang ditunjukkan pada Gambar di atas, algoritma ini memiliki kinerja yang sangat baik dalam mendeteksi tepi objek pada gambar meskipun terdapat gangguan noise. Hasil deteksi tepi menunjukkan kontur yang jelas, detail gambar tetap terjaga, dan informasi penting dari gambar tidak hilang. Hal ini membuat gambar dapat digunakan untuk proses lanjutan dengan hasil yang optimal.

### C. Analisis Hasil Eksperimen
Untuk menunjukkan efek deteksi tepi dari algoritma di bawah gambar yang berbeda, dibawah ini membandingkan algoritma dengan algoritma Sobel tradisional dengan threshold yang berbeda pengaturan operator Sobel tradisional dan ambang batas adaptif setiap gambar ditunjukkan pada Gambahar dibawah ini.
![Contoh Gambar](hasil/Edge_Detection_Different_Threshold.jpg "Ini adalah contoh gambar")

## Canny Edge Detection
###
Hasil dati berbagai fase gambar asli wajah, pasangan gambar asli wajah, deteksi tepi canny, segmentasi gambar dan hasil akurasi gambar.

### Segmentasi gambar

![Contoh Gambar](hasil/wajah1.png "Ini adalah contoh gambar")

![Contoh Gambar](hasil/wajah10.png "Ini adalah contoh gambar")

![Contoh Gambar](hasil/wajah2.png "Ini adalah contoh gambar")

![Contoh Gambar](hasil/wajah6.png "Ini adalah contoh gambar")

![Contoh Gambar](hasil/wajah7.png "Ini adalah contoh gambar")

![Contoh Gambar](hasil/wajah8.png "Ini adalah contoh gambar")

![Contoh Gambar](hasil/wajah9.png "Ini adalah contoh gambar")

### Hasil akurasi

| Image     | Accuracy | SSIM   |
|-----------|----------|--------|
| wajah 1   | 96.15%   | 52%    |
| wajah 10  | 93.07%   | 34%    |
| wajah 2   | 90.61%   | 26%    |
| wajah 6   | 95.06%   | 42%    |
| wajah 7   | 95.47%   | 45%    |
| wajah 8   | 94.24%   | 40%    |
| wajah 9   | 91.68%   | 28%    |
| Rata-rata | 93.75%   | 38.01% |

Hasil yang ditemukan dengan menggunakan metode canny edge detection menghasilkan 7 gambar wajah asli. Tingkat keberhasilan rata-rata adalah 93.75%.
