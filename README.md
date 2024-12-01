# 🚀 Final Project OS Server & Sistem Admin 🚀

## ✨ Spesifikasi
- Ubuntu-22.04.5-live-server
- RAM 2 GB
- Storage 35 GB

## 🛠 Teknologi yang Akan Digunakan
- Node.js
- LAMP
- Docker
- SSH
- DNS
- Netdata

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
