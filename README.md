# 🚀 Final Project OS Server & Sistem Admin 🚀

## 🌐 Domain
<a href="https://kingzuy.my.id" target="_blank" rel="noopener noreferrer">kingzuy.my.id</a>

## ✨ Spesifikasi
- Ubuntu-22.04.5-live-server
- RAM 2 GB
- Storage 35 GB

## 🛠 Teknologi yang Akan Digunakan
- Node.js (15 Desember 2024)
- LAMP (12 Desember 2024)
- Docker (15 Desember 2024)
- SSH (4 November 2024)
- DNS (30 November 2024)
- Netdata (15 Desember 2024)
- Firewall (12 Desember 2024)

## 📈 Progrest
1. Install openssh:
- melakukan update
```bash
sudo apt update && sudo apt upgrade
```
- install open ssh
```bash
sudo apt install openssh-server
```
2. Install LAMP
- install Apache2
```bash
sudo apt install apache2
```
- Tampilkan aplikasi UFW
```bash
sudo ufw app list
```
- Konfigurasi Firewall  
```bash
# Izinkan OpenSSH
sudo ufw allow OpenSSH

# Izinkan koneksi SSH
sudo ufw allow 22

# Izinkan Apache
sudo ufw allow Apache
sudo ufw allow 'Apache Full'

# Izinkan port HTTP/HTTPS
sudo ufw allow 80
sudo ufw allow 443
```
- Aktifkan Firewall
```bash
# Aktifkan UFW
sudo ufw enable

# Cek status UFW
sudo ufw status
```
- Install mysql
```bash
# Install mysql
sudo apt install mysql-server

# Masuk Mysql
sudo mysql

# Ganti/Add Password
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
- Install php
```bash
# Install php
sudo apt install php libapache2-mod-php php-mysql

# Cek
php -v

# Config
sudo nano /etc/apache2/mods-enabled/dir.conf

# Menjadi seperti ini
<IfModule mod_dir.c>
    DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
```
- Install phpmyadmin
```bash
sudo apt install phpmyadmin php-mbstring php-zip php-gd php-json php-curl
```
3. Setup DNS<br>
buka cloudflare, lalu add domain , masukan nama domain kalian, lalu next, pilih yang free lalu next, pada bagian `Your assigned Cloudflare nameservers: ` copy paste ke ns domain kalian, lalu click check nameservers now
<img src="assets/WhatsApp Image 2024-12-02 at 01.54.39_27d82b87.jpg">
<img src="assets/WhatsApp Image 2024-12-02 at 02.04.13_0f336714.jpg">
<img src="assets/WhatsApp Image 2024-12-01 at 18.35.43_b9dbcc4e.jpg">
<img src="assets/WhatsApp Image 2024-12-01 at 18.33.35_49bc85d7.jpg">

4. Install Node.js
- Melakukan update
```bash
sudo apt update
```
- Install Dependensi yang Dibutuhkan
```bash
sudo apt install -y curl software-properties-common
```
- Menambahkan Repositori NodeSource
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
```
- Install Node.js
```bash
sudo apt install -y nodejs
```
- Verifikasi Instalasi
```bash
node -v
```
5. Install DOcker
- Melakukan update
```bash
sudo apt update
```
- Install Docker
```bash
sudo apt install docker.io
```
```
- Cek Docker
```bash
docker -v
```
