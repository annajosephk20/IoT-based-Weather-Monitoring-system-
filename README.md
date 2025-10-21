# 🌦️ IoT-Based Weather Monitoring System Using NodeMCU and ThingSpeak

This project monitors real-time **temperature**, **humidity**, and **atmospheric pressure** using **DHT11** and **BMP180** sensors connected to a **NodeMCU (ESP8266)**. The data is sent to the **ThingSpeak cloud platform** via Wi-Fi, where it is visualized as live graphs.

---

## 🧠 Features

* Real-time monitoring of temperature, humidity, and pressure
* Data visualization on **ThingSpeak** cloud dashboard
* Low-cost and Wi-Fi–enabled IoT solution
* Easy to modify and expand with additional sensors

---

## ⚙️ Components Used

* NodeMCU ESP8266
* DHT11 (Temperature & Humidity Sensor)
* BMP180 (Pressure Sensor)
* Jumper wires & Breadboard
* Wi-Fi network

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

## 🧩 Libraries Required

Make sure to install these libraries from the **Arduino Library Manager**:

* `ESP8266WiFi.h`
* `ThingSpeak.h`
* `Wire.h`
* `Adafruit_Sensor.h`
* `Adafruit_BMP085_U.h`
* `DHT.h`

---

## 🛠️ How It Works

1. The DHT11 and BMP180 sensors collect temperature, humidity, and pressure data.
2. NodeMCU reads the sensor data and connects to the Wi-Fi network.
3. Data is sent to **ThingSpeak** using the provided API key.
4. The ThingSpeak channel displays live graphs of all parameters.

---

## 🚀 Setup Instructions

1. Open the code in **Arduino IDE**.
2. Install the required libraries.
3. Replace your **Wi-Fi SSID**, **password**, **ThingSpeak Channel ID**, and **API Key** in the code.
4. Upload the code to your **NodeMCU** board.
5. Open the **ThingSpeak** channel to view real-time weather data.

---

## 📊 Sample Output

**Serial Monitor Example:**

```
---- WEATHER STATION ----
Temp (DHT11): 28.5 °C
Humidity: 65.0 %
Temp (BMP180): 28.3 °C
Pressure: 1008.5 hPa
Data sent successfully!
```

---

## 📡 ThingSpeak Fields

| Field | Parameter        | Sensor |
| ----- | ---------------- | ------ |
| 1     | Temperature (°C) | DHT11  |
| 2     | Humidity (%)     | DHT11  |
| 3     | Temperature (°C) | BMP180 |
| 4     | Pressure (hPa)   | BMP180 |

---

## 🧾 License

This project is open-source and available under the **MIT License**.


