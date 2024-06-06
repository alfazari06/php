## Web Dinamis
Sebuah situs web dinamis adalah situs web yang menampilkan konten yang dapat berubah secara dinamis berdasarkan interaksi pengguna, waktu, atau data yang diperbarui. Artinya, konten tidak statis; itu bisa berubah tergantung pada berbagai faktor seperti input pengguna, permintaan server, atau data terbaru dari database.
## PHP
PHP (Hypertext Preprocessor) adalah bahasa pemrograman yang sering digunakan untuk mengembangkan situs web dinamis. PHP adalah bahasa pemrograman sisi server, yang berarti kode PHP dijalankan pada server web sebelum hasilnya dikirim ke browser pengguna. Ini memungkinkan pengembang untuk membuat situs web yang dinamis dengan mudah, karena PHP memungkinkan untuk berinteraksi dengan database, mengelola formulir, membuat halaman web dinamis, dan melakukan banyak tugas lainnya untuk memproses data dan membangun konten yang disesuaikan secara dinamis. PHP sangat populer di kalangan pengembang web karena kemampuannya yang kuat, fleksibilitas, dan kemudahan dalam belajar dan digunakan.


# Program Pertama
## kode program
```php
<?php

  

//dibawah ini berfungsi untuk menampilkan

/*

ini

komentar multi bari

*/

$meja = 30;

$tk_kelas = "XI";

$ketua_kelas = "جولي";

$wali_kelas = "صالح";

$ketua_gank = "عبد الرحمن";

$ketua_gank = "Rahmat"; //pengubahan nilai variabel

  

//konstanta

const KEPSEK = "HERWELIS";

define('kelas' , 'RPL 1');

  

/*kutip satu hanya membaca string, variabel dan string

dipisahkan dengan tanda titik */

echo 'jumlah meja di kelas: '. $meja . 'buah';

echo "<br>";

  

//kutip dua bisa membaca nilai dari sebuah variabel

echo "Sholat dlu, nabilang Pak $wali_kelas dan $ketua_kelas     ketua kelas";

echo "<br>";

  

///kutip satu dibaca string disini

echo "Kalau tidak, diracca` sama ketua gank $ketua_gank";

echo "<br>";

  

echo 'Kepseknya ' . KEPSEK;

echo "<br>";

echo 'kelasnya ' . $tk_kelas . ' ' . kelas; 
```

## Penjelasan
1. **Variabel**:
    - Variabel digunakan untuk menyimpan data. Contohnya adalah `$meja`, `$tk_kelas`, `$ketua_kelas`, `$wali_kelas`, dan `$ketua_gank`.
    - Pada baris `$ketua_gank = "Rahmat";`, nilai dari variabel `$ketua_gank` diubah dari `"عبد الرحمن"` menjadi `"Rahmat"`.
2. **Komentar**:
    - Komentar digunakan untuk memberikan penjelasan atau dokumentasi pada kode. Ada dua jenis komentar yang digunakan:
        - Komentar dalam bentuk `//`, yang berfungsi untuk memberikan komentar pada satu baris.
        - Komentar dalam bentuk `/* */`, yang berfungsi untuk memberikan komentar pada beberapa baris sekaligus.
3. **Konstanta**:
    - Konstanta didefinisikan menggunakan kata kunci `const` atau `define()`. Contohnya adalah `const KEPSEK = "HERWELIS";` dan `define('kelas' , 'RPL 1');`.
    - Konstanta bersifat tetap dan nilainya tidak dapat diubah setelah didefinisikan.
4. **Menampilkan Output**:
    - Fungsi `echo` digunakan untuk menampilkan output ke layar.
    - Pada beberapa baris, nilai dari variabel digabungkan dengan string menggunakan operator `.` untuk ditampilkan dalam output.
    - Perbedaan antara penggunaan kutip satu (`'`) dan kutip dua (`"`) adalah kutip dua memungkinkan penggunaan interpolasi string, di mana nilai variabel bisa langsung dimasukkan ke dalam string tanpa harus dipisahkan dengan operator `.`.
5. **Output Program**:
    - Program ini akan menampilkan beberapa baris teks yang mencakup nilai dari variabel dan konstanta yang telah didefinisikan sebelumnya, serta beberapa teks tambahan.

## Hasil
![h.php1.png](Asetphp/h.php1.png)

## Kesimpulan
Program PHP tersebut menggunakan variabel untuk menyimpan data seperti jumlah meja, kelas, nama-nama individu, dan konstanta untuk menyimpan informasi yang nilainya tetap. Komentar digunakan untuk memberikan penjelasan pada bagian-bagian kode. Program ini kemudian menampilkan output yang menggabungkan nilai variabel dan konstanta dengan teks tambahan menggunakan fungsi `echo`.

Dengan demikian, kesimpulannya adalah bahwa program ini merupakan contoh penggunaan dasar variabel, konstanta, komentar, dan fungsi `echo` dalam bahasa pemrograman PHP untuk menampilkan informasi ke layar.

# PHP Dasar
## Echo & Comentar
### Echo
Dalam konteks PHP, "echo" adalah perintah yang digunakan untuk menampilkan teks atau variabel ke dalam halaman web. Ini adalah cara umum untuk menghasilkan output dalam PHP. Misalnya, jika Anda ingin menampilkan pesan sederhana seperti "Hello, world!" di halaman web, Anda dapat menggunakan perintah "echo":

```php
echo "Hello, world!";

```
Perintah ini akan menampilkan "Hello, world!" di halaman web ketika halaman tersebut dimuat.

### Comentar
Sementara itu, "commentar" (komentar) adalah bagian dari kode yang tidak dieksekusi oleh server web. Mereka digunakan untuk memberikan penjelasan atau dokumentasi di dalam kode, atau untuk menonaktifkan sementara potongan kode tertentu tanpa menghapusnya sepenuhnya. Di PHP, ada dua jenis komentar:

1. Komentar satu bar: Untuk menulis komentar satu bar, Anda bisa menggunakan dua garis miring (`//`) diikuti oleh teks komentar. Kode di bawah ini adalah contoh komentar satu bar:

```php
// Ini adalah komentar satu bar

```

2. Komentar multi-baris: Untuk menulis komentar multi-baris, Anda dapat menggunakan tanda `/*` untuk memulai komentar dan `*/` untuk mengakhiri komentar. Semua teks di antara tanda tersebut akan dianggap sebagai komentar. Berikut adalah contoh komentar multi-baris:

```php
/*
Ini adalah
komentar multi-baris
*/

```

Komentar berguna untuk menjelaskan fungsi atau alur kerja dari potongan kode, dan dapat membantu pengembang lain dalam memahami kode yang ditulis. Komentar tidak akan ditampilkan di halaman web dan tidak akan memengaruhi kinerja kode PHP.

## variable & const
### Variable
Dalam pemrograman, "variabel" adalah suatu tempat di mana Anda bisa menyimpan nilai. Ini seperti sebuah kotak di mana Anda dapat menaruh berbagai jenis data, seperti angka, string teks, atau objek, dan Anda dapat mengaksesnya kapan pun Anda butuhkan. Variabel biasanya diberi nama yang menggambarkan nilainya untuk memudahkan penggunaan di dalam kode.

Contoh penggunaan variabel dalam PHP:
```php
$nama = "John"; // variabel $nama menyimpan string "John"
$umur = 25; // variabel $umur menyimpan angka 25

```

### Const
Selain variabel, dalam PHP Anda juga memiliki "konstanta" atau "const". Konstanta adalah seperti variabel tetapi nilainya tidak berubah selama jalannya program. Mereka biasanya didefinisikan dengan huruf besar dan dapat diakses di seluruh program PHP. Anda mendefinisikan konstanta menggunakan fungsi `define()`.

Contoh penggunaan konstanta dalam PHP:
```php
define("PI", 3.14); // Konstanta PI dengan nilai 3.14
echo PI; // Output: 3.14

```


## Operator

**Operator**: Operator digunakan untuk melakukan operasi pada variabel dan nilai. Ada berbagai jenis operator dalam pemrograman seperti operator aritmatika, operator perbandingan, dan operator logika. Beberapa operator dasar dalam PHP meliputi:

### Operator Aritmatika

#### Pemjumlahan

- **Penjelasan:**

    Penjumlahan (+): Digunakan untuk menambahkan dua nilai bersama-sama

```php

$nilai1 = 10;

$nilai2 = 5;

  

$penjumlahan = $nilai1 + $nilai2;

echo "Penjumlahan: " . $penjumlahan . "<br>";

```

```output

Penjumlahan: 15

```

- **Analisis**

    Penjumlahan (+):

    - Operator ini digunakan untuk menambahkan dua nilai bersama-sama.

    - Contoh: `$penjumlahan = $nilai1 + $nilai2;`

    - Hasilnya adalah penjumlahan dari nilai `$nilai1` dan `$nilai2`.

- **Kesimpulan**

    - Kesimpulannya, dengan operator ini, kita dapat menambahkan nilai-nilai numerik dalam PHP dengan mudah.

___

#### Pengurangan

- **Penjelasan:**

    Pengurangan (-): Digunakan untuk mengurangkan nilai kedua dari nilai pertama.

```php

$nilai1 = 10;

$nilai2 = 5;

  

$pengurangan = $nilai1 - $nilai2;

echo "Pengurangan: " . $pengurangan . "<br>";

```

```output

Pengurangan: 5

```

- **Analisis**

    Pengurangan (-):

    - Operator ini digunakan untuk mengurangkan nilai kedua dari nilai pertama.

    - Contoh: `$pengurangan = $nilai1 - $nilai2;`

    - Hasilnya adalah pengurangan dari nilai `$nilai2` dari `$nilai1`.

- **Kesimpulan**

    - Kesimpulannya, penggunaan operator ini memungkinkan kita untuk mengurangkan satu nilai dari yang lain dalam pemrograman PHP.

___

#### Perkalian

- **Penjelasan**

    Perkalian (*): Digunakan untuk mengalikan dua nilai bersama-sama.

```php

$nilai1 = 10;

$nilai2 = 5;

$perkalian = $nilai1 * $nilai2;

echo "Perkalian: " . $perkalian . "<br>";

```

```output

Perkalian: 50

```

- **Analisis**

    Perkalian (*):

    - Operator ini digunakan untuk mengalikan dua nilai bersama-sama.

    - Contoh: `$perkalian = $nilai1 * $nilai2;`

    - Hasilnya adalah perkalian dari `$nilai1` dan `$nilai2`.

- **Kesimpulan**

    - Kesimpulannya, dengan operator ini, kita dapat melakukan perkalian nilai-nilai numerik dalam PHP untuk mendapatkan hasil perkalian.

___

#### Pembagian

- Penjelasan

    Pembagian (/): Digunakan untuk membagi nilai pertama dengan nilai kedua.

```php

$nilai1 = 10;

$nilai2 = 5;

  

$pembagian = $nilai1 / $nilai2;

echo "Pembagian: " . $pembagian . "<br>";

```

```output

Pembagian: 2

```

- **Analisis**

    Pembagian (/):

    - Operator ini digunakan untuk membagi nilai pertama dengan nilai kedua.

    - Contoh: `$pembagian = $nilai1 / $nilai2;`

    - Hasilnya adalah pembagian dari nilai `$nilai1` dengan `$nilai2`.

- **Kesimpulan**

    - Kesimpulannya, operator ini memungkinkan kita untuk membagi nilai-niai numerik dalam PHP dan mendapatkan hasil pembagian.

___

#### Modulus

- Penjelasan

    Modulus (%): Digunakan untuk mengembalikan sisa pembagian dari nilai pertama dengan nilai kedua.

```php

$nilai1 = 10;

$nilai2 = 5;

  

$modulus = $nilai1 % $nilai2;

echo "Modulus: " . $modulus . "<br>";

```

```output

Modulus: 0

```

- **Analisis**

    Modulus (%):

    - Operator ini digunakan untuk mengembalikan sisa pembagian dari nilai pertama dengan nilai kedua.

    - Contoh: `$modulus = $nilai1 % $nilai2;`

    - Hasilnya adalah sisa pembagian dari `$nilai1` dengan `$nilai2`.

- **Kesimpulan**

    - Kesimpulannya, dengan menggunakan operator modulus, kita dapat menghitung sisa pembagian dari nilai-nilai numerik dalam PHP.

___

### Operator Perbandingan

