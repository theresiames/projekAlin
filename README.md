
# Game Puzzle OBE

## 1. Deskripsi Proyek

**Game Puzzle OBE** merupakan permainan edukasi berbasis web yang dirancang untuk membantu pengguna memahami dan mempraktikkan konsep Operasi Baris Elementer (OBE) dalam mata kuliah Aljabar Linear Elementer.

Dalam permainan ini, pemain diberikan sebuah matriks augmented yang harus diubah menjadi bentuk **Reduced Row Echelon Form (RREF)** dengan menggunakan tiga jenis Operasi Baris Elementer.

Pemain harus menentukan sendiri operasi yang akan dilakukan pada setiap langkah. Aplikasi menyediakan fitur bantuan berupa Hint apabila pemain mengalami kesulitan.

## 2. Tujuan Proyek

Tujuan pengembangan Game Puzzle OBE adalah:

1. Membantu pengguna memahami konsep Operasi Baris Elementer.
2. Melatih kemampuan dalam melakukan operasi pada matriks augmented.
3. Memahami proses penyelesaian Sistem Persamaan Linear (SPL) menggunakan metode Gauss-Jordan.
4. Mengenalkan bentuk REF dan RREF beserta perbedaannya.
5. Meningkatkan kemampuan berpikir logis dan ketelitian dalam menyelesaikan persoalan matriks melalui permainan.

## 3. Konsep Permainan

Pemain akan diberikan matriks augmented pada setiap level. Tugas pemain adalah mengubah matriks tersebut menjadi bentuk RREF dengan menggunakan operasi baris yang tersedia.

Pemain bebas menentukan urutan operasi selama operasi tersebut sesuai dengan aturan OBE.

### Tampilan Permainan

Permainan memiliki beberapa komponen utama:

- **Matriks:** Menampilkan matriks augmented yang sedang dikerjakan.
- **Panel Aksi:** Menyediakan tiga jenis operasi baris elementer.
- **Riwayat Langkah:** Menampilkan daftar operasi yang telah dilakukan.
- **Undo:** Membatalkan operasi terakhir.
- **Hint:** Memberikan petunjuk mengenai operasi yang dapat dilakukan berikutnya.
- **Informasi Permainan:** Menampilkan level, jumlah langkah, langkah minimum acuan, dan skor.
- **Pesan Kemenangan:** Muncul ketika matriks berhasil mencapai bentuk RREF.

## 4. Fitur Utama

### 4.1. Operasi Baris Elementer

Pemain dapat menggunakan tiga jenis operasi berikut:

**1. Pertukaran Baris (Swap)**

Menukar posisi dua baris dalam matriks.

Rᵢ ↔ Rⱼ

**2. Perkalian Baris (Scale)**

Mengalikan suatu baris dengan konstanta bukan nol.

Rᵢ ← kRᵢ, dengan k ≠ 0

**3. Penjumlahan Baris (Add Row)**

Menambahkan suatu baris dengan kelipatan baris lainnya.

Rᵢ ← Rᵢ + kRⱼ

### 4.2. Pengecekan RREF

Aplikasi memiliki sistem pengecekan otomatis untuk menentukan apakah matriks sudah memenuhi syarat RREF, yaitu:

1. Setiap pivot bernilai 1.
2. Setiap kolom pivot memiliki elemen selain pivot bernilai 0.
3. Posisi pivot pada baris berikutnya berada lebih ke kanan.
4. Semua baris nol berada di bagian paling bawah.

### 4.3. Hint (Petunjuk)

Fitur Hint memberikan saran operasi yang dapat dilakukan pemain untuk mengubah matriks menuju bentuk RREF.

Petunjuk menggunakan proses Gauss-Jordan yang berjalan di belakang layar. Pemain tetap harus memilih dan melakukan operasi sendiri.

### 4.4. Riwayat dan Undo

- Riwayat mencatat setiap operasi yang dilakukan pemain.
- Tombol Undo memungkinkan pemain membatalkan operasi terakhir.
- Matriks dapat dikembalikan ke kondisi sebelumnya tanpa mengulang permainan dari awal.

### 4.5. Sistem Skor dan Bintang

Pemain mendapatkan skor berdasarkan jumlah langkah yang digunakan untuk menyelesaikan matriks.

Penilaian menggunakan tiga kategori bintang:

- **3 Bintang:** Jumlah langkah maksimal satu langkah di atas langkah minimum acuan.
- **2 Bintang:** Jumlah langkah lebih banyak dari kategori tiga bintang, tetapi masih mendekati langkah minimum.
- **1 Bintang:** Matriks berhasil diselesaikan dengan jumlah langkah yang lebih banyak.

## 5. Level Permainan

Permainan memiliki lima level dengan tingkat kesulitan yang meningkat.

| Level | Ukuran Matriks | Tingkat Kesulitan |
|---|---|---|
| 1 | 2 × 3 | Angka kecil dan operasi dasar |
| 2 | 3 × 4 | Sistem Persamaan Linear dengan solusi tunggal |
| 3 | 3 × 4 | Membutuhkan pertukaran baris |
| 4 | 3 × 4 | Sistem Persamaan Linear dengan solusi tak hingga |
| 5 | 4 × 5 | Sistem Persamaan Linear yang memungkinkan tidak memiliki solusi |

