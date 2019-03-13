# PHP-Modul-7

1. Berikan contoh kode keneksi untuk ke database pd php?

-> 
  
  <?php
  
  
$host = "localhost";

$db = "db_universitas";

$uname = "root";

$pass = "";

$connect = mysqli_connect($host, $uname, $pass, $db);

  
2. Bagaimana cara anda membuat database pada phpMySQl!
  -> Dari CMD xampp
    1. Pertama masukkan kode mysql -u root
    
    2. Kemudian masukkan kode "create database (nama database);"(tanpa tanda petik)
    
    3. Kemudian ketikan show databases; untuk melihat database kita
    
    4. Database selesai dibuat
    
  -> Dari PHPmyAdmin
  1. Nyalakan xampp untuk mysql
  
  2. Buka localhost/phpmyadmin di web
  
  3. Kemudian tekan pilihan new
  
  4. dan isikan nama database lalu tekan create
  
  -> Dari FIle PHP
  
  1. buat file php
  
  2. Lalu ketikkan code code ini
  
    <?php
    
    $sql = "CREATE DATABASE (nama database)";
    
    if($koneksi->query($sql) == TRUE){
    
        echo "Database berhasil dibuat";
        
    } else {
    
        echo "Database gagal dibuat";
    }
    
?>
  
  
  
3. Berikan code query untuk menampilkan sebuah data yang ada pada ke database?
SELECT * FROM (nama Tabel);

Contoh :
<?php
   
    $sql = "SELECT * FROM user";
    
    $result = $koneksi->query($sql);
    
    foreach($result as $result){
    
    $id = $result["id"];
    
    $nama = $result["nama"];
    
    $role = $result["role"];
    
    $availability = $result["availability"];
    
    $age = $result["age"];
    
    $location = $result["location"];
    
    $experience = $result["years_experience"];
    
    $email = $result["email"];
    

        }
        
?>

4. Berikan code query untuk mengupdate sebuah data yang ada pada ke database?

"UPDATE dosen SET (nama kolom) = 'variabel/isinya', (nama kolom)='variabel/isinya' WHERE (nama kolom)= variabel/isinya";

Contoh :

"UPDATE dosen SET nama_dosen = '$nama_dosen', telp='$telp' WHERE id_dosen= $id_dosen";

5. Berikan code query untuk menghapus sebuah data yang ada pada ke database?

"DELETE FROM dosen WHERE (nama kolom yang menjadi primary key) = data dari kolom primary key";

Contoh :

"DELETE FROM dosen WHERE id_dosen = $id_dosen";

Menambah Data
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Tambah%20Data.png)
Hasil Tambah Data
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Hasil%20Tambah%20Data.png)
Tabel Setelah data ditambah
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Lihat%20data%20setelah%20ditambah.png)
Update data
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Update%20data.png)
Hasil update data
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Hasil%20update%20data.png)
Data setelah di update
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Data%20setelah%20di%20update.png)
Hapus data
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Hapus%20Data.png)
Setelah hapus data
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Setelah%20Hapus%20Data.png)
Data setelah di hapus
![alt text](https://github.com/RaflyAmartharizqi/PHP-Modul-7/blob/master/dosen/Data%20setelah%20dihapus.png)