- **Penjelasan**

    1. Operator Sama dengan (== ):

     Operator ini digunakan untuk membandingkan apakah dua nilai sama.

     Contohnya, `$a == $b` akan menghasilkan true jika nilai variabel `$a` sama dengan nilai variabel `$b`, dan false jika tidak sama.

  

    2. Operator Tidak Sama dengan (!=):

     Operator ini digunakan untuk membandingkan apakah dua nilai tidak sama.

     Contohnya, `$a != $b` akan menghasilkan true jika nilai variabel `$a` tidak sama dengan nilai variabel `$b`, dan false jika sama.

  

    3. Operator Kurang dari (<):

     Operator ini digunakan untuk membandingkan apakah nilai kiri kurang dari nilai kanan.

     Contohnya, `$a < $b` akan menghasilkan true jika nilai variabel `$a` kurang dari nilai variabel `$b`, dan false jika tidak kurang dari.

  

    4. Operator Lebih Besar dari (>):

     Operator ini digunakan untuk membandingkan apakah nilai kiri lebih besar dari nilai kanan.

     Contohnya, `$a > $b` akan menghasilkan true jika nilai variabel `$a` lebih besar dari nilai variabel `$b`, dan false jika tidak lebih besar dari.

  

    5. Operator Kurang dari atau Sama dengan (<=):  

     Operator ini digunakan untuk membandingkan apakah nilai kiri kurang dari atau sama dengan nilai kanan.

     Contohnya, `$a <= $b` akan menghasilkan true jika nilai variabel `$a` kurang dari atau sama dengan nilai variabel `$b`, dan false jika tidak kurang dari atau sama dengan.

  

    6. Operator Lebih Besar dari atau Sama dengan (>=):  

     Operator ini digunakan untuk membandingkan apakah nilai kiri lebih besar dari atau sama dengan nilai kanan.

     Contohnya, `$a >= $b` akan menghasilkan true jika nilai variabel `$a` lebih besar dari atau sama dengan nilai variabel `$b`, dan false jika tidak lebih besar dari atau sama dengan.

- **Kode Program**

```php

<?php

$a = 5;

$b = 10;

  

// Operator sama dengan (==)

if ($a == $b) {

    echo "$a sama dengan $b";

} else {

    echo "$a tidak sama dengan $b";

}

echo "<br>";

  
  

// Operator tidak sama dengan (!=)

if ($a != $b) {

    echo "$a tidak sama dengan $b";

} else {

    echo "$a sama dengan $b";

}

echo "<br>";

  
  

// Operator kurang dari (<)

if ($a < $b) {

    echo "$a kurang dari $b";

} else {

    echo "$a tidak kurang dari $b";

}

echo "<br>";

  
  

// Operator lebih besar dari (>)

if ($a > $b) {

    echo "$a lebih besar dari $b";

} else {

    echo "$a tidak lebih besar dari $b";

}

echo "<br>";

  
  

// Operator kurang dari atau sama dengan (<=)

if ($a <= $b) {

    echo "$a kurang dari atau sama dengan $b";

} else {

    echo "$a tidak kurang dari atau sama dengan $b";

}

echo "<br>";

  
  

// Operator lebih besar dari atau sama dengan (>=)

if ($a >= $b) {

    echo "$a lebih besar dari atau sama dengan $b";

} else {

    echo "$a tidak lebih besar dari atau sama dengan $b";

}

?>

```

```output

5 tidak sama dengan 10

  

5 tidak sama dengan 10

  

5 kurang dari 10

  

5 tidak lebih besar dari 10

  

5 kurang dari atau sama dengan 10

  

5 tidak lebih besar dari atau sama dengan 10

  

```

- **Analisis**

    - Dua variabel `$a` dan `$b` diinisialisasi dengan nilai numerik, masing-masing 5 dan 10.

    - Program kemudian membandingkan `$a` dan `$b` menggunakan berbagai operator perbandingan dan menampilkan pesan berdasarkan hasil perbandingan.

    - Karena `$a` (5) tidak sama dengan `$b` (10), maka pesan "5 tidak sama dengan 10" akan ditampilkan.

    - Karena `$a` (5) kurang dari `$b` (10), maka pesan "5 kurang dari 10" akan ditampilkan.

    - Karena `$a` (5) tidak lebih besar dari `$b` (10), maka pesan "5 tidak lebih besar dari 10" akan ditampilkan.

    - Karena `$a` (5) kurang dari atau sama dengan `$b` (10), maka pesan "5 kurang dari atau sama dengan 10" akan ditampilkan.

    - Karena `$a` (5) tidak lebih besar dari atau sama dengan `$b` (10), maka pesan "5 tidak lebih besar dari atau sama dengan 10" akan ditampilkan.

- **Kesimpulan**

    - Program ini membantu memahami cara kerja operator perbandingan dalam PHP.

    - Operator perbandingan digunakan untuk membandingkan nilai dan mengontrol alur program berdasarkan hasil perbandingan.

    - Program seperti ini bermanfaat dalam logika pemrograman untuk membuat keputusan berdasarkan kondisi tertentu.

### Operator Logika

- **Penjelasan**

    Dalam PHP, operator logika digunakan untuk menggabungkan kondisi logis dan menghasilkan nilai boolean (true atau false) berdasarkan kebenaran kondisi tersebut. Contoh operator:

    1. **AND (&&):** Menghasilkan true jika kedua kondisi benar.

    2. **OR (||):** Menghasilkan true jika salah satu atau kedua kondisi benar.

    3. **NOT (!):** Membalikkan nilai kondisi, true menjadi false, dan sebaliknya.

```php

<?php

$a = 5;

$b = 10;

$c = 15;

  

// Operator logika AND (&&)

if ($a < $b && $b < $c) {

    echo "$a kurang dari $b dan $b kurang dari $c";

} else {

    echo "Kondisi AND tidak terpenuhi";

}

echo "<br>";

  

// Operator logika OR (||)

if ($a > $b || $b > $c) {

    echo "$a lebih besar dari $b atau $b lebih besar dari $c";

} else {

    echo "Kondisi OR tidak terpenuhi";

}

echo "<br>";

  

// Operator logika NOT (!)

if (!($a == $b)) {

    echo "$a tidak sama dengan $b";

} else {

    echo "$a sama dengan $b";

}

?>

  

```

```output

5 kurang dari 10 dan 10 kurang dari 15

  

Kondisi OR tidak terpenuhi

  

5 tidak sama dengan 10

```

- **Anlisis**

    - Kita memiliki tiga variabel `$a`, `$b`, dan `$c` dengan nilai 5, 10, dan 15.

    - Operator logika `AND` digunakan untuk memeriksa apakah `$a` kurang dari `$b` dan `$b` kurang dari `$c`. Jika  keduanya benar, pesan yang sesuai ditampilkan.

    - Operator logika `OR` digunakan untuk memeriksa apakah `$a` lebih besar dari `$b` atau `$b` lebih besar dari `$c`. Jika salah satu atau kedua kondisi benar, pesan yang sesuai ditampilkan.

    - Operator logika `NOT` digunakan untuk membalikkan nilai kondisi `$a` == `$b`. Jika `$a` tidak sama dengan `$b`, pesan yang sesuai ditampilkan.

- **Kesimpulan**

    - Kode ini menggunakan operator logika untuk membuat keputusan berdasarkan kondisi-kondisi yang dievaluasi.

    - Operator logika memungkinkan kita untuk menggabungkan kondisi-kondisi logis dan mengontrol alur program berdasarkan kebenaran kondisi tersebut.

    - Dengan menggunakan operator logika, kita dapat membuat program yang lebih kompleks dengan logika yang bergantung pada kondisi-kondisi tertentu.
## Conditional statement
### IF
#### Penjelasan
Pernyataan kondisional "if" dalam bahasa pemrograman PHP digunakan untuk membuat keputusan berdasarkan kondisi tertentu. Dengan menggunakan "if", Anda dapat mengontrol aliran eksekusi program berdasarkan kebenaran atau kevalidan dari suatu kondisi.

Berikut adalah sintaks dasar dari pernyataan kondisional "if" dalam PHP:
```php
if (kondisi) {
    // Blok kode yang akan dieksekusi jika kondisi benar
```
- Jika `kondisi` dievaluasi sebagai benar, maka blok kode di dalam kurung kurawal `{}` setelah pernyataan "if" akan dieksekusi.

#### Struktur
```php
<?php

$variable = nilai_variable;

  

if ($variable >= nilai_variable) {

    echo "output_yang_ditampilkan";

}

?>
```
#### Program
```php
<?php

$umur = 25;

  

if ($umur >= 18) {

    echo "Anda sudah cukup umur.";

}

?>
```
#### Hasil 
![h.php2.png](Asetphp/h.php2.png)
#### Analisis
1. Program tersebut menggunakan struktur kontrol if untuk melakukan pengecekan kondisi tertentu.
2. Variabel `$umur` diinisialisasi dengan nilai 25.
3. Dalam blok if, program memeriksa apakah nilai `$umur` lebih besar dari atau sama dengan 18.
4. Jika kondisi tersebut terpenuhi (nilai `$umur` lebih besar dari atau sama dengan 18), maka program akan mencetak pesan "Anda sudah cukup umur.".
5. Jika kondisi tersebut tidak terpenuhi (nilai `$umur` kurang dari 18), tidak ada output yang dihasilkan.
#### Kesimpulan Program
Program PHP di atas adalah contoh sederhana penggunaan kondisional if dalam bahasa pemrograman PHP. Ini adalah program singkat yang menetapkan sebuah variabel `$umur` dengan nilai 25, dan kemudian memeriksa apakah nilai variabel tersebut lebih besar dari atau sama dengan 18. Jika ya, maka pesan "Anda sudah cukup umur." akan dicetak.

Jadi, jika nilai `$umur` adalah 25 atau lebih, maka outputnya akan menjadi "Anda sudah cukup umur.". Jika nilai `$umur` kurang dari 18, maka tidak akan ada output yang dicetak.

Program ini digunakan untuk memberikan pesan berdasarkan kondisi tertentu, dalam hal ini, memberikan pesan kepada pengguna bahwa mereka sudah cukup umur jika umurnya 18 tahun atau lebih.


### IF-else
#### Penjelasan
Dalam bahasa pemrograman PHP, struktur pengendali `if-else` digunakan untuk membuat keputusan berdasarkan kondisi tertentu. Ini memungkinkan program untuk mengeksekusi kode yang berbeda tergantung pada apakah suatu kondisi itu benar (true) atau salah (false).

Berikut adalah penjelasan tentang `if-else` di PHP:

**else**: Ini adalah bagian opsional yang dapat ditambahkan setelah if. Jika kondisi dalam if tidak terpenuhi (false), maka blok kode di dalam else akan dieksekusi.
Contoh:
```php
$umur = 15;
if ($umur >= 18) {
    echo "Anda sudah cukup umur.";
} else {
    echo "Anda belum cukup umur.";
}

```
#### Struktur
```php
<?php

Variable = Nilai_variable;

  

if(Variable >= Nilai_variable){

    echo "output_yang_ditampilkan";

} else {

    echo "output_yang_ditampilkan";

}

?>

```
#### Program
```php
<?php

$nilai = 80;

  

if($nilai >= 75){

    echo "Nilai Anda Baik!";

} else {

    echo "Maaf, Anda kenak remedial.";

}

?>
```
#### Hasil 
![h.if-else.png](Asetphp/h.if-else.png)
#### Analisis
Program PHP di atas adalah contoh sederhana dari penggunaan struktur kontrol if-else untuk mengevaluasi nilai dari variabel `$nilai` dan memberikan respons berdasarkan nilai tersebut. Di sini, variabel `$nilai` diatur ke nilai 80.

Analisis program ini adalah sebagai berikut:

1. **Inisialisasi Variabel**: Variabel `$nilai` diinisialisasi dengan nilai 80.

2. **Pengecekan Kondisi**: Dalam blok if, kondisi dievaluasi. Jika nilai dari variabel `$nilai` lebih besar atau sama dengan 75, maka pesan "Nilai Anda Baik!" akan dicetak. Jika tidak, maka program akan masuk ke blok else.

3. **Output**: Jika kondisi di blok if terpenuhi (nilai `$nilai` lebih besar atau sama dengan 75), maka pesan "Nilai Anda Baik!" akan dicetak. Jika tidak, maka pesan "Maaf, Anda kenak remedial." akan dicetak.

Dalam hal ini, karena nilai `$nilai` adalah 80, yang lebih besar dari 75, maka output yang akan dihasilkan adalah "Nilai Anda Baik!". Jadi, program memberikan respons positif berdasarkan nilai yang diberikan.
#### Kesimpulan Program
Kesimpulannya, program memberikan respons berdasarkan nilai yang diberikan, memberikan apresiasi ketika nilai mencapai atau melebihi batas tertentu, dan memberikan peringatan ketika nilai di bawah batas tersebut.
### if-else if-else
#### Penjelasan
Struktur kontrol `if-else-if-else` digunakan untuk mengevaluasi beberapa kondisi secara berurutan. Dalam konteks PHP, struktur ini memungkinkan Anda untuk memeriksa beberapa kondisi dan menjalankan blok kode yang sesuai dengan kondisi yang terpenuhi pertama kali.

Berikut adalah penjelasan tentang `if-else-if-else`:

1. **if**: Blok pertama dari struktur ini, di mana Anda menentukan kondisi pertama yang ingin Anda periksa. Jika kondisi ini terpenuhi (true), blok kode dalam if akan dieksekusi.
    