Setiap level memiliki karakteristik matriks yang berbeda sehingga pemain dapat mempelajari berbagai kondisi penyelesaian SPL.

## 6. Penerapan Materi Aljabar Linear

Proyek ini menerapkan beberapa konsep utama dalam Aljabar Linear Elementer.

### 6.1. Matriks Augmented

Matriks augmented merupakan gabungan antara matriks koefisien dan matriks konstanta dari suatu Sistem Persamaan Linear. Matriks ini menjadi objek utama yang harus diselesaikan pemain.

### 6.2. Operasi Baris Elementer

OBE digunakan untuk melakukan transformasi terhadap baris-baris matriks tanpa mengubah himpunan solusi SPL.

### 6.3. Metode Gauss-Jordan

Metode Gauss-Jordan merupakan metode penyelesaian SPL dengan melakukan operasi baris hingga matriks mencapai bentuk RREF. Metode ini juga digunakan sebagai dasar pembuatan fitur Hint.

### 6.4. Reduced Row Echelon Form (RREF)

RREF merupakan bentuk matriks yang memenuhi seluruh kriteria eselon baris tereduksi. Pencapaian bentuk RREF menjadi kondisi utama untuk menyelesaikan setiap level.

### 6.5. Rank Matriks

Rank matriks digunakan untuk menentukan jenis solusi SPL berdasarkan perbandingan rank matriks koefisien dengan rank matriks augmented.

Klasifikasi solusi:

- **Solusi tunggal:** rank(A) = rank([A|b]) = jumlah variabel.
- **Solusi tak hingga:** rank(A) = rank([A|b]) dan lebih kecil dari jumlah variabel.
- **Tidak ada solusi:** rank(A) berbeda dengan rank([A|b]).

## 7. Sistem di Balik Permainan

Aplikasi menggunakan beberapa proses utama untuk mendukung jalannya permainan:

1. **Fungsi OBE:** Menjalankan operasi pertukaran, perkalian, dan penjumlahan baris.
2. **Pengecek RREF:** Memeriksa apakah matriks sudah memenuhi kriteria RREF.
3. **Generator Level:** Menghasilkan matriks permainan melalui transformasi OBE dari matriks RREF yang telah ditentukan.
4. **Mesin Hint:** Menggunakan langkah Gauss-Jordan untuk memberikan saran operasi kepada pemain.
5. **Sistem Undo:** Menyimpan kondisi matriks sebelumnya agar operasi dapat dibatalkan.
6. **Klasifikasi Solusi:** Menentukan jenis solusi SPL berdasarkan rank matriks.

## 8. Teknologi yang Digunakan

Teknologi yang digunakan dalam pengembangan proyek:

- **HTML:** Membuat struktur halaman web.
- **CSS:** Mengatur tampilan dan desain antarmuka permainan.
- **JavaScript:** Mengimplementasikan logika permainan, operasi matriks, pengecekan RREF, Hint, Undo, dan sistem skor.

## 9. Cara Bermain

1. Buka aplikasi Game Puzzle OBE melalui browser.
2. Pilih level permainan yang tersedia.
3. Perhatikan matriks augmented yang ditampilkan.
4. Pilih salah satu dari tiga operasi baris elementer.
5. Tentukan baris yang akan dioperasikan dan masukkan nilai yang diperlukan.
6. Tekan tombol eksekusi untuk menerapkan operasi.
7. Perhatikan perubahan matriks dan riwayat langkah.
8. Gunakan Hint apabila membutuhkan petunjuk.
9. Gunakan Undo apabila ingin membatalkan operasi terakhir.
10. Selesaikan matriks hingga mencapai bentuk RREF.
11. Dapatkan skor dan bintang berdasarkan jumlah langkah yang digunakan.

## 10. Kondisi Kemenangan

Pemain dinyatakan berhasil menyelesaikan level apabila matriks augmented telah memenuhi seluruh kriteria RREF.

Setelah berhasil, aplikasi akan menampilkan:

- Pesan keberhasilan.
- Jumlah langkah yang digunakan.
- Skor yang diperoleh.
- Jumlah bintang.
- Jenis solusi SPL.

Pemain kemudian dapat melanjutkan ke level berikutnya.

## 11. Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dilakukan untuk meningkatkan kualitas permainan:

- Menambahkan variasi matriks pada setiap level.
- Mengembangkan sistem peringkat berdasarkan skor.
- Menambahkan mode gelap dan terang.
- Menambahkan penjelasan materi OBE pada halaman tutorial.
- Menambahkan animasi perubahan matriks agar proses operasi lebih mudah dipahami.

## 12. Kesimpulan

Game Puzzle OBE merupakan media pembelajaran interaktif yang menggabungkan konsep permainan puzzle dengan materi Operasi Baris Elementer dalam Aljabar Linear Elementer.

Melalui permainan ini, pengguna tidak hanya memperoleh hasil akhir penyelesaian SPL, tetapi juga terlibat langsung dalam proses transformasi matriks menggunakan tiga jenis OBE.

Dengan demikian, proyek ini diharapkan dapat membantu pengguna memahami konsep OBE, metode Gauss-Jordan, bentuk RREF, serta klasifikasi solusi Sistem Persamaan Linear melalui pengalaman belajar yang lebih menarik dan interaktif.
