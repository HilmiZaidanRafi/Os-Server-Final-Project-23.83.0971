# Final-Project-Os-Server-23TK01-23.83.0971
- Nama:Muhammad Hilmi Zaidan Rafi
- Kelas:23TK01
- Mata Kuliah:OS SERVER dan SISTEM ADMIN

## Daftar Isi
1. [Installasi OPEN SSH SERVER](#1.-[Installasi-OPEN-SSH-SERVER](https://github.com/HilmiZaidanRafi/Os-Server-Final-Project-23.83.0971/edit/main/README.md#1installasi-open-ssh-server))
2. [Installasi MY-SQL SERVER](#2.-Installasi-MY-SQL-SERVER)
3. [Installasi APACHE2](#3.-Installasi-APACHE2)
4. [Installasi DATABASE SERVER](#4.-Installasi-DATABASE-SERVER)
5. [Installasi SAMBA](#5.-Installasi-SAMBA)

## 1.Installasi OPEN SSH SERVER

**Langkah 1: Lakukan Instalasi Paket SSH Server**

```
sudo apt install openssh-server -y
```

**Langkah 2: Mengaktifkan Layanan ssh server**
```
sudo systemctl enable ssh
```

**Langkah 3: Memulai Layanan SSH SERVER**

```
sudo systemctl start ssh
```

**Langkah 4: Cek ip ubuntu server**
```
ip add
```

**Langkah 5: Cek status SSH SERVER**

```
sudo systemctl status ssh
```

**Langkah 6: Konfigurasi SHH SERVER**
```
Buka CMD pada windows,lakukan konfigurasi pada ubuntu dengan cara <ssh username ubuntu@ip address ubuntu server> contoh:ssh hilmiserver@192.168.1.3
setelah itu ketik manual "yes" dan masukkan password ubuntu server
```
![5](https://github.com/user-attachments/assets/51dbafd6-661b-449c-adf9-6561d4781bf0)
![6 (2)](https://github.com/user-attachments/assets/9d176305-0c51-4fc8-b00d-89b805bb0651)
![7](https://github.com/user-attachments/assets/483c98b2-4a57-4aee-91bd-d04f646325b0)

## 2.Installasi MY-SQL SERVER
 **Langkah 1:Install mysql server dengan perintah**
```
sudo apt install mysql-server -y
```

**Langkah 2:Install tumpukan LAMP (Linux, Apache, MySQL, PHP) pada sistem operasi dengan perintah**
```
sudo apt install php libapache2-mod-php phpmysql
```

**Langkah 3:Membuka File Konfigurasi Direktori Apache dengan perintah**
```
sudo nano /etc/apache2/mods-enabled/dir.conf
```
- Tambahkan "index.php" pada di sebelah kanan "DirectoryIndex"
![13](https://github.com/user-attachments/assets/bc71d80c-e143-4286-87f4-263067b5e662)

**Langkah 4:Membuka file bernama “info.php” pada direktori var/www/html**
```
sudo nano /var/www/html/info.php
```
- isikan dengan code dibawah
```
<?php

phpinfo ();

?>
```


**Langkah 5:CEK KONFIGURASI**
- Buka pada google chrome pada windows <ip addres ubuntu server/info.php>
- cth :192.168.1.3/info.php
![17](https://github.com/user-attachments/assets/09d78e4b-6473-4435-9994-f8efce33b653)
![18](https://github.com/user-attachments/assets/c7119923-5f59-4e86-bb2a-3f155b4154c8)

## 3.Installasi APACHE2
**Langkah 1:Perbarui daftar paket dengan perintah**
```
sudo apt update
```

**Langkah 2:Installasi apache 2 dengan perintah**
```
sudo apt install apache2 -y
```
- samakan dengan foto di bawah

**Langkah 3:Memulai layanan server apahe2 dengan perintah**
```
sudo systemctl start apache2
```
**Langkah 4:Lakukan pengecekan ip addres ubuntu server dengan perintah**
```
 ip add
```
**Langkah 5:Buka pada browser google chrome pada windows dan ketikkan ip addres tadi “192.168.1.3”**
- contoh ip saya:192.168.1.3
  ![23](https://github.com/user-attachments/assets/a90e2a6c-dd81-4b99-a381-a4eb3c1e3f4b)

## 4.Installasi DATABASE SERVER
**Langkah 1:Installasi paket mariadb**
```
sudo apt-get update
sudo apt-get install mariadb-server
```

**Langkah 2:Untuk mengamankan installasi (Opsional)**
```
sudo mysql_secure_installation
```
![27](https://github.com/user-attachments/assets/1bd2d90e-721f-44f1-8d72-2902ff0dfe91)
![28](https://github.com/user-attachments/assets/a80b0d07-67fb-4cf4-ae5d-f9da48b6f1ba)

**Langkah 3:Lakukan instalasi paket**
```
sudo apt-get install phpmyadmin
```
![29#1](https://github.com/user-attachments/assets/b299c071-eb17-4fe8-8a36-81b3bb77ec23)
![29#2](https://github.com/user-attachments/assets/1dd7b1e7-052e-45dc-b345-61eb2a212386)
![29#3](https://github.com/user-attachments/assets/e45213a0-5731-455c-a605-20769ac4fb1f)
![29#4](https://github.com/user-attachments/assets/f967ac4d-68df-4ed4-91c4-bd5b73c0ce3a)

**Langkah 4:Restart ulang layanan**
```
sudo systemctl restart apache2
```
**Langkah 5:CEK KONFIGURASI**
Buka pada browser windows gogole chrome dan ketikkan <ip address ubuntu server/phpmyadmin/> cth:192.168.1.3/phpmyadmin/ 
![31](https://github.com/user-attachments/assets/ada112e1-0200-4e5f-b030-0bc5d9e868d1)
![32](https://github.com/user-attachments/assets/932ebaa4-3402-4087-aebd-7b81b16857a9)

## 5.Installasi SAMBA
**Langkah 1:Memperbarui daftar paket dengan perintah**

```
sudo apt update
sudo apt upgrade-y
```
**Langkah 2:Membuat direktori baru bernama ‘sambashare” dengan perintah**

```
sudo mkdir /sambashare
```
**Langkah 3:Mengubah izin akses dengan perintah**
```
sudo chmod 0777  /sambasahre
```
**Langkah 4:Menambah pengguna baru bernama**
- cth: username “user1” dan membuat password ”0971”

```
sudo useradd user1
```
![37](https://github.com/user-attachments/assets/40b41835-c4da-4faf-9b41-617f146445ca)

**Langkah 5:Mengedit file konfigurasi utama dengan perintah**
```
sudo nano /etc/samba/smb.conf
```
**Langkah 6:Memulai ulang layanan samba dengan perintah**
```
 sudo systemctl restart smbd
 sudo systemctl restart nmbd
```
**Langkah 7:Cek status dengan perintah “sudo systemctl status smbd” pastikan muncul tulisan “running”**
```
 sudo systemctl status smbd
```
**Langkah 8:Buka file eksplorer pada windows,dan pilih bagian “This PC” kemudian ketikkan pada taskbar atas ip add ubuntu server (192.168.1.3) lalu masukkan username dan passwd yang sudah di buat tadi**
![42](https://github.com/user-attachments/assets/9b71d66b-6533-4b0f-86f0-dbbeeaa1df00)
![43](https://github.com/user-attachments/assets/219a9a55-760a-4ab2-bcfa-5f66ee2d82bb)
![44](https://github.com/user-attachments/assets/3a0d6387-ef5d-4d30-9947-e232c06e5ca0)
![45](https://github.com/user-attachments/assets/21821aaa-0bed-40bf-a471-31f1490aaf58)


