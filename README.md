# 🛡️ SMART R4: Real-Time Embedded RFID Attendance System

[![Hardware: Arduino UNO R4](https://img.shields.io/badge/Hardware-Arduino%20UNO%20R4%20WiFi-00979D?style=for-the-badge&logo=arduino)](https://store.arduino.cc/)
[![Protocol: SPI](https://img.shields.io/badge/Protocol-SPI-red?style=for-the-badge)](https://en.wikipedia.org/wiki/Serial_Peripheral_Interface)
[![Academic: WVSU](https://img.shields.io/badge/Institution-WVSU-gold?style=for-the-badge)](https://www.wvstateu.edu/)

**SMART R4** is an enterprise-grade embedded solution designed for contactless attendance tracking. Developed as part of the **CS 445 – Embedded Systems** curriculum at **West Virginia State University**, this system leverages the Renesas RA4M1 architecture (Arduino UNO R4) and the MFRC522 radio-frequency identification module to automate identity verification.

---

## 👨‍🏫 Academic Metadata
* **Course:** CS 445 – Embedded Systems
* **Instructor:** Dr. Ali Al-Sinayyid
* **Developer:** Shikhar Pandey
* **Institution:** West Virginia State University

---

## 🏗️ System Architecture & Logic Flow

The system operates on a low-latency verification loop, utilizing the **Serial Peripheral Interface (SPI)** protocol for high-speed data transfer between the MCU and the RFID transceiver.



[Image of RFID system block diagram]


### How It Works:
1. **Signal Induction:** The MFRC522 module creates an electromagnetic field. When a passive RFID tag enters this field, it powers up and transmits its Unique Identifier (UID).
2. **Data Acquisition:** The Arduino UNO R4 captures the UID via the MFRC522 library over the SPI bus.
3. **Verification Logic:** The firmware compares the captured UID against a pre-authorized hash table stored in the MCU's flash memory.
4. **Actionable Output:** * **Authorized:** Attendance is logged with a high-precision timestamp.
   * **Unauthorized:** Access is denied, and the event is flagged in the Serial Monitor.

---

## 🛠️ Hardware Specifications

| Component | Function |
| :--- | :--- |
| **Arduino UNO R4 WiFi** | Central Processing Unit (Renesas RA4M1 ARM Cortex-M4). |
| **MFRC522 Module** | 13.56 MHz RFID Reader/Writer. |
| **RFID Tags/Cards** | Passive transponders (Mifare 1k). |
| **Logic Level Shifting** | Jumper-wire bus configuration for SPI communication. |

---

## 💻 Software & Firmware Setup

### 1. Toolchain
* **IDE:** Arduino IDE (v2.0+ recommended)
* **Board Package:** Arduino Mbed OS (UNO R4) via Board Manager.

### 2. Dependency Management
The following libraries must be initialized within the environment:
* `MFRC522.h` - Hardware abstraction for the RFID module.
* `SPI.h` - Low-level serial communication protocol.

### 3. Pin Mapping (SPI Configuration)
| MFRC522 Pin | Arduino UNO R4 Pin |
| :--- | :--- |
| **SDA (SS)** | 10 |
| **SCK** | 13 |
| **MOSI** | 11 |
| **MISO** | 12 |
| **RST** | 9 |

---

## 📈 Testing & Validation

The system underwent rigorous validation phases:
* **Protocol Verification:** Verified MOSI/MISO integrity using the Serial Monitor.
* **UID Simulation:** Stress-tested the lookup table with both authorized and "spoofed" UIDs to ensure zero false-positive entries.
* **Environmental Testing:** Validated read distances and interference levels for the 13.56 MHz frequency.

---

## 🔮 Future Roadmap
* **Cloud Integration:** Utilizing the UNO R4’s ESP32-S3 co-processor to push logs directly to a Firebase/Google Sheets database.
* **OLED Interface:** Adding an I2C-based 128x64 display for standalone visual feedback.
* **Biometric Layer:** Implementing multi-factor authentication (MFA) combining RFID and fingerprint scanning.

---

## 📝 Conclusion
The **SMART R4** project successfully demonstrates the principles of real-time embedded logic, interrupt handling, and serial communication. It provides a robust foundation for modern, low-cost institutional attendance management.

**Developed by [Shikhar Pandey](https://github.com/shikhar0777)** *Embedded Systems Engineering @ WVSU*