2. **else if**: Ini adalah bagian opsional yang dapat digunakan setelah if. Jika kondisi dalam if tidak terpenuhi, maka kondisi dalam else if akan diperiksa. Jika kondisi else if ini terpenuhi, blok kode di dalamnya akan dieksekusi.
    
3. **else**: Blok terakhir dari struktur, yang akan dieksekusi jika tidak ada kondisi di dalam if atau else if yang terpenuhi. Ini bersifat opsional dan bisa ada atau tidak.
#### Struktur
```php
<?php

Variable = nilai_variable;

  

if (Variable >= nilai_variable) {

    echo "output_yang_ditampilkan";

} elseif (Variable  >= nilai_variable) {

    echo "output_yang_ditampilkan";

} elseif (Variable >= nilai_variable) {

    echo "output_yang_ditampilkan";

} else {

    echo "output_yang_ditampilkan";

}

?>
```
#### Program
```php
<?php

$nilai = 90;

  

if ($nilai >= 90) {

    echo "Nilai Anda sangat baik!";

} elseif ($nilai >= 80) {

    echo "Nilai Anda baik.";

} elseif ($nilai >= 70) {

    echo "Anda mendapat nilai cukup.";

} else {

    echo "Maaf, Anda kenak remedial.";

}

?>
```
#### Hasil 
![h.if-else-if.png](Asetphp/h.if-else.png)
#### Analisis
Analisis program ini adalah sebagai berikut:

1. **Inisialisasi Variabel**: Variabel `$nilai` diinisialisasi dengan nilai 90.
    
2. **Pengecekan Kondisi**: Program mengevaluasi nilai dari variabel `$nilai` menggunakan struktur `if-else-if-else`.
    
    - Jika nilai `$nilai` lebih besar atau sama dengan 90, maka pesan "Nilai Anda sangat baik!" akan dicetak.
    - Jika nilai `$nilai` lebih besar atau sama dengan 80 (tetapi kurang dari 90), maka pesan "Nilai Anda baik." akan dicetak.
    - Jika nilai `$nilai` lebih besar atau sama dengan 70 (tetapi kurang dari 80), maka pesan "Anda mendapat nilai cukup." akan dicetak.
    - Jika nilai `$nilai` kurang dari 70, maka pesan "Maaf, Anda kenak remedial." akan dicetak.
3. **Output**: Karena nilai `$nilai` adalah 90, yang lebih besar atau sama dengan 90, maka pesan "Nilai Anda sangat baik!" akan dicetak.
#### Kesimpulan Program
- Program menggunakan struktur kontrol `if-else-if-else` untuk mengevaluasi nilai dari variabel `$nilai` dan memberikan respons berdasarkan rentang nilai yang terpenuhi.
- Rentang nilai yang dinilai dimulai dari nilai tertinggi ke nilai terendah, yaitu 90 ke 70.
-  Program memberikan respons yang sesuai dengan rentang nilai yang terpenuhi pertama kali.
- Dalam hal ini, karena nilai yang diberikan adalah 90, yang memenuhi kondisi pertama, maka pesan "Nilai Anda sangat baik!" akan dicetak.
- Pesan yang dicetak sesuai dengan kondisi yang terpenuhi, menunjukkan apresiasi terhadap nilai yang tinggi.
- Program ini dapat dengan mudah diubah untuk menangani lebih banyak rentang nilai atau kondisi tambahan sesuai kebutuhan.
### Switch-case
#### Penjelasan
Struktur kontrol `switch-case` dalam PHP digunakan untuk memeriksa nilai satu variabel atau ekspresi terhadap serangkaian nilai yang mungkin. Ini adalah alternatif yang lebih bersih dan terstruktur dibandingkan dengan menggunakan serangkaian pernyataan `if-else` berturut-turut.
#### Struktur
```php
<?php
Variable = "nilai_variable_yang_ingin_ditampilkan";

switch (Variable) {
    case "nilai_variable":
        echo "output_yang_ditampilkan";
        break;
    case "nilai_variable":
        echo "output_yang_ditampilkan";
        break;
    case "nilai_variable":
        echo "output_yang_ditampilkan";
        break;
    default:
        echo "output_yang_ditampilkan";
}
?>
```
#### Program
```php
<?php
$hari = "Selasa";

switch ($hari) {
    case "Senin":
        echo "Hari ini adalah hari Senin.";
        break;
    case "Selasa":
        echo "Hari ini adalah hari Selasa.";
        break;
    case "Rabu":
        echo "Hari ini adalah hari Rabu.";
        break;
    default:
        echo "Hari ini adalah hari lainnya.";
}
?>

```
#### Hasil 
![h.switch.png](Asetphp/h.if-else.png)
#### Analisis
Program PHP di atas menggunakan struktur `switch-case` untuk mengevaluasi nilai variabel `$hari` dan memberikan respons berdasarkan nilai tersebut. Variabel `$hari` diatur ke nilai "Selasa".

Analisis program ini adalah sebagai berikut:

1. **Inisialisasi Variabel**: Variabel `$hari` diinisialisasi dengan nilai "Selasa".
    
2. **Pengecekan Kondisi**: Program menggunakan struktur `switch-case` untuk mengevaluasi nilai variabel `$hari`.
    
    - Jika nilai `$hari` adalah "Senin", maka pesan "Hari ini adalah hari Senin." akan dicetak.
    - Jika nilai `$hari` adalah "Selasa", maka pesan "Hari ini adalah hari Selasa." akan dicetak.
    - Jika nilai `$hari` adalah "Rabu", maka pesan "Hari ini adalah hari Rabu." akan dicetak.
    - Jika nilai `$hari` tidak cocok dengan semua nilai case yang ada, maka blok kode di dalam default akan dieksekusi.
3. **Output**: Karena nilai variabel `$hari` adalah "Selasa", maka pesan "Hari ini adalah hari Selasa." akan dicetak.
#### Kesimpulan Program
- Program menggunakan struktur kontrol `switch-case` untuk mengevaluasi nilai dari variabel `$hari` dan memberikan respons berdasarkan nilai tersebut.
-  Setiap `case` dalam struktur `switch` menentukan nilai-nilai yang mungkin untuk variabel yang dievaluasi.
-  Jika nilai variabel `$hari` cocok dengan salah satu nilai case yang ada, maka blok kode yang sesuai dengan case tersebut akan dieksekusi.
- Jika nilai variabel `$hari` tidak cocok dengan semua nilai case yang ada, maka blok kode di dalam `default` akan dieksekusi.
-  Dalam kasus program di atas, karena nilai variabel `$hari` adalah "Selasa", maka pesan "Hari ini adalah hari Selasa." akan dicetak.
- `Switch-case` memberikan cara yang efisien dan bersih untuk menangani serangkaian kondisi yang mungkin berbeda berdasarkan nilai dari satu variabel atau ekspresi.
## Array
### Array 1 dimensi
#### Penjelasan
Array satu dimensi adalah struktur data yang digunakan untuk menyimpan sekumpulan nilai atau elemen dalam satu dimensi. Artinya, array tersebut hanya memiliki satu baris atau satu level. Setiap elemen dalam array memiliki indeks yang berurutan, dimulai dari 0.

Dalam array satu dimensi, setiap elemen dapat diakses dengan menggunakan indeksnya. Indeks digunakan untuk menunjukkan posisi relatif elemen dalam array. Misalnya, elemen pertama memiliki indeks 0, elemen kedua memiliki indeks 1, dan seterusnya.
#### Struktur
```php
<?php

// Mendefinisikan array satu dimensi

Variable. = array("Nilai", "Nilai", "Nilai", "Nilai");

// Mencetak elemen-elemen array satu per satu

echo "Daftar buah:\n";

echo "============\n";

echo "<br>";

echo "nilai_variable. " . Variable[0] . "\n";

echo "<br>";

echo "nilai_variable.. " . Variable[1] . "\n";

echo "<br>";

echo "nilai_variable.. " . Variable[2] . "\n";

echo "<br>";

echo "nilai_variable.. " . Variable[3] . "\n";

?>
```
#### Program
```php
<?php

// Mendefinisikan array satu dimensi

$buah = array("apel", "jeruk", "pisang", "anggur");


// Mencetak elemen-elemen array satu per satu

echo "Daftar buah:\n";

echo "============\n";

echo "<br>";

echo "1. " . $buah[0] . "\n";

echo "<br>";

echo "2. " . $buah[1] . "\n";

echo "<br>";

echo "3. " . $buah[2] . "\n";

echo "<br>";

echo "4. " . $buah[3] . "\n";

?>
```
#### Hasil 
![h.array-1dimensi.png](Asetphp/h.if-else.png)
#### Analisis
Program PHP di atas menggunakan array satu dimensi untuk menyimpan daftar nama buah dan kemudian mencetaknya satu per satu.

Analisis program ini adalah sebagai berikut:

1. **Mendefinisikan Array**: Program mendefinisikan sebuah array satu dimensi dengan nama `$buah`. Array ini berisi empat elemen, yaitu "apel", "jeruk", "pisang", dan "anggur".
    
2. **Mencetak Elemen Array**: Setelah mendefinisikan array, program mencetak setiap elemen array satu per satu menggunakan pernyataan `echo`. Setiap elemen dipisahkan dengan baris baru menggunakan tag `<br>` untuk membuatnya terlihat lebih rapi di antarmuka web.
    
3. **Output**: Program mencetak daftar buah satu per satu dengan format yang telah ditentukan.
#### Kesimpulan Program
- Program menggunakan array satu dimensi untuk menyimpan daftar nama buah.
- Daftar buah disimpan dalam array dengan nama `$buah`, yang memiliki empat elemen: "apel", "jeruk", "pisang", dan "anggur".
- Setelah mendefinisikan array, program mencetak setiap elemen array satu per satu dengan menggunakan pernyataan `echo`.
- Setiap elemen dicetak dengan format yang sesuai dengan nomor urutnya dalam daftar buah.
- Program mencetak daftar buah dalam format yang terstruktur dan mudah dibaca.
- Penggunaan tag HTML `<br>` digunakan untuk memisahkan setiap elemen buah dalam output agar terlihat lebih rapi di antarmuka web.

### Array  Asosiatif
#### Penjelasan
Array asosiatif adalah tipe array di mana setiap elemen memiliki pasangan kunci-nilai yang terkait. Berbeda dengan array numerik, di mana kunci-kunci elemen secara otomatis diberikan oleh PHP (biasanya berupa angka berurutan), dalam array asosiatif, kunci-kunci ini dapat ditentukan secara eksplisit oleh pengguna.
#### Struktur
```php
$array = array(

    "buah1" => nilai1,

    "buah2" => nilai2,

    "buah3" => nilai3,
    
    "4" => nilai3,
    ...

);
```
#### Program
```php
<?php
// Mendefinisikan array asosiatif
$buah_harga = array(
    "apel" => 5000,
    "jeruk" => 7000,
    "pisang" => 3000,
    "anggur" => 10000
);

// Mengakses dan mencetak informasi dari array asosiatif
echo "Daftar Buah dan Harganya:\n";
echo "=========================\n";
foreach ($buah_harga as $nama_buah => $harga) {
    echo $nama_buah . " : Rp " . $harga . "\n";
}
?>

```
#### Hasil 
![h.array-asosiatif.png](Asetphp/h.array-asosiatif.png)
#### Analisis
1. **Mendefinisikan Array Asosiatif**: Baris pertama mendefinisikan sebuah array asosiatif dengan nama `$buah_harga`. Setiap elemen array memiliki pasangan kunci-nilai, di mana kunci adalah nama buah dan nilai adalah harga buah tersebut.
    
2. **Mencetak Informasi**: Program mencetak judul "Daftar Buah dan Harganya:" diikuti oleh garis pemisah "=========================". Ini adalah bagian dari output yang akan dicetak.
    
3. **Looping Melalui Array**: Program menggunakan loop foreach untuk mengulang melalui setiap pasangan kunci-nilai dalam array asosiatif `$buah_harga`. Pada setiap iterasi, nilai kunci disimpan dalam variabel `$nama_buah`, sedangkan nilai disimpan dalam variabel `$harga`.
    
4. **Mencetak Setiap Pasangan**: Dalam setiap iterasi, program mencetak nama buah dan harganya dengan format yang ditentukan. Nama buah diikuti oleh tanda titik dua dan harga, yang dipisahkan oleh tanda "Rp". Setiap pasangan kunci-nilai dicetak dalam baris terpisah.
    
5. **Output**: Setelah loop selesai dieksekusi, program akan mencetak daftar buah dan harganya sesuai dengan informasi yang tersedia dalam array asosiatif.
#### Kesimpulan Program
Program menggunakan array asosiatif untuk menyimpan dan mencetak daftar buah beserta harganya. Setiap buah memiliki kunci nama buah dan nilai harga buah. Dengan menggunakan loop foreach, program mencetak setiap pasangan kunci-nilai dalam format yang terstruktur. Ini memberikan cara yang efisien dan mudah dimengerti untuk mengelola informasi terkait dalam PHP.

