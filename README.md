# Student App
Aplikasi untuk pengujian konsep Cloud Computing dan ITNSA

1. Deploy di VM CentOS dengan Apache, Git
   ```bash
   sudo yum update -y
   sudo yum install -y git httpd php php-mysqlnd 
   
2. Konfigurasi file config.php sesuai dengan credentials service AWS anda
3. SQL untuk membuat tabel
Jalankan query ini di database RDS Anda (misalnya melalui MySQL Workbench atau DBeaver) untuk membuat tabel siswa.
   ```bash
   CREATE DATABASE db_sekolah;
   USE db_sekolah;
   CREATE TABLE siswa (
    id INT(11) PRIMARY KEY AUTO_INCREMENT,
    nama VARCHAR(255) NOT NULL,
    nomor_presensi INT(11) NOT NULL,
    kelas VARCHAR(100) NOT NULL,
    foto_filename VARCHAR(255) NULL -- Menyimpan nama file foto
   );

4. Buat direktori baru di dalam folder aplikasi untuk menyimpan file foto
   ```bash
   sudo mkdir /var/www/html/uploads
5. Konfigurasi DNS di MikroTik dengan ketentuan http://<nama>.internal
5. Test 
