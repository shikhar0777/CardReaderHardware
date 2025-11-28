SMART R4 – RFID Attendance System

Using Arduino UNO R4 WiFi & MFRC522

Course: CS 445 – Embedded Systems
Instructor: Dr. Ali Al-Sinayyid.
Student: Shikhar Pandey
Institution: West Virginia State University


Project Overview

SMART R4 is an RFID-based attendance system developed using the Arduino UNO R4 WiFi and the MFRC522 RFID reader. When an RFID card is tapped, the system reads the card’s UID, verifies whether it is authorized, and then displays either “Access Granted” or “Access Denied” on the Serial Monitor.
Authorized entries can also be logged with timestamps for attendance tracking.

This project provides a fast, contactless, and reliable alternative to traditional manual attendance systems.

Software Setup

To run and develop this project, the following software components are required:

1. Arduino IDE (Latest Version)

Used for writing, compiling, and uploading the program.

2. Required Framework and Libraries

Install the following libraries through the Arduino IDE Library Manager:

MFRC522 Library – required for interfacing with the RFID module

SPI Library – built-in library used for SPI communication

3. Board Package

Install the board support package for:

Arduino UNO R4 / Renesas RA4M1
Available under:
Tools → Board Manager → Arduino Mbed OS (UNO R4)

This software setup ensures proper compilation, library support, and smooth communication with the hardware.

Components Used

Arduino UNO R4 WiFi

MFRC522 RFID Reader

RFID Cards/Tags

Jumper Wires

How It Works

User taps an RFID card on the MFRC522 reader

The module reads the unique UID

Arduino checks the UID against authorized values

Valid UID → Attendance recorded

Invalid UID → Access denied

Status is displayed on the Serial Monitor

Logged data can be exported to Excel or cloud storage for record-keeping

Objectives

Develop a functional RFID attendance system

Correctly read and verify RFID card UIDs

Provide a fast and error-free attendance process

Enable simple digital record management

Testing

Functionality tested through the Arduino IDE Serial Monitor

UIDs simulated and validated

SPI communication verified between Arduino and MFRC522.

Full system flow tested virtually before hardware deployment

Conclusion

The SMART R4 RFID Attendance System delivers a clean, low-cost, and modern solution for tracking attendance in classrooms, labs, offices, and similar environments. It demonstrates essential embedded systems principles and provides a strong foundation for future upgrades such as WiFi-based logging, LCD output, buzzer alerts, or full dashboard integration.