### Array multidimensi
#### Penjelasan
Array multidimensi adalah tipe array di mana setiap elemen array juga dapat menjadi array sendiri. Ini berarti kita memiliki array dalam array. Array multidimensi digunakan untuk menyimpan data yang memiliki struktur yang lebih kompleks daripada array satu dimensi. Sebagai contoh, kita dapat menggunakan array multidimensi untuk menyimpan data tabel, matriks, atau data terstruktur lainnya.
#### Struktur
```php
$array = array(

    array(nilai1, nilai2, nilai3, ...),

    array(nilai4, nilai5, nilai6, ...),

    ...
```
#### Program
```php
$matriks = array(

    array(1, 2, 3),

    array(4, 5, 6),

    array(7, 8, 9)

);

echo $matriks[0][0]; // Output: 1

echo $matriks[1][1]; // Output: 5

echo $matriks[2][2]; // Output: 9
```
#### Hasil 
![h.multidimensi.png](Asetphp/h.multidimensi.png)
#### Analisis
Pada kode di atas, kita memiliki variabel `$matriks` yang merupakan array multidimensi dengan ukuran 3x3. Setiap elemen dalam array utama adalah array lain yang berisi tiga elemen.

- `$matriks[0][0]` mengakses elemen pertama dari array pertama dalam `$matriks`, sehingga menghasilkan output 1.
- `$matriks[1][1]` mengakses elemen kedua dari array kedua dalam `$matriks`, sehingga menghasilkan output 5.
- `$matriks[2][2]` mengakses elemen ketiga dari array ketiga dalam `$matriks`, sehingga menghasilkan output 9.
#### Kesimpulan Program
- Program tersebut menggunakan array multidimensi dalam bahasa pemrograman PHP.
- Array multidimensi digunakan untuk menyimpan data dalam bentuk matriks atau struktur data yang lebih kompleks, di mana setiap elemen dapat diakses menggunakan indeks dari array induk dan array anak.
- Program menunjukkan cara mengakses elemen-elemen spesifik dari matriks menggunakan indeks baris dan kolom.
- Contoh penggunaan dalam program menunjukkan cara mengakses elemen-elemen utama matriks, seperti elemen pertama dari setiap baris, yang merepresentasikan nilai-nilai diagonal dalam matriks.
- Array multidimensi sangat berguna dalam pemrograman untuk memanipulasi dan mengelola data yang memiliki struktur terstruktur, seperti matriks, tabel, atau kumpulan data yang terkait.

## Looping (Pembagian)

### For
#### Penjelasan
Di dalam bahasa pemrograman PHP, pernyataan `for` digunakan untuk melakukan iterasi (pengulangan) sejumlah tertentu. Ini memungkinkan Anda untuk mengeksekusi serangkaian pernyataan dengan jumlah iterasi yang telah ditentukan sebelumnya.
#### Struktur
```php
for (inisialisasi; kondisi; perubahan) {

    // blok kode yang akan diulang
```
#### Program
```php
for ($i = 1; $i <= 5; $i++) {

    echo $i;
```
#### Hasil 
![h.for.png](Asetphp/h.for.png)
#### Analisis
1. `for ($i = 1; $i <= 5; $i++) {`: Pernyataan `for` dimulai dengan inisialisasi `$i` yang diatur ke 1. Kemudian, ada kondisi iterasi yang mengevaluasi apakah nilai `$i` kurang dari atau sama dengan 5. Jika kondisi ini terpenuhi, blok pernyataan dalam pernyataan `for` akan dieksekusi. Setelah setiap iterasi, nilai `$i` akan ditambah satu.
    
2. `echo $i;`: Pada setiap iterasi, nilai `$i` akan dicetak. Dalam contoh ini, nilai `$i` akan mencetak angka dari 1 hingga 5.
    
3. Setelah blok pernyataan dieksekusi, kendali akan kembali ke pernyataan `for`. Jika kondisi iterasi masih terpenuhi (nilai `$i` masih kurang dari atau sama dengan 5), iterasi berikutnya akan dilakukan. Jika tidak, eksekusi program akan melanjutkan ke pernyataan di luar blok `for`.
#### Kesimpulan Program
- rogram menggunakan pernyataan `for` untuk melakukan iterasi sejumlah tertentu.
- Pernyataan `for` terdiri dari tiga bagian: inisialisasi, kondisi, dan iterasi.
- Inisialisasi (`$i = 1`) menginisialisasi variabel iterasi `$i` ke nilai awal 1.
- Kondisi (`$i <= 5`) mengevaluasi apakah nilai variabel iterasi `$i` masih kurang dari atau sama dengan 5. Jika benar, iterasi akan terus dilakukan; jika tidak, iterasi berhenti.
- Iterasi (`$i++`) mengatur variabel iterasi `$i` untuk nilai berikutnya setiap kali iterasi dilakukan.
- Dalam blok pernyataan `for`, nilai variabel iterasi `$i` dicetak menggunakan `echo`.
- Setelah iterasi berakhir, eksekusi program melanjutkan ke pernyataan di luar blok `for`.
### While
#### Penjelasan
Pernyataan `while` dalam PHP digunakan untuk melakukan iterasi (pengulangan) atas serangkaian pernyataan selama kondisi tertentu terpenuhi.
#### Struktur
```php
while (kondisi) {

    // blok kode yang akan diulang

    // perubahan kondisi harus dilakukan di dalam blok kode
```
#### Program
```php
$i = 1;

while ($i <= 5) {

    echo $i;

    $i++;
```
#### Hasil 
![h.while.png](Asetphp/h.while.png)
#### Analisis
1. `$i = 1;`: Variabel `$i` diinisialisasi dengan nilai 1 di luar pernyataan `while`. Ini menyiapkan variabel yang akan digunakan sebagai penghitung iterasi.
    
2. `while ($i <= 5) {`: Pernyataan `while` dimulai di sini. Kondisi iterasi adalah `$i` kurang dari atau sama dengan 5. Selama kondisi ini terpenuhi, blok pernyataan dalam pernyataan `while` akan dieksekusi. Ini berarti iterasi akan terus berlanjut selama nilai variabel `$i` kurang dari atau sama dengan 5.
    
3. `echo $i;`: Pada setiap iterasi, nilai variabel `$i` dicetak. Pada awalnya, `$i` memiliki nilai 1, kemudian akan mencetak nilai 1, 2, 3, 4, dan 5 pada setiap iterasi karena nilai `$i` akan bertambah satu setiap kali pernyataan dalam blok `while` dieksekusi.
    
4. `$i++;`: Setelah mencetak nilai `$i`, nilai variabel `$i` akan ditambah satu. Hal ini diperlukan untuk mencegah pernyataan `while` terus berjalan tanpa henti, sehingga variabel iterasi terus meningkat setiap kali iterasi dilakukan.
#### Kesimpulan Program
- Program menggunakan pernyataan `while` untuk melakukan iterasi (pengulangan) selama kondisi tertentu terpenuhi.
- Variabel `$i` diinisialisasi dengan nilai 1 di luar pernyataan `while`.
- Kondisi iterasi adalah `$i` kurang dari atau sama dengan 5. Ini berarti iterasi akan terus dilakukan selama nilai variabel `$i` kurang dari atau sama dengan 5.
- Pada setiap iterasi, nilai variabel `$i` dicetak menggunakan `echo`.
- Setelah mencetak nilai `$i`, nilai variabel `$i` ditambah satu menggunakan operator penambahan `$i++`. Ini dilakukan untuk memastikan bahwa nilai variabel iterasi terus bertambah setiap kali iterasi dilakukan, sehingga iterasi akhirnya berhenti saat nilai `$i` melebihi 5.
- Hasilnya adalah program akan mencetak angka dari 1 hingga 5 secara berurutan.
### do-while
#### Penjelasan
Pernyataan `do-while` dalam PHP mirip dengan pernyataan `while`, namun dengan perbedaan bahwa pernyataan dalam blok `do` akan dieksekusi setidaknya satu kali, bahkan jika kondisi pada awalnya salah.

Pernyataan `do-while` berguna ketika Anda ingin menjalankan blok pernyataan setidaknya sekali sebelum mengevaluasi kondisi untuk iterasi selanjutnya.
#### Struktur
```php
do {

    // blok kode yang akan diulang

    // perubahan kondisi harus dilakukan di dalam blok kode

} while (kondisi);
```
#### Program
```php
$i = 1;

do {

    echo $i;

    $i++;

} while ($i <= 5);
```
#### Hasil 
![h.do-while.png](Asetphp/h.do-while.png)
#### Analisis
1. `$i = 1;`: Variabel `$i` diinisialisasi dengan nilai 1 di luar pernyataan `do-while`. Ini menyiapkan variabel yang akan digunakan sebagai penghitung iterasi.
    
2. `do { ... }`: Ini adalah blok pernyataan yang akan dieksekusi setidaknya satu kali. Pada blok ini, kita mencetak nilai variabel `$i` menggunakan `echo`, dan kemudian nilai variabel `$i` ditambah satu.
    
3. `while ($i <= 5);`: Setelah blok pernyataan di dalam `do` selesai dieksekusi, kondisi iterasi dievaluasi. Jika kondisi (`$i <= 5`) benar, iterasi akan terus dilakukan, dan blok pernyataan dalam `do` akan dieksekusi lagi. Jika kondisi itu salah, iterasi berhenti, dan eksekusi program melanjutkan ke pernyataan setelah blok `do-while`.
#### Kesimpulan Program
- Program menggunakan pernyataan `do-while` untuk melakukan iterasi (pengulangan) setidaknya satu kali, bahkan jika kondisi pada awalnya salah.
- Variabel `$i` diinisialisasi dengan nilai 1 di luar pernyataan `do-while`.
- Blok pernyataan dalam `do` mencetak nilai variabel `$i` menggunakan `echo`, kemudian nilai variabel `$i` ditambah satu.
- Setelah blok pernyataan dalam `do` dieksekusi, kondisi iterasi (`$i <= 5`) dievaluasi. Jika kondisi ini benar, iterasi akan terus dilakukan, dan blok pernyataan dalam `do` akan dieksekusi lagi. Jika kondisi ini salah, iterasi berhenti, dan eksekusi program melanjutkan ke pernyataan setelah blok `do-while`.
- Hasilnya adalah program akan mencetak angka dari 1 hingga 5 secara berurutan karena kondisi `$i <= 5` terpenuhi. Meskipun nilai `$i` awalnya adalah 1 (dan tidak memenuhi kondisi pada awalnya), pernyataan `do-while` memastikan bahwa setidaknya satu iterasi akan dilakukan sebelum kondisi diuji kembali.
- Pernyataan `do-while` berguna ketika kita ingin menjalankan blok pernyataan setidaknya sekali sebelum mengevaluasi kondisi untuk iterasi selanjutnya.
### Foreach
#### Penjelasan
Pernyataan `foreach` dalam PHP digunakan untuk mengulang melalui setiap elemen dalam array atau objek. Ini memungkinkan Anda untuk mengakses nilai setiap elemen dalam array atau properti setiap objek secara langsung tanpa menggunakan indeks atau kunci
#### Struktur
```php
foreach ($array as $nilai) {

    // blok kode yang akan diulang

}
```
#### Program
```php
$nama = array("Rehan", "Frhan", "Ardi");

foreach ($nama as $namatrio) {

    echo $namatrio;

}
```
#### Hasil 
![h.frch.png](Asetphp/h.frch.png)
#### Analisis
1. Variabel `$nama` didefinisikan sebagai array yang berisi tiga elemen: "Rehan", "Frhan", dan "Ardi".
    
2. Pernyataan `foreach` digunakan untuk mengiterasi melalui setiap elemen dalam array `$nama`.
    
3. Pada setiap iterasi, nilai dari elemen saat ini disimpan dalam variabel `$namatrio`.
    
4. Dalam blok pernyataan `foreach`, nilai `$namatrio` dicetak menggunakan `echo`.
#### Kesimpulan Program
- Program menggunakan pernyataan `foreach` untuk mengiterasi melalui setiap elemen dalam array.
- Variabel `$nama` didefinisikan sebagai array yang berisi tiga elemen: "Rehan", "Frhan", dan "Ardi".
- Pernyataan `foreach` digunakan untuk mengiterasi melalui setiap elemen dalam array `$nama`.
- Pada setiap iterasi, nilai dari elemen saat ini disimpan dalam variabel `$namatrio`
- Dalam blok pernyataan `foreach`, nilai `$namatrio` dicetak menggunakan `echo`.
- Hasil eksekusi program ini akan mencetak semua nama yang ada dalam array `$nama`, yaitu "Rehan", "Frhan", dan "Ardi", tanpa spasi atau pemisah lain karena tidak ada karakter tambahan setelah `$namatrio` dalam pernyataan `echo`.




