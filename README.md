#  AquaFeed — Sistem Monitoring & Kontrol Pemberian Pakan Ikan Otomatis Berbasis IoT

# Deskripsi Proyek


**GitHub**: https://github.com/USERNAME/aquafeed-iot

---

##  Anggota Tim

| NRP | Nama | Jobdesk | Akun |
|-----|------|---------|------|
| 2124600030 | Aidabn Pasha Rabani | Project Manager | Aidan031 |
| XXXXXXXXX | Nama Anggota 2 | Hardware Specialist | [@username](https://github.com/username) |
| 2124600058 | M Reihan Maulana | Programmer | reiihaaannn |
| XXXXXXXXX | Nama Anggota 4 | UI/UX Designer | [@username](https://github.com/username) |
| XXXXXXXXX | Nama Anggota 5 | 3D Designer | [@username](https://github.com/username) |

---

## 💡 Ide Proyek

Sistem otomatis berbasis IoT untuk memberikan pakan ikan secara terjadwal sekaligus
memantau kualitas air akuarium/kolam secara real-time.

---

## 📋 Deskripsi

Menggunakan mikrokontroler ESP32, sensor suhu DS18B20, sensor pH, motor servo, 
dan modul RTC DS3231 untuk mengotomatisasi jadwal pemberian pakan ikan. 
Data kondisi air (suhu, pH) dikirim ke dashboard berbasis web yang dapat 
diakses dari jarak jauh melalui koneksi internet. Pengguna juga dapat 
mengontrol pemberian pakan secara manual melalui aplikasi.

---

## ✨ Fitur

- ⏰ Pemberian pakan otomatis berbasis jadwal (RTC)
- 🌡️ Monitoring suhu dan pH air secara real-time
- 📱 Kontrol manual jarak jauh via web/mobile
- 🔔 Notifikasi kondisi air abnormal
- 📊 Dashboard monitoring berbasis web

---

## 🛠️ Komponen Hardware

| Komponen | Fungsi |
|----------|--------|
| ESP32 | Mikrokontroler utama & koneksi WiFi |
| Sensor DS18B20 | Mengukur suhu air |
| Sensor pH | Mengukur tingkat keasaman air |
| Motor Servo | Menggerakkan mekanisme pakan |
| RTC DS3231 | Penjadwalan waktu pemberian pakan |
| LCD I2C 16x2 | Menampilkan informasi lokal |

---

## ⚙️ Cara Instalasi

1. Clone repository ini
```bash
   git clone https://github.com/USERNAME/aquafeed-iot.git
```
2. Buka folder `firmware/esp32_main/`
3. Install library yang dibutuhkan di Arduino IDE
4. Sesuaikan konfigurasi WiFi di file `config.h`
5. Upload kode ke ESP32

---

## 📷 Dokumentasi

![Prototype](./assets/prototype.jpg)
![Dashboard](./assets/dashboard.png)
![Skema Rangkaian](./assets/schematic.png)

---

## 🚀 Peluang Pengembangan

- Notifikasi WhatsApp/Telegram saat kondisi air abnormal
- Tambah sensor turbidity (kejernihan air)
- Kamera untuk pemantauan visual ikan secara real-time
- Analitik data & prediksi berbasis machine learning
- Integrasi dengan platform smart home (Google Home/Alexa)
- Aplikasi mobile Android/iOS

---

## 📁 Struktur Folder
