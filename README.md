SMART R4 – RFID Attendance System
Using Arduino UNO R4 WiFi & MFRC522

Course: CS 445 – Embedded Systems
Instructor: Dr. Ali Al-Sinayyid
Student: Shikhar Pandey
West Virginia State University

Project Overview

The SMART R4 project is a simple RFID-based attendance system that uses the Arduino UNO R4 WiFi and the MFRC522 RFID reader.
When an RFID card is tapped, the system reads the card’s UID, checks if it is authorized, and displays Access Granted or Access Denied on the Serial Monitor. Authorized scans can be logged with timestamps for attendance tracking.

The system provides a fast, contactless, and reliable alternative to manual attendance methods.

💻 Software Setup

To run this project, you need:

1. Arduino IDE (Latest Version)

Used for writing, compiling, and uploading the code.

2. Required Framework & Packages

Install the following libraries in Arduino IDE:

MFRC522 Library (for the RFID module)

SPI Library (built-in, used for communication)

3. Board Package

Arduino UNO R4 / Renesas RA4M1 Board Support
(Install from: Tools → Board Manager → Arduino Mbed OS / UNO R4)

That’s all needed for development, testing, and uploading.

Components Used

Arduino UNO R4 WiFi

MFRC522 RFID Reader

RFID Tags/Cards

Jumper Wires

How It Works

User taps the RFID card

MFRC522 reads the card UID

Arduino processes and checks authorization

Valid UID → Attendance recorded

Invalid UID → Access denied

Results shown on Serial Monitor

Data can be exported to an Excel sheet or cloud system

Objectives

Build a simple RFID attendance system

Read and verify card UIDs accurately

Make attendance fast and error-free

Allow easy digital record-keeping

Testing

Code tested through Arduino IDE Serial Monitor

UIDs simulated and validated

SPI communication verified

Full flow tested virtually before hardware connection

Conclusion

The SMART R4 RFID Attendance System is a clean, low-cost, and modern solution for classrooms, labs, and offices. It demonstrates key embedded systems concepts and can be upgraded easily with WiFi logging, LCD display, buzzer alerts, or a full dashboard.