## Var dump

### Penjelasan
Dalam PHP, `var_dump()` adalah fungsi yang digunakan untuk menampilkan informasi mengenai variabel. Fungsi ini sangat berguna untuk debugging, karena dapat memberikan informasi rinci tentang jenis data dan nilai dari variabel apa pun.
### Struktur
```php

```
### Program
```php
<?php
$person = array(
    'nama' => 'John Doe',
    'umur' => 30,
    'email' => 'john@example.com'
);


$karyawan = array(
    array(
        'nama' => 'Alice',
        'departemen' => 'HR',
        'gaji' => 5000
    ),
);

// Menampilkan informasi array asosiatif
echo "Informasi array asosiatif:\n";
var_dump($person);
echo "\n";

// Menampilkan informasi array multidimensi
echo "Informasi array multidimensi:\n";
var_dump($karyawan);
?>

```
### Hasil
![h.var_dump.png](/Asetphp/h.var_dump.png)
### Analisis 
- Array `$person` memiliki tiga elemen: 'nama', 'umur', dan 'email', yang masing-masing memiliki nilai berupa nama, umur, dan email seorang individu.
- Array `$karyawan` merupakan array multidimensi yang berisi satu array lagi di dalamnya. Setiap elemen array di dalam `$karyawan` mewakili seorang karyawan dan memiliki tiga elemen: 'nama', 'departemen', dan 'gaji'.

Kemudian, program ini menggunakan fungsi `var_dump()` untuk menampilkan informasi tentang kedua array tersebut. Hasil dari `var_dump()` akan menampilkan informasi tentang struktur dan nilai dari setiap elemen array, termasuk tipe data dan panjang string (jika berlaku).
### Kesimpulan Program
- Array asosiatif digunakan untuk menyimpan pasangan kunci-nilai di mana kunci adalah string dan nilainya dapat berupa tipe data apa pun.
- Array multidimensi adalah array yang berisi satu atau lebih array di dalamnya. Hal ini memungkinkan kita untuk mengatur data dalam struktur yang lebih kompleks, seperti tabel atau matriks.
- Fungsi `var_dump()` digunakan untuk menampilkan informasi rinci tentang struktur dan nilai dari variabel, termasuk array. Ini adalah alat yang sangat berguna untuk debugging dalam pengembangan PHP karena membantu kita memahami struktur data dengan lebih baik.
## Function
### Penjelasan:**
Function dalam bahasa PHP adalah blok kode yang diberi nama dan digunakan untuk menjalankan tugas tertentu. Function memungkinkan kita untuk mengorganisir kode menjadi bagian yang terpisah dan dapat digunakan kembali di berbagai bagian dalam program. Dengan menggunakan function, kita dapat mengelompokkan kode yang memiliki fungsi serupa dan mempermudah pemeliharaan dan pengembangan program.

### *Struktur:*

### Kode Program
```php
function nama_function(parameter1, parameter2, ...) {
    // Blok kode yang dijalankan ketika function dipanggil
    // ...
    return nilai;
}

*Contoh Program:*
php
function tambah($a, $b) {
    $hasil = $a + $b;
    return $hasil;
}

$angka1 = 5;
$angka2 = 3;
$hasil_penjumlahan = tambah($angka1, $angka2);

echo "Hasil penjumlahan: " . $hasil_penjumlahan;
```

### *Hasil:*
![h.function.png](Asetphp/h.function.png)
### *Analisis:*
- Dalam contoh program di atas, kita mendefinisikan sebuah function bernama tambah yang menerima dua parameter $a dan $b.
- Di dalam function tambah, kita menambahkan nilai dari parameter $a dan $b dan menyimpan hasilnya di variabel $hasil.
- Kemudian, kita mengembalikan nilai $hasil menggunakan pernyataan return.
- Di luar function, kita mendefinisikan dua variabel $angka1 dan $angka2 yang akan digunakan sebagai argumen saat memanggil function tambah.
- Hasil penjumlahan dari function tambah disimpan di variabel $hasil_penjumlahan.
- Akhirnya, kita mencetak hasil penjumlahan menggunakan pernyataan echo.
### *Kesimpulan:*
Program ini menggunakan function tambah untuk menjumlahkan dua angka dan mencetak hasilnya. Penggunaan function memungkinkan kita untuk mengorganisir kode menjadi blok yang terpisah dan dapat digunakan kembali. Keuntungan menggunakan function antara lain:
- Modularitas: Kode penjumlahan dipisahkan ke dalam function tambah, sehingga memudahkan pemeliharaan dan pengembangan kode. Jika ada perubahan pada logika penjumlahan, kita hanya perlu memodifikasi function tambah, bukan seluruh program.
- Reusabilitas: Function tambah dapat dipanggil berkali-kali dengan argumen yang berbeda. Kita dapat menggunakan kembali function ini di berbagai bagian program yang membutuhkan operasi penjumlahan.
- Keterbacaan: Penggunaan function dengan nama yang deskriptif, seperti tambah, membuat kode lebih mudah dipahami dan mempermudah pemahaman terhadap fungsi yang dilakukan oleh blok kode tersebut.

## PHP
### Get Method
#### Penjelasan
Metode GET dalam PHP adalah salah satu metode HTTP yang digunakan untuk mengirim data dari klien (browser) ke server. Data yang dikirim dengan metode GET ditambahkan ke URL sebagai parameter, yang membuatnya terlihat di address bar browser. Metode ini umumnya digunakan untuk mengambil data dari server tanpa mengubahnya, seperti saat melakukan pencarian di mesin pencari atau mengambil informasi dari database berdasarkan query.
#### Struktur
```php

```
#### Kode Program
**From get**
```php

<!DOCTYPE html>

<html lang="en">

  

<head>

    <title>Document</title>

</head>

  

<body>

    <!-- Pada atribut action, kalian tuliskan nama file php yang bertugas untuk mengelola atau menangkap data dari form tersebut. -->

    <form action="proses_get.php" method="GET">

        <input type="text" name="nama_lengkap" placeholder="Masukkan nama">

        <input type="number" name="umur" placeholder="Masukkan umur"> <br>

        <button type="submit">Kirim</button>

    </form>

</body>

  

</html>

```

**Proses get**
```php
<?php

// Key dari array-nya, sesuai dengan nama dari atribut name di setiap input-nya

$nama = $_GET["nama_lengkap"];

$umur = $_GET["umur"];

?>

  

var_dump$_GET

  

<!DOCTYPE html>

<html lang="en">

  

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Ariq Hikari Hidayat - XI RPL 2 - GET</title>

</head>

  

<body>

    <p>Nama anda

        <!-- Ini adalah versi singkatnya dari php echo,

             yang fungsinya untuk menampilkan data -->

        <?= $nama ?>

    </p>

    <p>Umur anda <?= $umur ?> tahun</p>

</body>

  

</html>
```

#### Hasil
![h.method.png](Asetphp/h.method.png)

![h.get.png](Asetphp/h.get.png)

#### Analisis
- **Form**:
    - Form ini menggunakan metode GET untuk mengirim data ke `proses_get.php` ketika tombol "Kirim" diklik.
    - Input pertama adalah text input untuk memasukkan nama lengkap, dengan atribut `name="nama_lengkap"`.
    - Input kedua adalah number input untuk memasukkan umur, dengan atribut `name="umur"`.
    - Tombol submit mengirim data dari kedua input tersebut ke `proses_get.php`.


- **Mengambil Data GET**:
    
    - `$_GET["nama_lengkap"]` mengambil nilai dari parameter `nama_lengkap` yang dikirim melalui URL.
    - `$_GET["umur"]` mengambil nilai dari parameter `umur` yang dikirim melalui URL.
- **Menampilkan Isi GET**:
    
    - `var_dump($_GET)` menampilkan semua data yang diterima melalui metode GET untuk tujuan debugging. Ini akan menampilkan array asosiatif yang berisi kunci dan nilai dari data yang dikirimkan.
- **Menggunakan Data di HTML**:
    
    - Data yang diterima dari `$_GET` digunakan untuk ditampilkan di dalam HTML.
    - `<?= htmlspecialchars($nama) ?>` adalah shorthand dari `<?php echo htmlspecialchars($nama); ?>` untuk menampilkan nama yang dikirim.
    - `<?= htmlspecialchars($umur) ?>` menampilkan umur yang dikirim.
    - `htmlspecialchars()` digunakan untuk menghindari serangan XSS dengan mengonversi karakter khusus menjadi entitas HTML.


#### Kesimpulan
1. **Form HTML**:
    
    - Menggunakan metode GET untuk mengirimkan data ke `proses_get.php`.
    - Memiliki input untuk nama lengkap dan umur.
2. **Proses PHP**:
    
    - Mengambil data yang dikirim melalui URL menggunakan `$_GET`.
    - Menampilkan data yang diterima dengan `var_dump()` untuk debugging.
    - Menggunakan data tersebut untuk menampilkan pesan di halaman HTML.
3. **Keamanan**:
    
    - Menggunakan `htmlspecialchars()` untuk mencegah serangan XSS saat menampilkan data yang dikirim oleh pengguna.

### Post Method
#### Penjelasan
Metode POST adalah salah satu cara untuk mengirimkan data dari klien (seperti browser web) ke server web. Metode ini sering digunakan dalam formulir HTML ketika data perlu dikirim ke server untuk diproses, seperti dalam kasus pendaftaran pengguna, pengiriman komentar, dan sebagainya.
#### Struktur
```php

```

#### Kode Program
**Form posh
```php

<!DOCTYPE html>

<html lang="en">

  

<head>

    <title>Document</title>

</head>

  

<body>

    <!-- Pada atribut action, kalian tuliskan nama file php yang bertugas untuk mengelola atau menangkap data dari form tersebut. -->

    <form action="proses_posh.php" method="POST">

        <input type="text" name="nama_lengkap" placeholder="Masukkan nama">

        <input type="number" name="umur" placeholder="Masukkan umur">

        <input type="password" name="password" placeholder="Masukkan password"><br>

        <button type="submit">Kirim</button>

    </form>

</body>

  

</html>

```

proses posh
```php

<?php

// Key dari array-nya, sesuai dengan nama dari atribut name di setiap input-nya

//$nama = $_GET["nama"];

$umur = $_POST["umur"];

  

var_dump($_POST);

  

?>

  

<!DOCTYPE html>

<html lang="en">

  

<head>

    <title> XI RPL 1 - POST</title>

</head>

  

<body>

    <p>Nama anda <?= $_POST["nama_lengkap"] ?></p>

    <p>Umur anda <?= $umur ?> tahun</p>

    <p>Password anda aman!</p>

</body>

  

</html>

```
#### Hasil
![h.posh.png](Asetphp/h.posh.png)

![h.posh1.png](Asetphp/h.posh1.png)
#### Analisis
- **Form**:
    - Form ini menggunakan metode POST untuk mengirim data ke `proses_posh.php` ketika tombol "Kirim" diklik.
    - Input pertama adalah text input untuk memasukkan nama lengkap, dengan atribut `name="nama_lengkap"`.
    - Input kedua adalah number input untuk memasukkan umur, dengan atribut `name="umur"`.
    - Input ketiga adalah password input untuk memasukkan kata sandi, dengan atribut `name="password"`.
    - Tombol submit mengirim data dari ketiga input tersebut ke `proses_posh.php`.


- **Mengambil Data POST**:
    
    - `$_POST["nama_lengkap"]` mengambil nilai dari parameter `nama_lengkap` yang dikirim melalui form.
    - `$_POST["umur"]` mengambil nilai dari parameter `umur` yang dikirim melalui form.
    - `$_POST["password"]` mengambil nilai dari parameter `password` yang dikirim melalui form (meskipun tidak ditampilkan dalam output).
- **Menampilkan Isi POST**:
    
    - `var_dump($_POST)` menampilkan semua data yang diterima melalui metode POST untuk tujuan debugging. Ini akan menampilkan array asosiatif yang berisi kunci dan nilai dari data yang dikirimkan.
- **Menggunakan Data di HTML**:
    
    - Data yang diterima dari `$_POST` digunakan untuk ditampilkan di dalam HTML.
    - `<?= htmlspecialchars($_POST["nama_lengkap"]) ?>` adalah shorthand dari `<?php echo htmlspecialchars($_POST["nama_lengkap"]); ?>` untuk menampilkan nama yang dikirim.
    - `<?= htmlspecialchars($umur) ?>` menampilkan umur yang dikirim.
    - `htmlspecialchars()` digunakan untuk menghindari serangan XSS dengan mengonversi karakter khusus menjadi entitas HTML.

#### Kesimpulan Program
1. **Form HTML**:
    
    - Menggunakan metode POST untuk mengirimkan data ke `proses_posh.php`.
    - Memiliki input untuk nama lengkap, umur, dan password.
