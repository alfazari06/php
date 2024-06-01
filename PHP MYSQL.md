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
![[h.koneksi.jpeg]]

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
![[h.knks.png]]
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
![[h.ubahdata.png]]
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
![[ubahda.png]]
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
![[hps.png]]
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
![[hasil.png]]

![[hasill.png]]

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
![[ab.png]]

![[ac.png]]

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
![[ad.png]]

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

