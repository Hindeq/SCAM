# 🩺 SCAM – Contextual Monitoring of Cardio-Motor Anomalies

SCAM is an intelligent IoT system that monitors physiological parameters (BPM, SpO₂) and motion (accelerometer & gyroscope) in real-time to detect anomalies such as tachycardia, bradycardia, and falls.
It combines an ESP32 with sensors, a distributed backend, a Flutter Web interface deployed on Netlify, and cloud services for processing, authentication, and alert management.

---

## 🚀 Key Features

* Read physiological data via sensors (BPM, SpO₂)
* Analyze inertial signals (accelerometer & gyroscope)
* Real-time detection of cardio-motor anomalies
* Alert management and data logging
* Flutter Web dashboard displaying:

  * BPM / SpO₂ charts
  * Detected anomalies
  * Alert history
* Secure authentication via Firebase
* IoT → Cloud communication via ESP32

---

## 🏗️ System Architecture

![General Architecture](./architecture.jpeg)

---

## 📡 IoT System Diagram

The diagram below shows the connections between the ESP32, sensors, and LCD screen.
![IoT Diagram](schema_iot.png)

### 🔌 Main Connections

**MAX30102 → ESP32 (I2C)**

* VIN → 3.3V
* GND → GND
* SDA → GPIO 25
* SCL → GPIO 26

**MPU6050 → ESP32 (I2C)**

* VCC → 3.3V
* GND → GND
* SDA → GPIO 25
* SCL → GPIO 26

**LCD 16×4 → ESP32 (Custom I2C)**

* VCC → 5V
* GND → GND
* SDA → GPIO 25
* SCL → GPIO 26

---

## 🛠️ Technologies Used

### Frontend

* Flutter Web
* Deployed on Netlify

### Backend / Processing

* API + Python processing deployed on Render

### Cloud & Data

* Firebase Authentication
* Firebase Realtime Database (live data)
* Supabase (alert storage & history)

### Hardware

* ESP32
* MAX30102 sensor
* MPU6050 (IMU)

---

## 🔗 Overall Workflow

1. **ESP32** reads BPM, SpO₂, accelerometer, and gyroscope data.
2. Data is sent to the **Render backend**, processed, and simultaneously sent to **Firebase** for real-time dashboard visualization.
3. Render publishes alerts to **Supabase**.
4. The **Flutter Web interface (Netlify)** fetches and displays:

   * Real-time measurements
   * Detected alerts
   * Anomaly history

The entire pipeline operates continuously in real-time.

---

[Project Repository & Assets](https://github.com/user-attachments/assets/0490d894-e8a2-4f73-82d4-a3bbb7b8ca40)

## ❤️ Team

This project was a collaboration between students from **Data Analytics & Artificial Intelligence** and **Master of Computer Engineering & Distributed Systems**, as part of the **IoT & Networking** and **Cloud Computing** modules.

### Master ADIA – Data Analytics & Artificial Intelligence

* Hind ELQORACHI
* Latifa KHAIR
* Kawtar KINAD

### Master IISE – Computer Engineering & Distributed Systems

* Meryam EL HEFIANE
* Jihad AHBRI
* Farah BABA

---

## Supervision

The project was supervised by instructors responsible for the respective modules:

* [Prof. Amine RGHIOUI], [Internet of Things]
* [Prof. Monsef BOUGHROUS], [Networking / Cloud Computing]

---

## 📄 License

Academic project — not intended for commercial use.
**Ibn Zohr University - IT Center of Excellence**
