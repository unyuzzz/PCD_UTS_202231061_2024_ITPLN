
# UTS Pengolahan Citra
pada line 1, diawali dengan memanggil function cv2, matplotlib.pyplot dengan alias plt, serta function numpy dengan alias np.
- cv2 diperuntukan untuk dapat memanggil gambar yang ingin di olah citranya
- matplotlib.pyplot alias plt diperuntukan untuk memvisualkan data
- numpy alias np, diperuntukan untuk komputasi ilmiah yang dapat menyediakan objek array multidimensi yang efisien.

# Detec warna merah, hijau dan biru pada sebuah gambar.
    - deklarasi image yang berisikan gambar yang akan diolah dengan perintah cv2.imread('bahan2.jpg')
    - deklarasi alpha, untuk mengatur kontras pada gambar yaitu sebesar 1.5
    - deklarasi beta, untuk mengatur kecerahan pada gambar yaitu akan diatur sebesar 50
    - lalu pada deklarasi congtrast_image dimaksud untuk dapat menyinkron antara kontras dengan kecerahan pada gambar yang akan diolah citranya dengan perintah cv2.convertScaleAbs(image, alpha=alpha, beta=beta)
    - pada image_rgb ini akan bekerja untuk mengubah atau mengkonversi ke RGB dengan perintah 'cv2.cvtColor()' untuk memastikan bahwa saluran warna yang dihasilkan sesuai dengan kebutuhan.
    - Display Images: Kode menciptakan empat gambar yang akan ditampilkan, yaitu citra kontras, serta salinan citra asli dalam kanal warna merah, hijau, dan biru. Ini dilakukan dengan menggunakan plt.subplot() untuk mengatur layout gambar dan plt.imshow() untuk menampilkan gambar. Variabel images berisi daftar gambar, sementara titles berisi judul yang sesuai.
    - Selanjutnya, kode menghitung dan memplot histogram untuk setiap saluran warna (merah, hijau, dan biru) dari citra asli. diperuntukan fungsi cv2.calcHist() untuk menghitung histogram dan plt.plot() untuk memplotnya. Histogram digunakan untuk menunjukkan distribusi intensitas piksel di setiap saluran warna.
    - plt.show() digunakan untul menampilkan semua gambar dan histogram yang sudah diolah.

# membuat ambang batas dari gambar
    - Membaca Citra: Gambar dibaca dari file 'Bahan2.jpg' menggunakan 'cv2.imread()' .
    -  pada image_rgb ini akan bekerja untuk mengubah ke RGB dengan perintah 'cv2.cvtColor()' untuk memastikan bahwa saluran warna yang dihasilkan sesuai dengan kebutuhan.
    - Citra RGB akan dibagi menjadi saluran warna merah (r), hijau (g), dan biru (b) menggunakan cv2.split().
    - Variabel thresh_images dan titles diinisialisasi untuk menyimpan citra hasil ambang batas dan judul yang sesuai.
    - Melakukan proses thresholding untuk setiap kondisi, yaitu citra asli, saluran biru, perbedaan antara saluran merah dan biru (r-b), dan perbedaan antara saluran merah dan hijau (r-g-b).
    - Histogram dari setiap channel dihitung menggunakan cv2.calcHist(). Nilai ambang batas kemudian dicari berdasarkan karakteristik histogram. Proses ini dilakukan untuk membagi citra menjadi area hitam dan putih sesuai ambang batas yang ditentukan.
    - Menggunakan nilai ambang batas yang telah ditentukan, citra asli dibagi menjadi citra ambang batas untuk setiap saluran warna: biru, hijau, dan merah. Ini dilakukan menggunakan cv2.threshold() dengan opsi cv2.THRESH_BINARY.
    - Citra hasil ambang batas untuk setiap saluran warna (biru, hijau, dan merah) ditampilkan menggunakan Matplotlib.
