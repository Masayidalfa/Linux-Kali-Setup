# Linux-Kali-Setup
Beberapa Hal yang harus dilakukan ketika baru install kali linux

## Fix Update
1. Backup sources.list bawaan
2. Ubah source.list menggunakan deb alternatif barkeley agar update ngebut karena pake yang official lelet banget kaya keong

```bash
sudo nano /etc/apt/sources.list
```

setelah itu ganti isinya dengan :
```bash
deb https://mirrors.ocf.berkeley.edu/kali/  kali-rolling main contrib non
# For source package access, uncomment the following line
# deb-src https://mirrors.ocf.berkeley.edu/kali/ kali-rolling main contrib
```

jika sudah, lanjutkan dengan command :
```bash
sudo apt clean
sudo apt update
sudo apt upgrade
sudo apt dist-upgrade
```

jika mau langsung bisa dengan command :
```bash
sudo apt update && apt upgrade -y
```

hal ini dilakukan untuk full upgrade pada versi terbaru

Selanjutnya bisa dilanjutkan dengan menginstall package package apa saja
