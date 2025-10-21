# 🌦️ IoT-Based Weather Monitoring System Using NodeMCU and ThingSpeak

This project monitors real-time **temperature**, **humidity**, and **atmospheric pressure** using **DHT11** and **BMP180** sensors connected to a **NodeMCU (ESP8266)**. The data is sent to the **ThingSpeak cloud platform** via Wi-Fi, where it is visualized through live graphs and dashboards.

---

## 🧠 Features

* Real-time monitoring of temperature, humidity, and pressure
* Cloud-based data visualization using **ThingSpeak**
* Low-cost, energy-efficient, and Wi-Fi–enabled IoT system
* Simple to assemble and easy to expand with additional sensors

---

## ⚙️ Components Used

* NodeMCU ESP8266
* DHT11 Sensor (Temperature & Humidity)
* BMP180 Sensor (Barometric Pressure)
* Breadboard and Jumper Wires
* Wi-Fi Connection

---

## 🔌 Circuit Connections

| Component    | NodeMCU Pin |
| ------------ | ----------- |
| DHT11 Data   | D4 (GPIO2)  |
| BMP180 SDA   | D2          |
| BMP180 SCL   | D1          |
| Power (VCC)  | 3.3V        |
| Ground (GND) | GND         |

---

## 🖼️ Circuit Diagram
![weather circuit diagram](https://github.com/user-attachments/assets/8bb29114-87c9-43ca-b2a8-8d8b213b2c69)


## 🧩 Required Libraries

Install the following libraries in **Arduino IDE** before uploading the code:

* `ESP8266WiFi.h`
* `ThingSpeak.h`
* `Wire.h`
* `Adafruit_Sensor.h`
* `Adafruit_BMP085_U.h`
* `DHT.h`

---

## 🛠️ How It Works

1. The DHT11 and BMP180 sensors measure environmental parameters.
2. The NodeMCU ESP8266 reads sensor data and connects to Wi-Fi.
3. The measured data is sent to the **ThingSpeak** channel using an API key.
4. ThingSpeak displays live graphs of temperature, humidity, and pressure in real time.

---

## 🚀 Setup Instructions

1. Open the project code in **Arduino IDE**.
2. Install the required libraries listed above.
3. Replace the Wi-Fi **SSID**, **password**, **Channel ID**, and **Write API Key** with your own.
4. Connect your NodeMCU to your PC and upload the code.
5. Open the Serial Monitor to verify data transmission.
6. Visit your **ThingSpeak channel** to view real-time updates.

---

## 📊 Sample Serial Output

```
---- WEATHER STATION ----
Temp (DHT11): 28.5 °C
Humidity: 65.0 %
Temp (BMP180): 28.3 °C
Pressure: 1008.5 hPa
Data sent successfully!
```

---

## 📡 ThingSpeak Field Mapping

| Field   | Parameter        | Sensor |
| ------- | ---------------- | ------ |
| Field 1 | Temperature (°C) | DHT11  |
| Field 2 | Humidity (%)     | DHT11  |
| Field 3 | Temperature (°C) | BMP180 |
| Field 4 | Pressure (hPa)   | BMP180 |

