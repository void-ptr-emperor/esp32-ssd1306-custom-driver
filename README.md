# ESP32 SSD1306 Custom Bare-Metal Driver

A low-level I2C driver for the SSD1306 OLED display, written from scratch in pure C for the ESP32 microcontroller. 

## 🛠 Technical Overview
This project is a fully standalone software module. All memory management, bitwise operations, and I2C protocol timing are implemented manually without relying on external display libraries.

**Key Features:**
* **No Third-Party Libraries:** Direct bus control without heavy dependencies (e.g., Adafruit_GFX or u8g2).
* **Low-Level I2C:** Manual generation of START/STOP conditions, bit-banging, and ACK verification via GPIO Open-Drain.
* **Custom Memory Buffer:** Local 1024-byte RAM buffer for mathematical pixel and text rendering.
* **Custom Font:** Integrated lightweight ASCII character dictionary (5x7 pixels).
* **Strict Naming Convention:** Architecture is built on strict naming rules (using the custom `for_` prefix) to prevent memory and namespace conflicts with the ESP-IDF system API.

## 💻 Tech Stack
* **MCU:** ESP32
* **Framework:** ESP-IDF
* **Language:** C (C11/C17)
