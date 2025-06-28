# 🌾 Smart Agriculture System using AI & IoT

An innovative smart farming solution built using **ESP32**, **IoT sensors**, **Firebase**, and **AI (Groq API)** to automate irrigation decisions based on real-time soil and weather conditions. Includes both **manual** and **auto** control with SMS alerts via **Twilio**.

---

##  Project Overview

This project helps farmers save water and improve crop health by:
- Monitoring **soil moisture**, **temperature**, and **humidity**.
- Fetching real-time **weather data** from OpenWeatherMap.
- Using **AI predictions** to decide whether to irrigate.
- Automatically controlling a water pump via **relay module**.
- Providing **manual override** via a secured web dashboard.
- Sending **SMS alerts** to farmers using Twilio API.

---

##  Technologies Used

- **ESP32 DevKit V1**
- **DHT22** (Temp & Humidity sensor)
- **Soil Moisture Sensors** (x3 for accuracy)
- **OpenWeatherMap API**
- **Groq AI API** (for irrigation decisions)
- **Firebase Realtime Database**
- **Twilio API** (for SMS alerts)
- **Web Dashboard** with login protection (Auto/Manual toggle)

---

##  How It Works

```mermaid
flowchart LR
    SoilSensors --> ESP32
    DHT22 --> ESP32
    ESP32 --> OpenWeather[OpenWeatherMap]
    ESP32 --> Firebase
    ESP32 --> GroqAI
    GroqAI --> ESP32
    ESP32 --> RelayModule
    ESP32 --> TwilioSMS
    Firebase --> WebDashboard
