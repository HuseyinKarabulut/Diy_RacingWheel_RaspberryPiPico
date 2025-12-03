# Diy_RacingWheel_RaspberryPiPico
# 🏎️ DIY Racing Wheel, Pedal Set & H-Pattern Shifter

![Status](https://img.shields.io/badge/Status-In%20Development-orange?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Raspberry%20Pi%20Pico-red?style=for-the-badge)
![License](https://img.shields.io/badge/License-Open%20Source-blue?style=for-the-badge)

<div align="center">
  <a href="#-türkçe">🇹🇷 Türkçe</a> | <a href="#-english">🇺🇸 English</a>
</div>

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### 📘 Proje Özeti
Bu proje, **Raspberry Pi Pico**, **360 darbe optik enkoder**, **3’lü pedal seti** (gaz, fren, debriyaj) ve **H-pattern manuel vites** kullanılarak geliştirilmiş, yüksek performanslı bir DIY yarış simülasyon kontrolcüsüdür.

Cihaz, **USB HID** protokolü sayesinde bilgisayar tarafından sürücü gerektirmeyen doğal bir oyun kontrolcüsü olarak algılanır. Düşük gecikme (low latency) ve yüksek kararlılık için optimize edilmiştir.

### 🚀 Özellikler
* 🎮 **Tam Uyumluluk:** USB HID standartlarında "Tak-Çalıştır" yarış direksiyonu.
* 🦶 **3 Pedal Seti:** Gaz, Fren ve Debriyaj eksenleri.
* ⚙️ **H-Pattern Vites:** 6 İleri + 1 Geri (veya özelleştirilebilir) manuel vites kutusu.
* 🎯 **Yüksek Hassasiyet:** 360 PPR Artımlı Optik Enkoder ile pürüzsüz direksiyon tepkisi.
* ⚡ **FFB Hazır Altyapı:** BTS7960 Motor Sürücü entegrasyonu (Force Feedback desteği için donanım hazır).
* 🧩 **Sağlam Mekanik:** 2020 V-Slot profiller ile modüler ve rijit şase.
* ⏱️ **Performans:** Kesme (interrupt) tabanlı okuma ile düşük input lag.
* 🖥️ **Oyun Desteği:** ETS2, Assetto Corsa, Forza Horizon, BeamNG.drive ve daha fazlası.

### 🔧 Donanım ve Bileşenler

#### 🧠 Mikrodenetleyici & Sürücüler
| Bileşen | Tip | Açıklama |
| :--- | :--- | :--- |
| **Raspberry Pi Pico** | MCU | Çift çekirdekli ARM Cortex-M0+ |
| **Optik Enkoder** | Sensör | 360 PPR Artımlı (Incremental), 5-24V DC |
| **BTS7960B** | Sürücü | 43A Yüksek Güçlü DC Motor Sürücü (H-Bridge) |

#### 🔌 Elektronik Bileşen Listesi
| Bileşen | Adet | Kullanım Amacı |
| :--- | :---: | :--- |
| **100 kΩ Potansiyometre** | 3 | Pedal konum sensörleri (Gaz, Fren, Debriyaj) |
| **KW11-3Z Mikro Switch** | 8 | Makaralı tip - Vites yolları için konum algılama |
| **KW3A Mikro Switch** | 2 | Ekstra fonksiyon veya vites sınırları için |
| **RS232 Erkek/Dişi Konnektör** | 2 | Pedal ve vites kutusu için modüler bağlantı |

#### 🏗️ Mekanik Parçalar
* **Şase:** 2020 Alüminyum V-Slot Profil.
* **3D Baskı:** Direksiyon göbeği, vites mekanizması, pedal kolları ve kutular.
* **Hırdavat:** Yaylar, Rulmanlar (608zz vb.), M3/M5 vida ve somun setleri.

### 💻 Firmware ve Yazılım
Yazılım şu anda geliştirme aşamasındadır ve aşağıdaki temel görevleri yerine getirir:
1.  **Enkoder Okuma:** Kesme (Interrupt) tabanlı, kayıpsız ve hızlı dönüş algılama.
2.  **ADC İşleme:** Pedallardan gelen analog verinin filtrelenmesi ve ölçeklenmesi.
3.  **Vites Mantığı:** Mikro switch kombinasyonlarının vites pozisyonuna çevrilmesi.
4.  **USB HID Raporlama:** Tüm verilerin PC'ye standart joystick paketi olarak gönderilmesi.

> **Not:** Kaynak kodlar yakında bu depoya (repository) eklenecektir.

### 📦 Proje Durumu
- [x] Donanım seçimi ve tedariği
- [x] Mekanik tasarım (3D parçalar)
- [ ] Elektronik devre montajı
- [ ] Firmware geliştirme (Devam ediyor 🔨)
- [ ] Force Feedback (FFB) yazılım entegrasyonu

### 📸 Görseller
*(Proje tamamlandığında detaylı fotoğraflar ve bağlantı şemaları buraya eklenecektir.)*

### 🤝 Katkı
Bu proje Açık Kaynak (Open Source) ruhuyla geliştirilmektedir. Her türlü katkıya açıktır!
* Hata bildirmek için **Issue** açabilirsiniz.
* Geliştirmeler için **Pull Request** gönderebilirsiniz.

---

<a name="-english"></a>
## 🇺🇸 English

### 📘 Project Summary
This project is a DIY racing simulation controller built using a **Raspberry Pi Pico**, a **360 PPR optical incremental encoder**, a **3-pedal set**, and an **H-pattern manual shifter**.

The device operates as a native **USB HID controller**, requiring no additional drivers on the PC. It is optimized for low latency and high stability, providing a realistic simulation experience.

### 🚀 Features
* 🎮 **USB HID Compatible:** Plug-and-play racing wheel behavior.
* 🦶 **3 Pedals:** Throttle, Brake, and Clutch inputs.
* ⚙️ **H-Pattern Shifter:** Manual gear shifting (e.g., 6+R layout).
* 🎯 **High Precision:** 360 PPR Optical Encoder for smooth steering input.
* ⚡ **FFB Ready:** Equipped with BTS7960 Motor Driver (Hardware ready for Force Feedback).
* 🧩 **Modular Frame:** Built on 2020 V-Slot Aluminum Profiles.
* ⏱️ **Low Latency:** Interrupt-based firmware for instant response.
* 🖥️ **Compatibility:** Works with ETS2, Assetto Corsa, Forza, BeamNG, etc.

### 🔧 Components & Hardware

#### 🧠 MCU & Drivers
| Component | Type | Description |
| :--- | :--- | :--- |
| **Raspberry Pi Pico** | MCU | Dual-core ARM Cortex-M0+ |
| **Optical Encoder** | Sensor | Incremental 360 PPR, 5-24V DC |
| **BTS7960B** | Driver | 43A High Power DC Motor Driver |

#### 🔌 Electronics BOM
| Component | Qty | Purpose |
| :--- | :---: | :--- |
| **100 kΩ Potentiometer** | 3 | Pedal sensors (Linear input) |
| **KW11-3Z Micro Switch** | 8 | Roller type – Gear position detection |
| **KW3A Micro Switch** | 2 | Additional sensing |
| **RS232 Connectors (M/F)** | 2 | Modular wiring for pedals/shifter |

#### 🏗️ Mechanical Parts
* **Frame:** 2020 V-Slot Aluminum Profile.
* **3D Printed Parts:** Steering hub, shifter mechanism, pedal arms.
* **Hardware:** Springs, Bearings, M3/M5 screws & nuts.

### 💻 Firmware Overview
The firmware is currently under active development:
1.  **Fast Encoder Reading:** Interrupt-based handling to catch every pulse.
2.  **ADC Sampling:** Reading and smoothing potentiometer values for pedals.
3.  **Gear Logic:** Translating micro switch states into joystick button presses.
4.  **USB Communication:** Real-time HID report generation.

> **Note:** Source code will be pushed to this repository soon.

### 📦 Project Status
- [x] Component selection
- [x] Mechanical design (3D Modeling)
- [ ] Electronics assembly
- [ ] Firmware development (Work in Progress 🔨)
- [ ] Force Feedback (FFB) implementation

### 📸 Images
*(Photos, wiring diagrams, and videos will be added here once the build progresses.)*

### 🤝 Contributing
Contributions are welcome!
Feel free to open an **Issue** for bugs or submit a **Pull Request** for improvements.
