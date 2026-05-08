<h1 align="center">Nusantara Panel</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/wayangm/NusantaraPanelCore/main/web/images/logo.png" alt="Nusantara Panel Logo" width="200"/>
</p>

<h2 align="center">Panel Kontrol Server Ringan dan Bertenaga untuk Web Modern</h2>

<p align="center">
  Distribusi panel hosting berbasis open source dengan identitas lokal Indonesia.
</p>

<p align="center">
  <a href="https://github.com/wayangm/NusantaraPanelCore/blob/main/CHANGELOG.md">Lihat Changelog</a> |
  <a href="https://github.com/wayangm/NusantaraPanelCore/issues">Laporkan Bug</a> |
  <a href="https://github.com/wayangm/NusantaraPanelCore/blob/main/CONTRIBUTING.md">Kontribusi</a>
</p>

---

## 🇮🇩 Tentang Nusantara Panel

**Nusantara Panel** adalah distribusi panel kontrol server berbasis open source (fork dari HestiaCP) yang dirancang untuk memudahkan administrator server dalam mengelola web domain, email, DNS, dan database dari satu antarmuka yang sederhana — dengan identitas dan branding lokal Indonesia.

Panel ini dikembangkan oleh **WG Media Indonesia** sebagai solusi hosting panel yang mandiri, transparan, dan bebas telemetri cloud.

---

## ✨ Fitur Utama

- **Web Server**: Apache2 & NGINX dengan PHP-FPM
- **Multi-PHP**: Versi 5.6 hingga 8.4 (default 8.3)
- **DNS Server**: BIND dengan kemampuan clustering
- **Mail Server**: POP/IMAP/SMTP + Anti-Virus + Anti-Spam + Webmail (ClamAV, SpamAssassin, Roundcube)
- **Database**: MariaDB/MySQL dan PostgreSQL
- **SSL Otomatis**: Let's Encrypt termasuk wildcard certificates
- **Firewall**: iptables + Fail2ban + ipset
- **Branding Lokal**: Identitas penuh milik Nusantara Panel

---

## 🖥️ Sistem Operasi yang Didukung

| OS | Versi |
|---|---|
| **Ubuntu** | 24.04 LTS, 22.04 LTS |
| **Debian** | 12, 11 |

> ⚠️ **Catatan:**
> - Tidak mendukung sistem operasi 32-bit.
> - Jika menggunakan VPS berbasis OpenVZ 7 atau lebih rendah, mungkin ada masalah dengan DNS dan/atau Firewall. Sangat disarankan untuk menggunakan VPS berbasis KVM atau LXC.

---

## 🚀 Cara Instalasi

> **PENTING:** Jalankan instalasi pada **server baru yang bersih** (fresh installation) untuk memastikan tidak ada konflik.

### Langkah 1: Login sebagai Root

```bash
ssh root@ip-server-anda
```

### Langkah 2: Jalankan Installer (Satu Perintah)

```bash
curl -sSL https://raw.githubusercontent.com/wayangm/NusantaraPanelCore/main/install/hst-install.sh | sudo bash -s -- \
  --email email@anda.com \
  --password passwordanda \
  --hostname panel.domain.anda
```

### Langkah 3: Akses Panel

Setelah instalasi selesai, buka browser dan akses:
```
https://ip-server-anda:8083
```

Login menggunakan `admin` dan password yang Anda tentukan saat instalasi.

---

## ⚙️ Opsi Instalasi Kustom

Untuk melihat semua opsi yang tersedia:

```bash
bash hst-install.sh -h
```

Contoh instalasi dengan opsi kustom:
```bash
curl -sSL https://raw.githubusercontent.com/wayangm/NusantaraPanelCore/main/install/hst-install.sh | sudo bash -s -- \
  --email admin@domain.com \
  --password admin123 \
  --hostname panel.domain.com \
  --multiphp yes \
  --postgresql no \
  --lang id
```

---

## 🔄 Cara Update

Update otomatis diaktifkan secara default. Untuk update manual:

```bash
apt-get update
apt-get upgrade
```

---

## 🐛 Laporan Bug & Dukungan

- Temukan bug? [Buat Issue baru di GitHub](https://github.com/wayangm/NusantaraPanelCore/issues).
- Sertakan langkah-langkah yang sudah dilakukan dan informasi sistem Anda agar kami bisa membantu lebih cepat.

---

## 🤝 Kontribusi

Kontribusi sangat disambut! Silakan baca [Panduan Kontribusi](https://github.com/wayangm/NusantaraPanelCore/blob/main/CONTRIBUTING.md) terlebih dahulu.

---

## 📄 Lisensi

Nusantara Panel dilisensikan di bawah [GPL v3](https://github.com/wayangm/NusantaraPanelCore/blob/main/LICENSE).

Nusantara Panel adalah hasil **rebranding** dari proyek [HestiaCP](https://github.com/hestiacp/hestiacp) yang juga dilisensikan di bawah GPL v3, yang sebelumnya berbasis dari proyek [VestaCP](https://vestacp.com/).

---

<p align="center">
  <strong>Nusantara Panel</strong> &mdash; Distribusi Panel Hosting Indonesia<br/>
  Dibangun di atas fondasi <a href="https://github.com/hestiacp/hestiacp">HestiaCP</a>, dikustomisasi dan dibranding ulang oleh <strong>WG Media Indonesia</strong><br/><br/>
  © 2024–2026 Nusantara Panel | WG Media Indonesia
</p>
