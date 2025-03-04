# IoT-Based Air Quality Monitoring System Using CAN Protocol

## Overview
Air pollution has become a critical concern affecting both human health and the environment. This project proposes an **IoT-based Air Quality Monitoring System** utilizing the **Controller Area Network (CAN) protocol** for reliable and efficient data transmission.

## System Architecture
The system comprises **two ESP32 microcontrollers** that communicate using the **MCP2515 CAN module**:
1. **Node 1 (Data Collection & Transmission):**
   - Collects real-time air quality data using sensors:
     - **Nova PM SDS011** – Particulate Matter (PM2.5, PM10)
     - **DHT22** – Temperature & Humidity
     - **MQ135** – Harmful Gas Detection
   - Displays data on a **0.96-inch OLED screen**
   - Transmits data via **CAN communication** to Node 2

2. **Node 2 (Data Processing & Cloud Integration):**
   - Receives data from Node 1 over CAN protocol
   - Processes and uploads data to **ThingSpeak**, a cloud-based IoT analytics platform

## Features
- **Real-time Monitoring:** Provides instant air quality updates
- **Reliable Communication:** Uses CAN protocol for interference-free data transfer
- **Remote Accessibility:** Data is accessible from anywhere via ThingSpeak
- **Cost-effective & Scalable:** Suitable for industrial and environmental applications

## Hardware Requirements
- **ESP32 (x2)** – Microcontrollers for data collection and processing
- **MCP2515 CAN Module (x2)** – CAN communication module
- **Nova PM SDS011** – Particulate matter sensor
- **DHT22** – Temperature and humidity sensor
- **MQ135** – Harmful gas detection sensor
- **0.96-inch OLED Display** – For real-time data visualization
- **CAN Bus Transceiver (SN65HVD230 or equivalent)** – Required for CAN communication

## Software Requirements
- **Arduino IDE** – For programming ESP32
- **ESP32 Board Package** – Installed in Arduino IDE
- **ThingSpeak API** – Cloud-based data analytics platform
- **Libraries Required:**
  - `Adafruit_Sensor.h`
  - `DHT.h`
  - `MQ135.h`
  - `SDS011.h`
  - `Wire.h`
  - `Adafruit_GFX.h`
  - `Adafruit_SSD1306.h`
  - `CAN.h`

## Installation & Setup
1. **Hardware Connections:**
   - Connect sensors to the first ESP32
   - Set up CAN communication between ESP32s
2. **Software Configuration:**
   - Install required libraries in Arduino IDE
   - Configure ThingSpeak API credentials
3. **Flashing Code:**
   - Upload the respective codes to **ESP32 Node 1** (Data collection) and **ESP32 Node 2** (Processing & Cloud Integration)
4. **Monitoring Data:**
   - View real-time air quality data on OLED display
   - Access ThingSpeak dashboard for remote monitoring


## Future Improvements
- Adding **GPS module** for location-based pollution tracking
- Implementing **machine learning** for predictive analytics
- Developing a **mobile app** for better user accessibility

## Contributing
Feel free to fork this repository, improve the system, and submit a pull request. Feedback and contributions are highly appreciated!

## License
This project is licensed under the **MIT License**.

---
*Developed by Akhilesh Manoj Lad*
