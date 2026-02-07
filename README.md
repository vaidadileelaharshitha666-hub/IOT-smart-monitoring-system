# IOT-smart-monitoring-system
This project is an IoT-based system designed to monitor and control water quality in fish farms. It continuously measures important parameters such as pH, dissolved oxygen, temperature, and water level. The system sends data to the cloud and automatically controls an aerator when water conditions become unsafe.
This helps improve fish health, reduce losses, and minimize manual work.
System Architecture Diagram:

Sensors
  ↓
Microcontroller (ESP32/ESP8266)
  ↓ (Wi-Fi)
Cloud Platform (Firebase/ThingSpeak/Blynk)
  ↓
Web/Mobile Dashboard
  ↓
User / Farmer

Sensor list and Justification:
The system uses the following sensors to monitor water quality:
Temperature Sensor (DS18B20) - Measures water temperature, which affects fish growth and metabolism.
pH Sensor (pH-4502C) - Monitors water acidity and alkalinity to maintain a healthy environment.
Dissolved Oxygen Sensor - Measures oxygen levels required for fish respiration.
Turbidity Sensor (SEN0189) -Checks water clarity to detect pollution and waste.
Water Level Sensor (Ultrasonic) - Measures pond depth to prevent overflow and water loss.
These sensors work together to ensure proper water conditions, improve fish health, and increase aquaculture productivity.

DATA FLOW EXPLANATION:
Step-by-Step Data Flow
1.Sensors collect real-time environmental data.
2.Microcontroller reads sensor values.
3.Data is converted into digital format.
4.Preprocessing is done at edge level.
5.Data is transmitted via Wi-Fi.
6.Cloud platform stores the data.
7.Data is visualized on the dashboard.
8.Alerts are triggered if abnormal values are detected.

Data Flow Diagram:
Sensors → ESP32 → Wi-Fi → Cloud Server → Database → Dashboard → User

Edge–Cloud Processing:

Edge Device (ESP32):
Reads sensor data
Filters noise
Performs threshold checks
Cloud Server:
Stores historical data
Performs analytics
Generates reports

Sample Dashboard View:

Parameter        -Value    -Status
Temperature      -27.5°C   -Normal 
pH Level         -7.2      -Normal 
Dissolved Oxygen -6.5 mg/L -Good   
Turbidity        -12 NTU   -Normal 
Water Level      -85 cm    -Stable 

Status indicators:
Green → Normal
Yellow → Warning
Red → Critical

IoT Architecture Understanding:
This project demonstrates a layered IoT architecture:
Perception Layer  -Sensors collect data 
Transport Layer   -Wi-Fi communication
Processing Layer  -Cloud storage & analytics
Application Layer -Dashboard & alerts

Practical Feasibility:
Real-World Applicability
Uses low-cost components
Easy to deploy in fish farms
Requires minimal maintenance
Operates on low power

Edge–Cloud Logic:

In this IoT-based aquaculture system, edge–cloud logic divides data processing between local devices and remote servers. The edge device, such as ESP32 or ESP8266, collects data from sensors and performs basic processing like filtering, calibration, and threshold checking. This helps in reducing delay and minimizes unnecessary data transmission.
When abnormal conditions are detected, the edge device can generate instant alerts or take local actions. Processed data is then sent to the cloud through the internet. This ensures fast response and efficient use of network resources. The cloud stores the received data and performs advanced analysis such as trend monitoring and report generation. It also provides dashboards and notifications for users. By combining edge and cloud computing, the system ensures reliable, scalable, and real-time monitoring of aquaculture environments.

Edge-Cloud Workflow:
Sensors → Edge Device → Cloud → Analytics → Dashboard → Alerts.