2. **Proses PHP**:
    
    - Mengambil data yang dikirim melalui metode POST menggunakan `$_POST`.
    - Menampilkan data yang diterima dengan `var_dump()` untuk debugging.
    - Menggunakan data tersebut untuk menampilkan pesan di halaman HTML.
3. **Keamanan**:
    
    - Menggunakan `htmlspecialchars()` untuk mencegah serangan XSS saat menampilkan data yang dikirim oleh pengguna.
    - Menyembunyikan data sensitif (seperti password) dari tampilan.


# Koneksi
## Kode Program 
```php
<?php

//koneksi ke database

$koneksi = mysqli_connect('localhost', 'root', '', 'rental_mobil');

  

if ($koneksi) {

    echo "<br> koneksi aman <br>";

} else {

    echo "error, tidak bisa koneksi ke database";

}
```
## Hasil
![h.koneksi.jpeg](Asetphp/h.koneksi.jpeg)

## Analisis
Program PHP di atas adalah skrip sederhana untuk menghubungkan aplikasi PHP ke database MySQL. Berikut adalah analisis detail dari kode tersebut:

1. **Membuat Koneksi ke Database:**
    ```php
    $koneksi = mysqli_connect('localhost', 'root', '', 'rental_mobil');
    ```
    Fungsi `mysqli_connect()` digunakan untuk membuat koneksi ke database MySQL. Fungsi ini membutuhkan empat parameter:
    - `'localhost'`: Menunjukkan bahwa server MySQL berjalan di komputer lokal.
    - `'root'`: Nama pengguna (user) untuk database. Biasanya, pengguna default adalah 'root'.
    - `''`: Kata sandi (password) untuk pengguna database. Dalam contoh ini, password tidak diisi (kosong).
    - `'rental_mobil'`: Nama database yang ingin dihubungkan.

2. **Memeriksa Koneksi:**
    ```php
    if ($koneksi) {
        echo "<br> koneksi aman <br>";
    } else {
        echo "error, tidak bisa koneksi ke database";
    }
    ```
    Kode ini memeriksa apakah koneksi ke database berhasil atau tidak:
    - Jika `$koneksi` mengembalikan nilai benar (true), maka koneksi berhasil, dan pesan "koneksi aman" akan ditampilkan.
    - Jika `$koneksi` mengembalikan nilai salah (false), maka koneksi gagal, dan pesan "error, tidak bisa koneksi ke database" akan ditampilkan.

**Analisis Tambahan:**
- **Keamanan:**
  - Menyimpan kata sandi dalam bentuk teks biasa (plain text) di dalam kode tidak aman. Sebaiknya, gunakan metode yang lebih aman untuk mengelola kredensial, seperti file konfigurasi yang di luar direktori web atau menggunakan variabel lingkungan (environment variables).
  - `root` adalah akun default MySQL yang memiliki hak istimewa penuh. Sebaiknya, buat akun pengguna khusus dengan hak terbatas untuk aplikasi Anda.

- **Kesalahan Koneksi:**
  - Akan lebih baik jika menampilkan pesan kesalahan spesifik menggunakan `mysqli_connect_error()` untuk membantu debug jika koneksi gagal. Contoh:
    ```php
    if (!$koneksi) {
        die("Koneksi gagal: " . mysqli_connect_error());
    }
    ```

- **Penanganan Koneksi:**
  - Setelah menggunakan koneksi, selalu pastikan untuk menutup koneksi dengan `mysqli_close($koneksi)` untuk menghemat sumber daya.

Berikut adalah versi yang ditingkatkan dari kode Anda:
```php
<?php

// Koneksi ke database
$koneksi = mysqli_connect('localhost', 'root', '', 'rental_mobil');

if (!$koneksi) {
    die("Koneksi gagal: " . mysqli_connect_error());
}

echo "<br> koneksi aman <br>";

// Setelah operasi selesai, tutup koneksi
mysqli_close($koneksi);
```

Dengan demikian, program ini menghubungkan aplikasi ke database MySQL, memeriksa apakah koneksi berhasil, dan menampilkan pesan yang sesuai. Kode yang ditingkatkan juga menyediakan penanganan kesalahan yang lebih baik dan menghemat sumber daya dengan menutup koneksi setelah selesai digunakan.
## Kesimpulan
1. **Tujuan Kode:**
    
    - Kode PHP ini bertujuan untuk membuat koneksi ke database MySQL yang bernama 'rental_mobil'.
2. **Cara Kerja:**
    
    - Menggunakan fungsi `mysqli_connect()` untuk mencoba menghubungkan aplikasi ke database.
    - Memeriksa apakah koneksi berhasil atau gagal dan menampilkan pesan yang sesuai.
3. **Penanganan Keberhasilan dan Kegagalan:**
    
    - Jika koneksi berhasil, menampilkan pesan "koneksi aman".
    - Jika koneksi gagal, menampilkan pesan "error, tidak bisa koneksi ke database".
4. **Keamanan:**
    
    - Menggunakan nama pengguna 'root' dan tanpa kata sandi, yang merupakan praktik kurang aman. Dianjurkan menggunakan nama pengguna dengan hak akses terbatas dan menyimpan kata sandi dengan cara yang lebih aman.
5. **Peningkatan Kode:**
    
    - Menambahkan penanganan kesalahan yang lebih baik dengan `mysqli_connect_error()` untuk mendapatkan pesan kesalahan yang lebih informatif.
    - Menutup koneksi setelah selesai menggunakan `mysqli_close($koneksi)` untuk menghemat sumber daya.

# Tampilkan Data

## Kode Program
```php mysql
<?php

  

//koneksi ke database

$koneksi = mysqli_connect('localhost', 'root', '', 'rental_raihan');

  

if ($koneksi) {

    echo "<br> koneksi aman <br>";

} else {

    echo "error, tidak bisa koneksi ke database";

}

//jalankan query seleksi

$select = mysqli_query($koneksi, "SELECT * FROM daftar_mobil");

  

//membuat array asosiatif dan memecah data berdasarkan kolomnya

$result = mysqli_fetch_assoc($select);

  

//menampilkan struktur array dari data tabel yang dijalankan di atas

//var_dump($result);

  

echo 'Berikut mobil-mobil beserta pemiliknya<br>';

  

$a = 1;

foreach ($select as $key => $data) {

    echo $a++ . ". " . $data['no_plat'] . " : " . $data['pemilik'] . '<br>';

}

  

//echo '<p>Halo ' . $result['pemilik'] . '!!</p><br>'
```

## Hasil
![h.knks.png](Asetphp/h.knks.png)
## Analisis
Program PHP di atas adalah skrip untuk menghubungkan ke database MySQL, menjalankan query, dan menampilkan hasil dari tabel `daftar_mobil`. Berikut adalah analisis rinci dari setiap bagian kode tersebut:

1. **Koneksi ke Database:**
    ```php
    $koneksi = mysqli_connect('localhost', 'root', '', 'rental_raihan');

    if ($koneksi) {
        echo "<br> koneksi aman <br>";
    } else {
        echo "error, tidak bisa koneksi ke database";
    }
    ```
    - Fungsi `mysqli_connect()` digunakan untuk membuat koneksi ke database MySQL. Parameter yang digunakan adalah:
      - `'localhost'`: Server database lokal.
      - `'root'`: Nama pengguna database.
      - `''`: Kata sandi pengguna (kosong dalam kasus ini).
      - `'rental_raihan'`: Nama database.
    - Koneksi diperiksa dengan kondisi if. Jika berhasil, mencetak "koneksi aman", jika gagal, mencetak pesan kesalahan.

2. **Jalankan Query Seleksi:**
    ```php
    $select = mysqli_query($koneksi, "SELECT * FROM daftar_mobil");
    ```
    - Fungsi `mysqli_query()` digunakan untuk menjalankan query SQL yang memilih semua data dari tabel `daftar_mobil`.

3. **Membuat Array Asosiatif:**
    ```php
    $result = mysqli_fetch_assoc($select);
    ```
    - Fungsi `mysqli_fetch_assoc()` digunakan untuk mengambil baris hasil query sebagai array asosiatif. Namun, hasil ini tidak digunakan lebih lanjut dalam kode.

4. **Menampilkan Struktur Array:**
    ```php
    //var_dump($result);
    ```
    - Baris ini dikomentari, tetapi jika diaktifkan, `var_dump($result)` akan menampilkan struktur dan isi dari array `$result`.

5. **Menampilkan Data:**
    ```php
    echo 'Berikut mobil-mobil beserta pemiliknya<br>';

    $a = 1;
    foreach ($select as $key => $data) {
        echo $a++ . ". " . $data['no_plat'] . " : " . $data['pemilik'] . '<br>';
    }
    ```
    - Menampilkan pesan awal.
    - Menggunakan loop `foreach` untuk iterasi hasil query (`$select`) dan menampilkan data nomor plat (`no_plat`) dan pemilik (`pemilik`) dari setiap baris.
    - Variabel `$a` digunakan untuk membuat nomor urut.

## Kesimpulan
- **Koneksi Database:** Koneksi ke database dilakukan dengan benar, dan hasilnya diperiksa.
- **Eksekusi Query:** Query SQL dijalankan untuk mengambil data dari tabel `daftar_mobil`.
- **Pengambilan dan Penampilan Data:** Hasil query diambil dan ditampilkan dalam format yang ramah pengguna.


# Tambahkan Data

## Program
```php
<?php

// Koneksi ke database

$koneksi = mysqli_connect('localhost', 'root', '', 'rental_raihan');

  

// Cek koneksi

if ($koneksi) {

    echo "<br>Koneksi berhasil<br>";

} else {

    die("Error, tidak bisa koneksi ke database: " . mysqli_connect_error());

}

  

// Jalankan query seleksi

$select = mysqli_query($koneksi, "SELECT * FROM daftar_mobil");

  

// Cek apakah query berhasil

if (!$select) {

    die("Error dalam menjalankan query: " . mysqli_error($koneksi));

}

  

// Mengambil semua data hasil query

$dataMobil = mysqli_fetch_all($select, MYSQLI_ASSOC);

  

// Menampilkan data

echo 'Berikut mobil-mobil beserta pemiliknya:<br>';

  

$a = 1;

foreach ($dataMobil as $data) {

    echo $a++ . ". " . htmlspecialchars($data['no_plat']) . " : " . htmlspecialchars($data['pemilik']) . '<br>';

}

  

// Tutup koneksi

mysqli_close($koneksi);

?>
```
## Hasil
![h.ubahdata.png](Asetphp/h.ubahdata.png)
## Analisis
```php mysql
$koneksi = mysqli_connect('localhost', 'root', '', 'rental_raihan');

// Cek koneksi
if ($koneksi) {
    echo "<br>Koneksi berhasil<br>";
} else {
    die("Error, tidak bisa koneksi ke database: " . mysqli_connect_error());
}

```
- **Analisis**: Program ini pertama-tama melakukan koneksi ke server database MySQL yang berjalan lokal (`localhost`) dengan menggunakan nama pengguna (`root`) dan tanpa kata sandi (`''`). Database yang dipilih adalah `rental_raihan`.
- **Fungsi**: `mysqli_connect` digunakan untuk menginisialisasi koneksi ke database. Jika koneksi berhasil, pesan "Koneksi berhasil" akan ditampilkan. Jika tidak berhasil, program akan berhenti dan menampilkan pesan error dengan `die`.

```php mysql
$select = mysqli_query($koneksi, "SELECT * FROM daftar_mobil");

// Cek apakah query berhasil
if (!$select) {
    die("Error dalam menjalankan query: " . mysqli_error($koneksi));
}

```
- **Analisis**: Program ini menjalankan query SQL `SELECT * FROM daftar_mobil` menggunakan `mysqli_query` untuk mengambil semua data dari tabel `daftar_mobil`.
- **Fungsi**: Setelah menjalankan query, program memeriksa apakah query berhasil dieksekusi. Jika tidak berhasil, program akan berhenti dan menampilkan pesan error menggunakan `die`.

```php mysql
$dataMobil = mysqli_fetch_all($select, MYSQLI_ASSOC);
```
- **Analisis**: Program ini mengambil semua baris hasil query yang disimpan dalam variabel `$select` menggunakan `mysqli_fetch_all`. Mode `MYSQLI_ASSOC` digunakan untuk mengembalikan data sebagai array asosiatif.
- **Fungsi**: Ini memungkinkan program untuk bekerja dengan data hasil query dalam bentuk array yang dapat diiterasi.

```php mysql
echo 'Berikut mobil-mobil beserta pemiliknya:<br>'; $a = 1; foreach ($dataMobil as $data) {     echo $a++ . ". " . htmlspecialchars($data['no_plat']) . " : " . htmlspecialchars($data['pemilik']) . '<br>'; }
```
- **Analisis**: Program ini menggunakan perulangan `foreach` untuk menampilkan data mobil dan pemiliknya yang sudah diambil dari tabel `daftar_mobil`. Setiap baris data ditampilkan dengan nomor urut dan menggunakan fungsi `htmlspecialchars` untuk mencegah injeksi HTML.
- **Fungsi**: Ini memastikan bahwa data yang ditampilkan aman dari karakter khusus HTML yang dapat memengaruhi tampilan halaman.

