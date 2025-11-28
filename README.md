Analisis Pengaruh Kategori Uang Saku terhadap Nilai Mata Kuliah ADS

Proyek ini berisi kode dan data untuk melakukan analisis statistik komparatif. Tujuannya adalah untuk menguji secara signifikan apakah terdapat perbedaan rata-rata Nilai Akhir Mata Kuliah Analisis Data Statistika (ADS) di antara berbagai Kategori Uang Saku mahasiswa.

1. Struktur Repository

Berikut adalah susunan folder dan file utama dalam repositori ini:

.
├── Code Final Banget.Rmd  # Skrip utama R Markdown untuk analisis statistik
├── dataset final.xlsx - Nilai ADS.csv  # Data utama yang digunakan untuk ANOVA
├── Poster #dalam pdf
└── README.md #Penjelasan singkat repository

2. Dataset yang Digunakan

Deskripsi Singkat

Nilai_RA, Nilai_RB, Nilai_RC

Komponen nilai akhir mata kuliah ADS (Kelas RA, RB, RC).

uang_saku_yang_diberikan_oleh_orangtua

Besaran uang saku dalam rentang nominal.

kategorik / Kategori_Uang_Saku

Variabel faktor yang digunakan dalam uji ANOVA (misalnya: Rendah, Sedang, Tinggi).

3. Library/Paket R yang Digunakan

Skrip Code Final Banget.Rmd membutuhkan paket-paket berikut. Pastikan Anda telah menginstalnya di lingkungan R Anda:

install.packages(c("readxl", "tidyverse", "car", "agricolae", "e1071"))


Setelah terinstal, paket-paket yang dimuat (dengan library()) dalam skrip adalah:

readxl: Untuk membaca data dari file Excel (.xlsx).

tidyverse: Kumpulan paket untuk manipulasi dan visualisasi data (termasuk dplyr dan ggplot2).

car: Digunakan untuk Uji Homogenitas Variansi (leveneTest).

agricolae: Dapat digunakan untuk uji lanjutan (post-hoc) seperti Tukey HSD (saat ini dikomentari).

e1071: Digunakan untuk menghitung statistik skewness.

4. Cara Menjalankan Skrip

Untuk mereproduksi analisis dan hasil, ikuti langkah-langkah berikut:

Prasyarat:

Pastikan Anda telah menginstal R dan RStudio.

Pastikan semua paket di atas (readxl, tidyverse, dll.) telah terinstal.

Pastikan file dataset final banget.xlsx berada di lokasi yang dapat diakses.

Langkah-langkah:

Buka file Code Final Banget.Rmd di RStudio.

Jalankan semua chunk kode dalam file .Rmd secara berurutan, atau gunakan tombol Knit untuk menghasilkan laporan akhir.

Output Utama

Skrip akan menghasilkan output di konsol yang meliputi:

Visualisasi: Boxplot, Dot Plot, dan Histogram.

Uji Asumsi: Hasil Uji Shapiro-Wilk (Normalitas) dan Uji Levene (Homogenitas).

Keputusan Uji: Secara otomatis menampilkan hasil ANOVA (jika data Normal) atau Kruskal-Wallis (jika data tidak Normal).

Statistik Deskriptif: Nilai Skewness per kategori.

Proyek ini merupakan bagian dari Tugas Besar Mata Kuliah Analisis Data Statistika (ADS) 2025 Institut Teknologi Sumatera.
