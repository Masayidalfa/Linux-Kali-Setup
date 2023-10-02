# Linux-Kali-Setup
Beberapa Hal yang harus dilakukan ketika baru install kali linux

## Fix Update
1. Backup sources.list bawaan
2. Ubah source.list menggunakan Server Mirror ID agar update ngebut karena pake yang official lelet banget kaya keong
3. bisa cek di web https://http.kali.org/README.mirrorlist

```bash
sudo nano /etc/apt/sources.list
```

setelah itu ganti isinya dengan :
```bash
# See https://www.kali.org/docs/general-use/kali-linux-sources-list-repositories/
deb https://xsrv.moratelindo.io/kali/ kali-rolling main contrib non-free non-free-firmware

# Additional line for source packages
# deb-src https://xsrv.moratelindo.io/kali/ kali-rolling main contrib non-free non-free-firmware
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
