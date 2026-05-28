<svg viewBox="0 0 400 420" xmlns="http://www.w3.org/2000/svg" font-family="'Segoe UI', Arial, sans-serif">
  <defs>
    <radialGradient id="bgGrad" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#0a2a4a"/>
      <stop offset="100%" stop-color="#051525"/>
    </radialGradient>
    <linearGradient id="circleGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#00c6ff"/>
      <stop offset="100%" stop-color="#0072ff"/>
    </linearGradient>
    <linearGradient id="fishGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#ffffff"/>
      <stop offset="100%" stop-color="#cceeff"/>
    </linearGradient>
    <filter id="glow">
      <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <filter id="shadow">
      <feDropShadow dx="0" dy="4" stdDeviation="6" flood-color="#00c6ff" flood-opacity="0.4"/>
    </filter>
    <clipPath id="clipCircle">
      <circle cx="200" cy="190" r="115"/>
    </clipPath>
  </defs>

  <!-- Background -->
  <rect width="400" height="420" fill="url(#bgGrad)" rx="30"/>

  <!-- Outer ring -->
  <circle cx="200" cy="190" r="130" fill="none" stroke="#00c6ff" stroke-width="2" stroke-opacity="0.3" stroke-dasharray="8 4"/>

  <!-- Main circle -->
  <circle cx="200" cy="190" r="115" fill="url(#circleGrad)" filter="url(#shadow)"/>

  <!-- Water body -->
  <ellipse cx="200" cy="235" rx="115" ry="70" fill="#0050c8" clip-path="url(#clipCircle)"/>

  <!-- Wave 1 -->
  <path d="M85 220 Q110 205 135 220 Q160 235 185 220 Q210 205 235 220 Q260 235 285 220 Q305 210 315 220 L315 310 L85 310 Z"
        fill="#0066e0" clip-path="url(#clipCircle)" opacity="0.8"/>

  <!-- Wave 2 -->
  <path d="M85 232 Q115 217 145 232 Q175 247 205 232 Q235 217 265 232 Q290 242 315 232 L315 310 L85 310 Z"
        fill="#0072ff" clip-path="url(#clipCircle)" opacity="0.6"/>

  <!-- Water shine -->
  <ellipse cx="200" cy="122" rx="60" ry="12" fill="white" fill-opacity="0.12"/>

  <!-- FISH -->
  <g filter="url(#glow)" transform="translate(200,194)">
    <ellipse cx="0" cy="-15" rx="42" ry="22" fill="url(#fishGrad)" transform="rotate(-5)"/>
    <polygon points="-42,-15 -62,-32 -62,2" fill="#cceeff" opacity="0.9"/>
    <path d="M-5,-37 Q8,-50 20,-37" stroke="#0099dd" stroke-width="2.5" fill="none" stroke-linecap="round"/>
    <circle cx="28" cy="-20" r="5" fill="#0a2a4a"/>
    <circle cx="29" cy="-21" r="1.8" fill="white"/>
    <path d="M40,-15 Q44,-12 40,-10" stroke="#88ccee" stroke-width="1.5" fill="none" stroke-linecap="round"/>
    <path d="M10,-15 Q5,-8 0,-15" stroke="#aaddee" stroke-width="1" fill="none" opacity="0.5"/>
    <path d="M20,-12 Q15,-5 10,-12" stroke="#aaddee" stroke-width="1" fill="none" opacity="0.5"/>
  </g>

  <!-- Bubbles -->
  <circle cx="158" cy="163" r="4" fill="none" stroke="white" stroke-width="1.5" opacity="0.6"/>
  <circle cx="170" cy="147" r="2.5" fill="none" stroke="white" stroke-width="1.2" opacity="0.4"/>
  <circle cx="148" cy="150" r="3" fill="none" stroke="white" stroke-width="1.2" opacity="0.5"/>
  <circle cx="240" cy="160" r="3.5" fill="none" stroke="white" stroke-width="1.5" opacity="0.5"/>
  <circle cx="252" cy="145" r="2" fill="none" stroke="white" stroke-width="1" opacity="0.4"/>

  <!-- Feed/pakan dots -->
  <circle cx="195" cy="112" r="4" fill="#FFD700" opacity="0.9"/>
  <circle cx="207" cy="123" r="3.5" fill="#FFA500" opacity="0.85"/>
  <circle cx="185" cy="125" r="3" fill="#FFD700" opacity="0.75"/>
  <circle cx="215" cy="135" r="3" fill="#FFA500" opacity="0.65"/>

  <!-- IoT signal -->
  <g transform="translate(280,114)" stroke="#00e5ff" fill="none" stroke-linecap="round" opacity="0.85">
    <path d="M0,0 A10,10 0 0,1 14,7" stroke-width="2.5"/>
    <path d="M-4,-6 A18,18 0 0,1 20,11" stroke-width="2"/>
    <path d="M-8,-12 A26,26 0 0,1 26,16" stroke-width="1.5"/>
    <circle cx="0" cy="0" r="3" fill="#00e5ff" stroke="none"/>
  </g>

  <!-- Brand name -->
  <text x="200" y="340" text-anchor="middle" font-size="36" font-weight="800" letter-spacing="3" fill="white">AQUA<tspan fill="#00e5ff">FEED</tspan></text>

  <!-- Tagline -->
  <text x="200" y="365" text-anchor="middle" font-size="11" fill="#7ecfff" letter-spacing="2.5">SMART IoT FISH FEEDING SYSTEM</text>

  <!-- Bottom accent -->
  <line x1="120" y1="378" x2="280" y2="378" stroke="#00c6ff" stroke-width="1.5" stroke-opacity="0.5"/>
  <circle cx="200" cy="378" r="3" fill="#00c6ff" opacity="0.7"/>
