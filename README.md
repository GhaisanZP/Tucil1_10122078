# Tucil1_10122078
# Penyelesaian IQ Puzzler Pro dengan Algoritma Brute Force

## Penjelasan Singkat Program
IQ Puzzler Pro adalah permainan papan yang diproduksi oleh perusahaan Smart Games. Tujuan
dari permainan ini adalah pemain harus dapat mengisi seluruh papan dengan piece (blok
puzzle) yang telah tersedia.
Komponen penting dari permainan IQ Puzzler Pro terdiri dari:
1. Board (Papan) – Board merupakan komponen utama yang menjadi tujuan permainan
dimana pemain harus mampu mengisi seluruh area papan menggunakan blok-blok yang
telah disediakan.
2. Blok/Piece – Blok adalah komponen yang digunakan pemain untuk mengisi papan
kosong hingga terisi penuh. Setiap blok memiliki bentuk yang unik dan semua blok harus
digunakan untuk menyelesaikan puzzle.

Tugasnya adalah menemukan cukup satu solusi dari permainan IQ Puzzler Pro dengan
menggunakan algoritma Brute Force, atau menampilkan bahwa solusi tidak ditemukan jika
tidak ada solusi yang mungkin dari puzzle.
Program ini mengimplementasikan algoritma brute force murni (tanpa teknik heuristik). Program membaca input dari file berekstensi `.txt` yang berisi :
- Dimensi papan (N x M) dan banyak piece (P).
- Jenis konfigurasi papan: **DEFAULT**, **CUSTOM**, atau **PYRAMID**.
- Bentuk pieces dalam format teks (huruf A-Z).

Setiap piece dicari varian orientasinya (rotasi 90°, 180°, 270°; refleksi horizontal dan vertikal, termasuk kombinasi dari hasil rotasi). Algoritma brute force kemudian diterapkan untuk mencoba menempatkan semua pieces ke board secara rekursif dengan menggunakan backtracking (tetap merupakan brute force murni karena tidak ada pemangkasan berdasarkan heuristik) sehingga seluruh board terisi tanpa adanya tumpang tindih. Jika solusi ditemukan, program menampilkan board solusi dengan warna yang berbeda untuk setiap piece, waktu pencarian (dalam milisecond), dan jumlah iterasi yang dilakukan. Program juga menyediakan opsi untuk menyimpan solusi ke file berekstensi `.txt`.

## Requirement Program dan Instalasi
- **Java Development Kit (JDK):** Minimal JDK 8
- **IDE/Text Editor:** Eclipse, IntelliJ IDEA, atau Visual Studio Code
- **Library Standar Java:** Menggunakan library seperti `java.io` dan `java.util`.

### Struktur Folder Proyek
- **src:** berisi source code program (.java).
- **bin:** berisi executable file (hasil kompilasi .class).
- **test:** berisi file output solusi (teks).
- **doc:** berisi laporan tugas kecil dalam bentuk PDF.

## Cara Mengompilasi Program
### Menggunakan Command Line:
1. Buka terminal dan navigasikan ke direktori root proyek.
2. Jalankan perintah:
`javac -d bin src/Main.java`
Perintah ini akan mengompilasi file Java dari folder **src** dan menempatkan file .class ke folder **bin**.

### Menggunakan IDE:
- **Eclipse:** Atur *Default Output Folder* ke **bin** melalui *Project Properties → Java Build Path → Source*.
- **Visual Studio Code:** Jalankan perintah:
`javac -d bin src/Main.java`

## Cara Menjalankan dan Menggunakan Program
### Menjalankan Program
Setelah dikompilasi, jalankan program dengan perintah:
`java -cp bin Main`
Atau, jika menggunakan IDE, cukup klik tombol _Run_ pada class **Main**.
### Cara Penggunaan:
1. Program akan meminta path file test case, misalkan file terdapat di folder `test` dan nama file ialah `testcase1.txt` maka tuliskan `test/testcase1.txt`.
2. Program membaca input dan memproses pieces.
3. Algoritma brute force mencoba semua kemungkinan penempatan (dengan berbagai orientasi) untuk setiap piece secara rekursif.
4. Jika solusi ditemukan, board solusi ditampilkan dengan warna untuk masing-masing piece, waktu pencarian, dan jumlah iterasi yang dilakukan.
5. Program juga menanyakan apakah ingin menyimpan solusi menjadi file berekstensi `.txt`. Jika ya, file output akan disimpan di folder **test** dengan nama file yang dihasilkan otomatis ditambahkan 'solusi_' (misalnya, `test/solusi_testcase1.txt`).

## Author / Identitas Pembuat
- NAMA : Ghaisan Zaki Pratama
- NIM  : 10122078