```php mysql
mysqli_close($koneksi);
```
- **Analisis**: Program ini menutup koneksi ke database setelah selesai menggunakan `mysqli_close`.
- **Fungsi**: Menutup koneksi membantu mengelola sumber daya dengan baik dan mencegah koneksi yang tidak perlu terbuka.
## Kesimpulan
Program PHP MySQL di atas adalah contoh sederhana penggunaan MySQL dalam PHP untuk terhubung ke database, menjalankan query untuk mengambil data, dan menampilkan hasilnya dalam halaman web. Ini juga menunjukkan praktik baik dalam menangani koneksi database, menjalankan query, dan menampilkan data dengan aman. Penting untuk memahami dan menerapkan prinsip-prinsip ini untuk membangun aplikasi web yang aman dan efisien.
# Ubah Data
## **Kode Program:**
```php
<?php

  

//koneksi ke database

  

$koneksi = mysqli_connect('localhost', 'root', '', 'rental_raihan');

  

if ($koneksi)  echo "<br> koneksi aman <br>";

 else { echo "error, tidak bisa koneksi ke database"; }

// Mengubah data dengan nomor plat tertentu

$no_plat_lama = "DD 2440 AX";

  

$no_plat_baru = "AB 1234 CD";

  

$pemilik_baru = "Jamil";

  

$update = mysqli_query($koneksi, "UPDATE daftar_mobil SET no_plat = '$no_plat_baru', pemilik = '$pemilik_baru' WHERE no_plat = '$no_plat_lama'");

  

if ($update) { echo "Data dengan nomor plat $no_plat_lama berhasil diubah menjadi nomor plat $no_plat_baru dengan pemilik $pemilik_baru";

  

} else { echo "Gagal mengubah data dengan nomor plat $no_plat_lama"; }

  

?>
```

## **Hasil:**
![ubahda.png](Asetphp/ubahda.png)
## **Analisis:**
1. Koneksi ke Database
```php
$koneksi = mysqli_connect('localhost', 'root', '', 'rental_raihan');  if ($koneksi) {     echo "<br> koneksi aman <br>"; } else {     echo "error, tidak bisa koneksi ke database"; }
```
- **Analisis**: Program ini menggunakan `mysqli_connect` untuk melakukan koneksi ke database MySQL yang berjalan lokal (`localhost`) dengan nama pengguna (`root`) dan tanpa kata sandi (`''`). Database yang digunakan adalah `rental_raihan`.
- **Fungsi**: Jika koneksi berhasil, pesan "koneksi aman" akan ditampilkan. Jika tidak, pesan error "error, tidak bisa koneksi ke database" akan muncul.

2. Mengubah Data dengan Nomor Plat Tertentu
```php
$no_plat_lama = "DD 2440 AX"; $no_plat_baru = "AB 1234 CD"; $pemilik_baru = "Jamil";  $update = mysqli_query($koneksi, "UPDATE daftar_mobil SET no_plat = '$no_plat_baru', pemilik = '$pemilik_baru' WHERE no_plat = '$no_plat_lama'");`
```
- **Analisis**: Program ini menjalankan query SQL `UPDATE` menggunakan `mysqli_query` untuk mengubah data dalam tabel `daftar_mobil`. Data yang diubah adalah nomor plat (`no_plat`) dan pemilik (`pemilik`) dari entri yang memiliki nomor plat lama (`$no_plat_lama`) menjadi nomor plat baru (`$no_plat_baru`) dan pemilik baru (`$pemilik_baru`).
- **Fungsi**: Query ini bertujuan untuk mengupdate data di database berdasarkan kondisi tertentu (`WHERE no_plat = '$no_plat_lama'`). Variabel `$update` akan menyimpan hasil dari query tersebut (berupa `true` jika berhasil, atau `false` jika gagal).

### 3. Menampilkan Pesan Berhasil atau Gagal
```php
`if ($update) {     echo "Data dengan nomor plat $no_plat_lama berhasil diubah menjadi nomor plat $no_plat_baru dengan pemilik $pemilik_baru"; } else {     echo "Gagal mengubah data dengan nomor plat $no_plat_lama"; }`

```

- **Analisis**: Setelah menjalankan query `UPDATE`, program memeriksa apakah query berhasil dieksekusi dengan memeriksa nilai `$update`. Jika `$update` bernilai `true`, program akan menampilkan pesan bahwa data berhasil diubah dengan nomor plat dan pemilik baru. Jika `$update` bernilai `false`, program akan menampilkan pesan bahwa gagal mengubah data dengan nomor plat lama.
- **Fungsi**: Ini memberikan feedback kepada pengguna atau pengembang mengenai hasil operasi SQL yang dilakukan.

## **Kesimpulan:**
Program PHP dan SQL di atas berfungsi untuk melakukan koneksi ke database, menjalankan query seleksi, menampilkan data sebelum perubahan, mengubah data dalam tabel "daftar_mobil", dan menampilkan data setelah perubahan. Program ini akan menampilkan nama-nama pemilik mobil sebelum dan setelah perubahan yang dilakukan. Pastikan koneksi ke database telah berhasil dan struktur tabel "daftar_mobil" sesuai sebelum menjalankan program ini. Perhatikan bahwa program ini mengubah data pemilik mobil dengan nomor plat lama tertentu menjadi pemilik baru yang ditetapkan. Anda dapat mengubah nilai variabel `$no_plat_lama` dan `$pemilik_baru` sesuai dengan data yang ingin diubah.

# Hapus Data

## **Kode Program:**

```html
<?php

// Koneksi ke database
$koneksi = mysqli_connect('localhost', 'root', '', 'rental_rahmat');

  
if ($koneksi) {
    echo "<br> Koneksi aman <br>";
} else {
    echo "Error, tidak bisa koneksi ke database";
}
  
// Jalankan query seleksi
$select = mysqli_query($koneksi, "SELECT * FROM daftar_mobil");
echo 'Berikut nama-nama pemilik mobil sebelum penghapusan<br>';

$a = 1;
foreach ($select as $key => $data) {
    echo $a++ . ", " . $data['no_plat'] . " : " . $data['pemilik'] . '<br>';
}


// Hapus data dalam tabel daftar_mobil
$no_plat_hapus = "AB 1234 CD";

$delete = mysqli_query($koneksi, "DELETE FROM daftar_mobil WHERE no_plat='$no_plat_hapus'");
  
if ($delete) {
    echo "Data berhasil dihapus<br>";
} else {
    echo "Gagal menghapus data";
}

  
// Jalankan query seleksi setelah penghapusan
$select_after_delete = mysqli_query($koneksi, "SELECT * FROM daftar_mobil");
  
echo 'Berikut nama-nama pemilik mobil setelah penghapusan<br>';
  
$a = 1;
foreach ($select_after_delete as $key => $data) {
    echo $a++ . ", " . $data['no_plat'] . " : " . $data['pemilik'] . '<br>';
}
  
?>
```

## **Hasil:**
![hps.png](Asetphp/hps.png)
## **Analisis:**
 1. Koneksi ke Database
```mysql
`// Koneksi ke database $koneksi = mysqli_connect('localhost', 'root', '', 'rental_raihan');  if ($koneksi) {     echo "<br> koneksi aman <br>"; } else {     echo "error, tidak bisa koneksi ke database"; }`

```

- **Analisis**: Program ini menggunakan fungsi `mysqli_connect` untuk menghubungkan PHP ke server database MySQL yang berjalan di `localhost`. Penggunaan `root` sebagai nama pengguna dan tidak ada kata sandi (`''`) menunjukkan koneksi dengan pengaturan default. Pesan "koneksi aman" ditampilkan jika koneksi berhasil, dan pesan error ditampilkan jika gagal.
- **Fungsi**: Ini adalah langkah awal yang penting untuk memastikan aplikasi web dapat terhubung ke basis data yang diperlukan untuk operasi selanjutnya.

2. Mengubah Data dengan Nomor Plat Tertentu
```mysql
// Mengubah data dengan nomor plat tertentu $no_plat_lama = "DD 2440 AX"; $no_plat_baru = "AB 1234 CD"; $pemilik_baru = "Jamil";  $update = mysqli_query($koneksi, "UPDATE daftar_mobil SET no_plat = '$no_plat_baru', pemilik = '$pemilik_baru' WHERE no_plat = '$no_plat_lama'");  if ($update) {     echo "Data dengan nomor plat $no_plat_lama berhasil diubah menjadi nomor plat $no_plat_baru dengan pemilik $pemilik_baru"; } else {     echo "Gagal mengubah data dengan nomor plat $no_plat_lama"; }`

```

- **Analisis**: Program ini menggunakan `mysqli_query` untuk menjalankan query SQL `UPDATE`. Query ini bertujuan untuk mengubah data dalam tabel `daftar_mobil` di mana nomor plat (`no_plat`) sama dengan `$no_plat_lama`. Data diubah dengan menetapkan nilai baru untuk `no_plat` dan `pemilik`.
- **Fungsi**: Variabel `$update` akan berisi hasil dari eksekusi query. Jika query berhasil dieksekusi, program akan memberikan respons bahwa data telah berhasil diubah dengan nomor plat dan pemilik baru. Jika query gagal, program akan memberikan pesan bahwa pengubahan data tidak berhasil.
## **Kesimpulan:**
Program PHP dan SQL di atas berfungsi untuk melakukan koneksi ke database, menjalankan query seleksi, menampilkan data sebelum penghapusan, menghapus data dalam tabel "daftar_mobil", dan menampilkan data setelah penghapusan. Program ini akan menampilkan nama-nama pemilik mobil sebelum dan setelah penghapusan yang dilakukan. Pastikan koneksi ke database telah berhasil dan struktur tabel "daftar_mobil" sesuai sebelum menjalankan program ini. Perhatikan bahwa program ini menghapus data dengan nomor plat tertentu yang ditentukan oleh nilai variabel `$no_plat_hapus`. Anda dapat mengubah nilai variabel tersebut sesuai dengan nomor plat yang ingin dihapus.

# Session/Login
## **Kode Program:**
```php
<?php

session_start();
  
//$username = "Jordan";
//$alamat = "Pampang";
  
//$_SESSION['$username'] = $username;
//$_SESSION['alamat'] = $alamat;
  
