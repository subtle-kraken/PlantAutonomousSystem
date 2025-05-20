# PlantAutonomousSystem
I want my plant to survive on its own


# 🌱 Smart Plant Watering System with ESP32

This project is an automated plant watering system using an ESP32, a soil moisture sensor, a water pump, and a water level alarm. It features a WiFi-enabled web interface to:

- Monitor soil moisture and water level
- Automatically water the plant every 10 minutes if needed
- Set the soil moisture threshold
- Trigger and stop an alert buzzer
- Manually test the buzzer

## 🔧 Features

- Web interface (served by the ESP32)
- Soil moisture monitoring
- Water level detection with buzzer alert (max 5 min)
- Adjustable moisture threshold
- Manual buzzer test and override
- Watering relay control

## 🧪 Demo

Access the ESP32 via its local IP address (shown in the serial monitor) and control the system from any device on the same network.

## 🛠️ Hardware Required

| Component                           | Quantity | Notes                                              |
|-------------------------------------|----------|----------------------------------------------------|
| ESP32 Dev Board                     | 1        | Any standard ESP32 module                         |
| Soil Moisture Sensor (analog)       | 1        | 3-pin sensor with AO pin                          |
| Water Level Sensor (or float switch)| 1        | Digital or analog; connected to GPIO 26          |
| Relay Module 5V (1-channel)         | 1        | Controls the water pump                           |
| Buzzer (Active)                     | 1        | GPIO 27                                           |
| Water pump (5V)                     | 1        | Powered by external 5V (e.g., 4xAA or USB)       |
| USB power supply or battery pack    | 1        | For powering ESP32 and peripherals               |
| Jumper wires + breadboard or solder | -        | For connections                                   |

## 📦 Optional

- Grow light (controlled via another relay)
- USB-to-terminal block adapter (if cutting cables is undesired)

## 🔌 Wiring Notes

- Connect sensors as described in code (`moistureSensorPin = 34`, `waterLevelPin = 26`)
- Relay IN → GPIO 5; Buzzer → GPIO 27
- Use VIN or a separate 5V supply if peripherals draw too much current

## 🖥️ How to Use

1. Upload the code using Arduino IDE (set board to `ESP32 Dev Module`)
2. Connect to WiFi (credentials in code)
3. Open serial monitor to find local IP
4. Access the web page from your browser
5. Set thresholds, test buzzer, or monitor status remotely

