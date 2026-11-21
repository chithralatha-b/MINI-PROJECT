# 🌱 Smart Plant Monitoring and Automatic Watering System

### An IoT-Based Solution for Intelligent Plant Care and Early Stress Detection

## 📌 Project Overview

Plants require regular care and suitable environmental conditions to grow and survive. Factors such as insufficient soil moisture, high temperature and unsuitable humidity can negatively affect plant health. However, manually monitoring plants every day can be difficult, especially when managing multiple plants or when regular care is overlooked.

The **Smart Plant Monitoring and Automatic Watering System** is an IoT-based project developed using the ESP32 microcontroller to monitor important environmental conditions and support timely plant care.

The system monitors soil moisture, temperature and humidity. Based on sensor readings, it identifies conditions that may affect plant health, provides visual alerts and activates a water pump when the soil becomes too dry.

The main objective is to reduce avoidable plant damage through continuous monitoring and automated watering.

## 🎯 Problem Statement

Plants may experience stress and eventually die due to:
- Insufficient or irregular watering.
- Excessive temperature.
- Unsuitable humidity conditions.
- Lack of regular monitoring and maintenance.
- Delayed identification of environmental stress.

Traditional plant care mainly depends on manual observation and watering schedules, which may not always reflect the actual requirements of a plant.

## 💡 Proposed Solution

Our system uses an ESP32-based monitoring approach to collect environmental data and respond to changing plant conditions.

The system:
- Measures soil moisture levels.
- Monitors surrounding temperature and humidity.
- Displays real-time readings on an OLED display.
- Identifies dry-soil and high-temperature conditions.
- Activates a water pump through a relay when watering is required.
- Provides visual warnings when the plant experiences unsuitable conditions.

## ⚙️ Hardware Components

| Component | Purpose |
|---|---|
| ESP32 | Main microcontroller and processing unit |
| Soil Moisture Sensor | Measures soil moisture level |
| DHT22 Sensor | Measures temperature and air humidity |
| OLED Display (SSD1306) | Displays sensor readings and plant status |
| Relay Module | Controls the water pump |
| Water Pump | Supplies water to the plant |
| LED | Provides visual alerts |
| Jumper Wires | Hardware connections |
| Power Supply | Supplies power to the components |

## 🔌 Pin Configuration

| Component | ESP32 GPIO |
|---|---|
| DHT22 Data | GPIO 4 |
| Soil Moisture Sensor | GPIO 34 |
| OLED SDA | GPIO 21 |
| OLED SCL | GPIO 22 |
| Warning LED | GPIO 2 |
| Relay Module | GPIO 26 |

**OLED I2C Address:** `0x3C`

## 🔄 Working Principle

1. **Data Collection:** The soil moisture sensor measures the moisture level in the soil, while the DHT22 measures temperature and humidity.

2. **Data Processing:** The ESP32 reads the sensor values and evaluates the environmental conditions.

3. **Condition Detection:** The system compares the readings against configured threshold values.

4. **Automatic Watering:** When the soil moisture level falls below the configured limit, the ESP32 activates the relay to operate the water pump.

5. **Temperature Monitoring:** When the temperature exceeds the configured threshold, the system generates a warning instead of automatically activating the pump.

6. **Plant Status Display:** The OLED display provides information about the current sensor readings and plant condition.

## 🧠 System Logic

The prototype uses the following example thresholds:

- Soil moisture below 30%: Dry soil detected.
- Temperature above 35°C: High-temperature warning.
- Dry soil and high temperature together: Plant stress warning.

| Condition | System Response |
|---|---|
| Normal soil moisture | Normal monitoring |
| Soil moisture below 30% | Activate water pump |
| Temperature above 35°C | Generate temperature warning |
| Dry soil + high temperature | Display plant stress warning and activate watering |

*Note: These are prototype threshold values. Actual thresholds should be adjusted according to plant species and growing conditions.*

## 🛠️ Technologies Used

- **Microcontroller:** ESP32
- **Programming Language:** Embedded C / C++
- **Development Environment:** Arduino IDE
- **Simulation Platform:** Wokwi
- **Sensors:** Soil Moisture Sensor, DHT22
- **Display:** OLED SSD1306
- **Communication Protocol:** I2C
- **Actuation:** Relay-controlled water pump

## 📚 Libraries Used

- `Wire.h`
- `DHT.h`
- `Adafruit_GFX.h`
- `Adafruit_SSD1306.h`

## 🚀 How to Run the Project

1. Clone or download this repository.
2. Open the Arduino IDE.
3. Install the required ESP32 board package.
4. Install the libraries listed above.
5. Connect the components according to the pin configuration.
6. Upload the program to the ESP32.
7. Power the system and observe the sensor readings on the OLED display.
8. Test different soil moisture and temperature conditions to observe the system response.

For the simulation version, the soil moisture input can be varied using a potentiometer in Wokwi.

## 🌍 Applications

- Home gardening.
- Indoor and outdoor plant monitoring.
- College gardens and green campuses.
- Plant nurseries.
- Small-scale agricultural applications.
- Smart gardening systems.

## 🌿 Environmental and Social Impact

The project aims to encourage responsible plant care and support plant survival through timely monitoring.

Potential benefits include:

- Reducing avoidable plant loss due to missed watering.
- Supporting efficient water usage through need-based watering.
- Encouraging awareness of environmental conditions.
- Reducing dependence on frequent manual monitoring.
- Supporting sustainable gardening practices.

## 🔮 Future Enhancements

- Integration with the Blynk IoT cloud dashboard for remote monitoring.
- Mobile notifications for abnormal environmental conditions.
- Plant-specific threshold configuration.
- Historical sensor data analysis.
- AI-based plant stress prediction.
- Multi-plant monitoring through a centralized dashboard.
- Improved automatic irrigation with water-level monitoring.

## 🏁 Project Outcome

The Smart Plant Monitoring and Automatic Watering System demonstrates how IoT technology can be used to improve plant care through environmental monitoring and automated responses.

Rather than depending entirely on manual observation, the system uses sensor data to identify conditions requiring attention and supports timely intervention.

**Our vision is simple: Don't just plant more trees. Help the plants we grow survive.**

---

### Keywords
`ESP32` `IoT` `Smart Agriculture` `Smart Gardening` `Plant Monitoring` `Automatic Watering` `Soil Moisture Sensor` `DHT22` `Embedded Systems` `Arduino IDE` `Wokwi`
