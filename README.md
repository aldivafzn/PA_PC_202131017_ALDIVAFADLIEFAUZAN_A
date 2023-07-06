
## word segmentation

Word segmentation dalam Jupyter Notebook adalah proses memisahkan teks berbahasa natural menjadi kata-kata individu menggunakan kode Python dalam lingkungan Jupyter Notebook. Dalam Jupyter Notebook, Anda dapat menggunakan pustaka dan alat pemrosesan bahasa alami (NLP) yang tersedia dalam Python untuk melakukan word segmentation.

Berikut adalah langkah-langkah umum untuk melakukan word segmentation dalam Jupyter Notebook:

Terlebih dahulu, mengimpor modul yang diperlukan: matplotlib.pyplot, skimage.io, skimage.color, dan skimage.measure. Modul-modul ini digunakan untuk membuat plot dan melakukan pemrosesan gambar.

Kemudian, mendefinisikan fungsi detect_letters(image_path) yang akan digunakan untuk mendeteksi huruf-huruf dalam gambar. Fungsi ini mengambil path gambar sebagai argumen.

Di dalam fungsi detect_letters, Anda membaca gambar menggunakan io.imread(image_path), mengonversikannya ke skala keabuan menggunakan color.rgb2gray(image), dan melakukan thresholding untuk mengubah gambar menjadi biner.

Setelah itu, menerapkan operasi morfologi dengan menggunakan measure.label untuk membersihkan gambar dan measure.find_contours untuk menemukan kontur huruf-huruf.

Selanjutnya, mendeteksi huruf-huruf berdasarkan area dan aspek rasio. Anda mengiterasi melalui setiap kontur dan menghitung dimensi dan properti huruf-huruf yang terdeteksi. Jika memenuhi kondisi tertentu (area > 100 dan aspek rasio > 0.2), maka huruf tersebut dianggap terdeteksi.

Fungsi detect_letters mengembalikan daftar huruf-huruf yang terdeteksi, yang berisi koordinat dan dimensi persegi panjang yang mengelilingi huruf.

Setelah mendefinisikan fungsi detect_letters,  memanggilnya dengan memberikan path gambar sebagai argumen. Hasil deteksi huruf-huruf disimpan dalam variabel detected_letters.

Selanjutnya, menggunakan matplotlib untuk menampilkan gambar awal, gambar dengan persegi panjang yang mengelilingi huruf-huruf yang terdeteksi, serta informasi dimensi huruf pada gambar tersebut.

Menggunakan plt.subplot dan plt.imshow, Anda menampilkan gambar awal pada subplot pertama.

Pada subplot kedua, menampilkan gambar dengan persegi panjang yang mengelilingi huruf-huruf yang terdeteksi. menggunakan plt.gca().add_patch(rect) untuk menambahkan persegi panjang pada gambar.

Pada subplot ketiga, menampilkan gambar dengan persegi panjang yang mengelilingi huruf-huruf yang terdeteksi. juga menambahkan teks yang menunjukkan dimensi huruf menggunakan plt.text.

Terakhir, menggunakan plt.tight_layout() untuk mengatur tata letak plot secara rapi dan plt.show() untuk menampilkan semua subplot.

Dengan demikian, kode tersebut memanfaatkan fungsi detect_letters untuk mendeteksi huruf-huruf dalam gambar dan menghasilkan visualisasi yang menunjukkan persegi panjang yang mengelilingi huruf-huruf yang terdeteksi.

Word segmentation dalam Jupyter Notebook memanfaatkan kekuatan dan fleksibilitas Python serta kemampuan interaktif Jupyter Notebook untuk menjalankan kode, memvisualisasikan data, dan melihat hasil dengan cepat.

