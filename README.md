
# Tugas project pengolahan citra (Deteksi Buah)
mendeteksi buah berdasarkan warna



## Penjelasan Program

- Import library, Mengimport library yang diperlukan yaitu OpenCV untuk pengolahan citra, NumPy untuk manipulasi array, dan matplotlib untuk menampilkan gambar.
- Membaca gambar, Membaca gambar dengan nama file 'uas.jpg' menggunakan fungsi cv2.imread() dan menyimpannya dalam variabel img.
- Konversi ruang warna, Mengubah ruang warna gambar dari BGR (Blue-Green-Red) ke HSV (Hue-Saturation-Value) menggunakan fungsi cv2.cvtColor(). Konversi ini berguna untuk memudahkan pemrosesan selanjutnya.
- Menentukan batas-batas warna, Menentukan batas-batas warna yang akan di-segmentasi pada gambar. Setiap batas warna ditentukan dalam format HSV. Batas warna tersebut akan digunakan untuk membuat mask (pemisah) pada langkah berikutnya.
- Membuat mask, Membuat mask menggunakan fungsi cv2.inRange(). Mask digunakan untuk memisahkan objek dengan warna yang sesuai dengan batas warna yang telah ditentukan sebelumnya.
- Dilasi mask, Mengaplikasikan operasi dilasi pada mask menggunakan fungsi cv2.dilate(). Dalam kode di atas, dilasi dilakukan dengan kernel berukuran (20, 10) dan dilaksanakan sebanyak satu iterasi. Operasi dilasi bertujuan untuk menghubungkan area yang terpisah dalam mask dan menghilangkan noise kecil.
- Mengambil objek yang telah dipisahkan, Mengambil objek pada gambar asli (img) menggunakan operasi bitwise AND dengan mask yang telah di-dilasi. Hal ini menghasilkan objek yang terisolasi pada gambar.
- Menampilkan hasil, Membuat subplot untuk menampilkan gambar asli (img), hasil segmentasi jeruk (jeruk), hasil segmentasi alpukat (alpukat), dan hasil segmentasi salak (salak) dalam satu frame. Fungsi imshow() digunakan untuk menampilkan gambar pada setiap subplot, dan set_title() digunakan untuk memberi judul pada setiap subplot. Terakhir, plt.show() digunakan untuk menampilkan frame dengan subplot.
    
