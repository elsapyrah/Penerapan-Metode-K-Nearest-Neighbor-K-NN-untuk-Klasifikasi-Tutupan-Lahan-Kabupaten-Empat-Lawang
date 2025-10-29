# Penerapan-Metode-K-Nearest-Neighbor-K-NN-untuk-Klasifikasi-Tutupan-Lahan-Kabupaten-Empat-Lawang

# Model
Tutupan lahan merupakan informasi penting dalam berbagai bidang seperti perencanaan tata ruang, pengelolaan sumber daya alam, pengelolaan lingkungan, dan mitigasi bencana. Tutupan lahan paling umum biasanya adalah kategori urban (perkotaan) dan keperluan pertanian.

Metode K-Nearest Neighbor (K-NN) adalah sebuah metode klasifikasi yang populer terhadap sekumpulan data berdasarkan pembelajaran data yang sudah terklasifikasikan sebelumnya. K-NN dilakukan  dengan mencari  kelompok k objek  dalam  data  training  yang paling dekat (mirip) dengan objek pada data baru atau data testing. Setelah memilih k tetangga terdekat pertama, langkah selanjutnya adalah menghitung jumlah data yang termasuk dalam masing-masing 
kelas dari k tetangga tersebut. Kelas dengan jumlah data terbanyak akan menjadi kelas 
pemenang, kemudian diberikan sebagai label kelas pada data.

Tahapan metode KNN:
1. Menentukan parameter K
2. Menghitung jarak antara data training dan data testing
3. Mengurutkan jarak yang terbentuk dari hasil perhitungan euclidean sebelumnya
4. Menentukan jarak terdekat sampai urutan K, dalam penelitian ini digunakan nilai K senilai 5
5. Data inputan sebagai data latih yang sudah dilakukan label ini memiliki nilai dari masing-masing hasil digitasi tersebut. Nilai DN dari piksel yang diambil dari hasil digitasi manual digunakan sebagai fitur dalam algoritma KNN, DN disini merupakan nilai spektral dari masing-masing landsat citra 8.
6. Mencari jumlah kelas dari tetangga terdekat dan tetapkan kelas tersebut sebagai kelas yang akan dievaluasi pada tahap berikutnya.

Perhitungan jumlah piksel:
luas wilayah/luas satu piksel

# Data
Citra satelit Landsat 8 yang diperoleh dari Google Earth Engine (GEE). Data citra yang digunakan merupakan data Kabupaten Empat Lawang yang diambil pada rentang waktu 1 April 2024 hingga 30 April 2024. 

# Evaluasi Model
1. Validation Error Matrix (sering juga disebut Confusion Matrix): tabel evaluasi yang digunakan untuk mengukur kinerja model klasifikasi dengan membandingkan hasil prediksi model dengan label sebenarnya (ground truth) pada data validasi atau testing.
2. Error Matrix pada algoritma KNN (K-Nearest Neighbors) adalah tabel evaluasi hasil klasifikasi, yang menunjukkan berapa banyak data yang diklasifikasikan dengan benar atau salah oleh model KNN dibandingkan dengan label aslinya.

# Hasil
Algoritma KNN menunjukkan akurasi yang lebih tinggi (0,970) dibandingkan set validasi (0,961), yang mengindikasikan bahwa model KNN memiliki performa lebih baik secara keseluruhan.


<img width="360" height="219" alt="image" src="https://github.com/user-attachments/assets/f0279259-decd-4ff5-9c41-8143204a1525" />

Terlihat area berwarna pink yang cukup luas diklasifikasikan sebagai lahan terbuka. Ini mencakup lahan kosong, ladang atau area terbuka lainnya yang tidak tertutup vegetasi atau bangunan. Garis-garis biru memanjang menunjukkan klasifikasi sungai atau badan air lainnya yang mengalir di wilayah tersebut. Area berwarna hijau merupakan klasifikasi tutupan lahan yang didominasi oleh vegetasi seperti hutan, perkebunan, atau area bervegetasi lainnya. Area coklat yang tersebar di beberapa wilayah lahan terbuka menunjukkan area yang dihuni atau area terbangun dengan bangunan dan infrastruktur perkotaan. Pada pengklasifikasian ini juga terdapat kelas lain yakni jalan yang diwakili warna ungu, tetapi sayangnya pada gambar kurang terlihat jelas karena tertutup oleh area klasifikasi lainnya seperti vegetasi dan lahan terbuka. 