</svg>


#  AquaFeed Sistem Monitoring & Kontrol Pemberian Pakan Ikan Otomatis Berbasis IoT


# Deskripsi Proyek
Menggunakan mikrokontroler Arduino Mega (ATMega2560), sensor suhu DS18B20, sensor pH, motor servo, 
dan modul RTC DS3231 untuk mengotomatisasi jadwal pemberian pakan ikan. 
Data kondisi air (suhu, pH) dikirim ke dashboard berbasis web yang dapat 
diakses dari jarak jauh melalui koneksi internet. Pengguna juga dapat 
mengontrol pemberian pakan secara manual melalui aplikasi.

---

# Tujuan Proyek


**GitHub**: https://github.com/USERNAME/aquafeed-iot

---

#  Anggota Tim

| NRP | Nama | Jobdesk | Akun |
|-----|------|---------|------|
| 2124600030 | Aidan Pasha Rabani | Project Manager | [Aidan031](https://github.com/Aidan031) |
| 21246000 | M Arya | Hardware Specialist | [maryacs212434](https://github.com/maryacs212434) |
| 2124600058 | M Reihan Maulana | Programmer | [reihaaannn](https://github.com/reihaaannn) |
| 2124600043 | Sabrina Keisha Maharani | UI/UX Designer | [sabrinakeisha](https://github.com/sabrinakeisha) |
| 2124600051 | M Ridho Andika | 3D Designer | [Ridhoandika112](https://github.com/Ridhoandika112) |
| 2124600035 | Setyo Wahyu Nur F |  |  |

---


# 🐟 AquaFeed IoT - Sistem Pemberi Pakan Ikan Otomatis

![Platform](https://img.shields.io/badge/Platform-ESP32-blue)
![Language](https://img.shields.io/badge/Language-C%2B%2B-green)
![Status](https://img.shields.io/badge/Project-In%20Development-yellow)

AquaFeed IoT adalah solusi berbasis Internet of Things untuk mempermudah pemantauan kualitas air dan otomatisasi pemberian pakan ikan secara real-time jarak jauh.

## 🚀 Fitur Utama
* **📅 Automated Feeding:** Penjadwalan pakan presisi berbasis waktu (NTP Server).
* **📱 Manual Override:** Tombol instan pada aplikasi untuk memberi pakan kapan saja.
* **📊 Feed Level Monitor:** Deteksi sisa pakan di wadah menggunakan sensor ultrasonik.
* **🌡️ Water Environment Analytics:** Monitoring suhu air demi menjaga ekosistem kolam yang ideal.

## 🛠️ Arsitektur Sistem
*(Masukkan gambar diagram blok sistem atau skematik hardware di sini)*