if (isset ($_POST['submit'])){
    $username = $_POST['username'];
    $password = $_POST['password'];
    $koneksi = mysqli_connect('localhost', 'root', '', 'latihan_rpl_1') or die('error koneksi');
    $result = mysqli_query($koneksi, "SELECT * FROM user
                            WHERE username = '$username' AND password = '$password'");
  
    $data = mysqli_fetch_assoc($result);
    var_dump($data);
    
    if (isset($data)){
        $_SESSION['username'] = $data['username'];
        $_SESSION['nama'] = $data['nama'];
        $_SESSION['status'] = 'login';
        header('Location: user.php');
    } else {
        echo "Username dan Password Salah";
    }

    }
  
?>
  
<!DOCTYPE html>
<html lang="en">
<head>
    <title>SessionLogin</title>
</head>
<body>
    <form method="post">
        <label for="">username</label>
        <input type="text" name="username">
        <br>
        <label for="">password</label>
        <input type="password" name="password">
        <br>
        <button type="submit" name="submit">Login</button>
    </form>
</body>
</html>
```

```php
<?php

session_start();
  
if ($_SESSION['status'] == 'login' && $_SESSION['username'] == 'admin') {
    header("Location: admin.php");
}
if ($_SESSION['status'] != 'login') {
    header('Location: session.php');
}
  
?>
<!DOCTYPE html>
<html lang="en">
  
<head>
    <title>Document</title>
</head>
<body>
    <h1>Halaman User</h1>
    <h1>Halo, <?= $_SESSION['nama'] ?></h1>
    <a href="logout.php">Logout</a>
</body>
</html>
```

```php
<?php
  
if ($_SESSION['status'] == 'login' && $_SESSION['username'] != 'admin') {
    header("Location: user.php");
    exit();
} else if ($_SESSION['status'] == 'login' && $_SESSION['username'] == 'admin') {
    header("Location: admin.php");
}else{
    header("Location: session.php");
}
```

```ph
<?php

session_start();
  
if ($_SESSION['status'] == 'login' && $_SESSION['username'] != 'admin') {
    header("Location: user.php");
}
  
if ($_SESSION['status'] != 'login') {
    header('Location: session.php');
}
  
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    <h1>Halaman Admin</h1>
    <h1>Halo, <?= $_SESSION['nama'] ?></h1>
    <a href="logout.php">Logout</a>
</body>
</html>
```

## **Hasil:**
![hasil.png](Asetphp/hasil.png)

![hasill.png](Asetphp/hasill.png)

## **Analisis:**
1. Pada bagian PHP:
    - Program memulai session dengan menggunakan fungsi `session_start()`. Hal ini penting untuk memulai dan mengelola session di PHP.
    - Jika terdapat data yang dikirimkan melalui metode POST dengan nama "submit" (diperiksa menggunakan `isset($_POST['submit'])`), maka program akan melakukan proses login.
    - Data username dan password yang dikirimkan melalui form diambil menggunakan `$_POST['username']` dan `$_POST['password']`.
    - Dilakukan koneksi ke database MySQL menggunakan `mysqli_connect()` dengan parameter host, username, password, dan nama database.
    - Dilakukan query SQL untuk mencocokkan data username dan password yang diberikan dengan data di tabel "user" menggunakan perintah `mysqli_query()`.
    - Hasil query diambil menggunakan `mysqli_fetch_assoc()` dan disimpan dalam variabel `$data`.
    - Hasil dari `$data` ditampilkan menggunakan `var_dump()` untuk tujuan debugging.
    - Jika `$data` memiliki nilai (artinya username dan password cocok), maka session akan diset dengan variabel-variabel dari data tersebut, dan pengguna akan diarahkan ke halaman "user.php" menggunakan `header('Location: user.php')`.
    - Jika tidak ada data yang cocok, maka akan ditampilkan pesan "Username dan Password Salah".
2. Pada bagian HTML:
    - Terdapat sebuah form dengan metode POST.
    - Form tersebut memiliki input field untuk username dan password.
    - Terdapat tombol "Login" yang akan mengirimkan data form saat ditekan.

## **Kesimpulan:**
File `session.php` adalah program PHP yang melakukan proses login menggunakan session. Program ini memeriksa apakah data username dan password yang diberikan cocok dengan data yang ada di database. Jika cocok, session akan diset dengan variabel-variabel dari data tersebut dan pengguna akan diarahkan ke halaman "user.php". Jika tidak cocok, pesan kesalahan akan ditampilkan. Namun, perlu diperhatikan bahwa file ini belum mengimplementasikan fitur keamanan seperti sanitasi input dan penggunaan prepared statement untuk mencegah serangan SQL Injection.

# Upload & Download

## Upload

### **Kode Program:**
```html
<!DOCTYPE html>
<html lang="en">
  
<head>
    <title>Document</title>
</head>
  
<body>
    <h2>Tambah Data</h2>
    <form method="post" enctype="multipart/form-data">
        <table>
            <tr>
                <td>Nama</td>
                <td><input type="text" name="nama"></td>
            </tr>
            <tr>
                <td>Email</td>
                <td><input type="text" name="email"></td>
            </tr>
            <tr>
                <td>Jenis Kelamin</td>
                <td>>
                    <select name="jenis_kelamin">
                        <option>Laki-laki</option>
                        <option>Perempuan</option>
                    </select>
                </td>
            </tr>
            <tr>
                <td>Alamat</td>
                <td><input type="text" name="alamat"></td>
            </tr>
            <tr>
                <td>Gambar</td>
                <td><input type="file" name="gambar"></td>
            </tr>
            <tr>
                <td></td>
                <td>
                    <button name="simpan" type="submit">Simpan</button>
                    <button type="reset">Reset</button>
                    <a href="table.php">Kembali</a>
                </td>
            </tr>
        </table>
    </form>
    <?php
  
    include "koneksi.php";
  
    function upload(): string
    {
        $nameImage = $_FILES['gambar']['name'];
        $directoryFile = $_FILES['gambar']['tmp_name'];
        $errorImage = intval($_FILES['gambar']['error']);
        $sizeFile = $_FILES['gambar']['size'];

        // cek apakah gambar ada
        if ($errorImage === 4) {
            echo "<script>alert('Anda Belum Upload Gambar')</script>";
            return false;
        }
  
        // mengambil ekstensi file
        $validType = ['svg', 'jpg', 'png', 'jpeg', 'webp'];
        $extensionFile = explode(".", $nameImage);
        $extensionValid = strtolower(end($extensionFile));
  
        // cek apakah yang diupload gambar atau bukan
        if (!in_array($extensionValid, $validType)) {
            echo "<script>alert('yang anda Upload bukan gambar')</script>";
            return false;
        }
  
        // cek size file
        if ($sizeFile > 3_000_000) {
            echo "<script>alert('Ukuran File Terlalu Besar!!(Maks 3MB)')</script>";
            return false;
        }

        // upload file
        $nameImage = uniqid() . "." . $extensionValid;
        move_uploaded_file($directoryFile, "img/{$nameImage}");

        // mengembalikan namafile yg sudah divalidasi
        return $nameImage;
    }
  
  
    if (isset($_POST['simpan'])) {
        $nama = $_POST['nama'];
        $email = $_POST['email'];
        $jenis_kelamin = $_POST['jenis_kelamin'];
        $alamat = $_POST['alamat'];
  
        $gambar = upload();
        if (!$gambar) {
            return;
        }
  
        // * true / false
        $query = mysqli_query($koneksi, "INSERT into siswa(nama,email,jenis_kelamin,alamat,gambar)
  
        values ('$nama','$email','$jenis_kelamin','$alamat', '$gambar')");
  
        if ($query == true) {
            echo "<script>
            alert('Tambah data Berhasil')
            window.location.href='table.php'
            </script>";
        } else {
            echo '<script>alert("Tambah data gagal")</script>';
        }
    }
  
    ?>

</body>
</html>
```

### **Hasil:**
![ab.png](Asetphp/ab.png)

![ac.png](Asetphp/ac.png)

### **Analisis:**

1. Pada bagian HTML, terdapat elemen `<form>` dengan atribut `enctype="multipart/form-data"`. Ini diperlukan agar formulir dapat mengirimkan data berupa file, dalam hal ini gambar.
2. Setelah itu, terdapat elemen input dengan `type="file"` dan `name="gambar"`. Bagian ini memungkinkan pengguna untuk memilih dan mengunggah file gambar dari perangkat mereka.
3. Pada bagian PHP, ada sebuah fungsi bernama `upload()` yang digunakan untuk mengelola proses upload gambar. Fungsi ini mengambil beberapa informasi dari `$_FILES`, seperti nama file (`$nameImage`), direktori sementara file (`$directoryFile`), kode error (`$errorImage`), dan ukuran file (`$sizeFile`).
4. Pertama, dilakukan pemeriksaan apakah gambar telah diunggah atau tidak. Jika `$errorImage` memiliki nilai 4, itu berarti tidak ada gambar yang diunggah. Dalam hal ini, pesan peringatan akan ditampilkan dan fungsi akan mengembalikan `false`.
5. Selanjutnya, ekstensi file ditentukan dengan memecah nama file menggunakan `explode()` dan mengambil bagian terakhir (`$extensionValid`). Kemudian, dilakukan pemeriksaan apakah ekstensi file tersebut ada di dalam array `$validType` yang berisi ekstensi yang diizinkan. Jika ekstensi tidak valid, pesan peringatan akan ditampilkan dan fungsi akan mengembalikan `false`.
6. Dilakukan pemeriksaan ukuran file dengan membandingkannya dengan batas maksimum yang ditetapkan (3MB dalam contoh ini). Jika ukuran file melebihi batas maksimum, pesan peringatan akan ditampilkan dan fungsi akan mengembalikan `false`.
7. Jika semua pemeriksaan berhasil, gambar akan diunggah ke direktori "img" dengan menggunakan fungsi `move_uploaded_file()`. Nama file gambar juga diubah menjadi unik dengan menggunakan fungsi `uniqid()`, ditambahkan dengan ekstensi yang valid.
8. Setelah file berhasil diunggah, nama file gambar yang telah divalidasi akan dikembalikan oleh fungsi.
9. Selanjutnya, pada bagian PHP yang mengurus penanganan formulir, dipanggil fungsi `upload()` untuk mengunggah gambar. Jika fungsi mengembalikan `false` (artinya terdapat kesalahan dalam upload gambar), maka program akan menghentikan eksekusi lebih lanjut dengan menggunakan `return`.
10. Jika upload gambar berhasil, data yang diisi pengguna seperti nama, email, jenis kelamin, alamat, dan nama file gambar akan dikumpulkan dan disimpan dalam variabel.
11. Dilakukan query SQL menggunakan `mysqli_query()` untuk memasukkan data siswa ke dalam tabel "siswa", termasuk nama file gambar yang sudah divalidasi.
12. Terakhir, terdapat penanganan pesan sukses atau gagal setelah query dieksekusi. Jika query berhasil, pesan sukses akan ditampilkan dan pengguna akan diarahkan kembali ke halaman "table.php". Jika query gagal, pesan gagal akan ditampilkan.

### **Kesimpulan:**
Program PHP tersebut memungkinkan pengguna untuk mengunggah gambar sebagai bagian dari formulir data siswa. Program ini melakukan beberapa pemeriksaan keamanan, seperti memeriksa apakah gambar diunggah, memeriksa ekstensi file, dan memeriksa ukuran file sebelum mengizinkan unggahan. Jika semua pemeriksaan berhasil, gambar akan diunggah ke direktori "img" dengan nama file yang unik. Setelah itu, data siswa beserta nama file gambar akan disimpan dalam database.

## Download
### **Kode Program:**
```php
<?php

include "koneksi.php";
  
$query = mysqli_query($koneksi, 'SELECT * FROM siswa');
  
$data = [];
$data[] = ["ID", "Nama","email", "Jenis Kelamin", "Alamat"];
while ($row = mysqli_fetch_assoc($query)) {
    $data[] = [
        $row['id_siswa'],
        $row['nama'],
        $row['email'],
        $row['jenis_kelamin'],
        $row['alamat']
    ];
}
  
$namafile = "excel_data.xls";
  
header("Content-Type: application/vnd.ms-excel");
header("Content-Disposition: attachment;filename=\"$namafile\"");
header("Cache-Control: max-age=0");
  
$output = fopen("php://output", "w");
  
foreach ($data as $row) {
    fputcsv($output, $row, "\t");
}
  
fclose($output);
exit;
```

**Hasil:**
![ad.png](Asetphp/ad.png)

### **Analisis:**
1. Pertama, program mengimpor file "koneksi.php" yang berisi pengaturan koneksi ke database. Ini diasumsikan sebagai file terpisah yang berisi kode untuk menghubungkan ke database MySQL.
2. Selanjutnya, dilakukan query SQL menggunakan `mysqli_query()` untuk mengambil data dari tabel "siswa". Query tersebut menghasilkan objek hasil query yang disimpan dalam variabel `$query`.
3. Dilakukan inisialisasi variabel `$data` sebagai array kosong. Kemudian, baris pertama pada array ini ditambahkan dengan judul kolom yaitu "ID", "Nama", "email", "Jenis Kelamin", dan "Alamat".
4. Selama masih ada baris hasil query yang tersedia, dilakukan perulangan menggunakan `mysqli_fetch_assoc()` untuk mengambil setiap baris data sebagai array asosiatif dalam variabel `$row`. Data dari setiap kolom kemudian ditambahkan sebagai elemen dalam array `$data`, sehingga setiap baris data memiliki nilai ID, Nama, email, Jenis Kelamin, dan Alamat.
5. Ditentukan nama file yang akan dihasilkan dengan variabel `$namafile`. Dalam contoh ini, nama file ditetapkan sebagai "excel_data.xls".
6. Diberikan header untuk menentukan jenis konten dan nama file yang akan diunduh. `header("Content-Type: application/vnd.ms-excel")` menentukan jenis konten sebagai file Excel, sedangkan `header("Content-Disposition: attachment;filename=\"$namafile\"")` menetapkan nama file dan mengatur agar file tersebut diunduh oleh pengguna.
7. Diberikan header "Cache-Control: max-age=0" untuk mencegah file disimpan dalam cache browser.
8. Dibuka file output dengan `fopen("php://output", "w")` menggunakan mode tulis ("w") dan file handle disimpan dalam variabel `$output`.
9. Dilakukan perulangan `foreach` untuk setiap baris data dalam array `$data`. Setiap baris data diubah menjadi format CSV dengan menggunakan `fputcsv()` dan ditulis ke file output yang dibuka sebelumnya.
10. Setelah selesai menulis semua data, file output ditutup dengan `fclose($output)`.
11. Program diakhiri dengan `exit` untuk menghentikan eksekusi program setelah file Excel dihasilkan.

### **Kesimpulan:**
Program PHP tersebut mengambil data dari tabel "siswa" dalam database MySQL menggunakan query SQL. Data tersebut kemudian diubah menjadi file Excel (.xls) yang diunduh oleh pengguna. Program ini menggunakan fungsi header untuk mengatur jenis konten dan nama file yang akan diunduh, serta menggunakan fungsi fopen, fputcsv, dan fclose untuk menghasilkan file Excel dengan data yang sesuai.

RahmatObs/Belajar PHP/Pengenalan PHP.md at master · DaniiNT/RahmatObs

