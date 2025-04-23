# 🔐 Fingerprint-Based Door Lock System Using ATmega328 + Keypad

This project implements a **biometric door lock system** using a fingerprint sensor and keypad interfaced with an **ATmega328 microcontroller** (Arduino Uno or standalone). It enables fingerprint **enrollment** and **authentication**, with access granted based on stored fingerprint IDs. The system is ideal for **home automation, secure labs, offices**, and educational demos.

---

## 📌 Features

- 🧠 **Biometric Authentication:** Unlocks door based on registered fingerprint.
- 🔢 **Keypad-Controlled ID Entry:** Enrolls fingerprint IDs using a 4x4 matrix keypad.
- 💾 **Fingerprint Enrollment:** Records and stores fingerprints directly from sensor and keypad.
- 🔒 **Access Control:** Unlocks a relay or door lock when authorized ID is detected.
- 🔄 **Real-Time Serial Monitor Output** for debugging and feedback.
- 💡 **Indicator LED** (pin 13) toggles for successful authentication.

---

## 🔧 Hardware Required

| Component                  
|-----------------------------
| ATmega328 Microcontroller / Arduino Uno 
| R305 / GT511C3 Fingerprint Sensor 
| 4x4 Matrix Keypad           
| LED (Pin 13) or Relay Module
| Jumper Wires / Breadboard   | As needed |
| Power Supply 5V for ATmega328 and 3.3v for fingerprint sensor        

---

## 🖥️ Libraries Required

- `Adafruit_Fingerprint`  
- `Keypad`

> These can be installed via Arduino Library Manager.

---

## ⚙️ Pin Configuration

| Device               | ATmega328 Pin |
|----------------------|---------------|
| Fingerprint Sensor TX | D10 (SoftwareSerial RX) |
| Fingerprint Sensor RX | D11 (SoftwareSerial TX) |
| Keypad Row Pins       | D2, D3, D4, D5 |
| Keypad Column Pins    | D6, D7, D8, D9 |
| Output LED / Relay    | D13            |

---

## 🔐 How It Works

### 1. **Enrollment:**
- Use the keypad to enter the ID (1–127) where the fingerprint will be stored.
- Place your finger twice to complete the enrollment process.

### 2. **Authentication:**
- Place a registered finger on the sensor.
- If ID is recognized, pin 13 (connected to a lock or indicator LED) is turned **HIGH** for a set time.
- You can set different actions based on different IDs (e.g., different access levels or timeouts).

### 3. **Serial Monitor Feedback:**
- Displays instructions and system status.
- Helpful for monitoring stored templates, enrollments, and matches.

---

## 🚀 Getting Started

1. Wire your components according to the pin configuration.
2. Install the required libraries.
3. Upload the sketch to Arduino UNO or ATmega328 using Arduino IDE.
4. Open the Serial Monitor (9600 baud) for interaction and debugging.
5. Use the keypad to enroll new fingerprints.
6. Test authentication with registered fingers.

---


## 🙌 Junaid Shabeer

Junaid Shabeer 
*Experimental Physicist & Embedded Systems Developer*  
LinkedIn Profile :->  www.linkedin.com/in/junaid-shabeer-machine-learning-physicist-b860a4285 
