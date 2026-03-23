Integrated AIoT Smart Car System 🏎️🤖
Autonomous Navigation | Edge AI Sound Recognition | Cloud Telemetry

This project demonstrates a high-level convergence of Embedded Systems, Machine Learning (TinyML), and Industrial IoT (IIoT). It features a dual-controller architecture capable of real-time environmental awareness and remote data visualization.

📸 System Overview
<p align="center">
<img src="Screenshot_1.jpg" width="600" alt="Physical Hardware Setup">


<i>Figure 1: The Integrated Physical Hardware Assembly</i>
</p>

🚀 Key Features
Edge AI Acoustic Awareness: Real-time sound classification (Bike vs. Car) using an SVM model on ESP32.

Reflexive Control: Arduino Nano manages mechanical stability and capacitive touch sensing.

IIoT Pipeline: Telemetry data sent via MQTT to a Node-RED orchestrator.

Real-time Dashboards: Time-series data visualization using InfluxDB and Grafana.

Contextual Stability: Automatic servo engagement based on IMU (MPU6050) orientation.

🛠️ Tech Stack & Architecture
Hardware Components
ESP32: The "Brain" for AI inference and Wi-Fi/MQTT gateway.

Arduino Nano: The "Reflex" controller for servos and touch sensors.

MPU6050: 6-Axis motion tracking.

HC-SR04: Ultrasonic proximity mapping.

Custom Chassis: Equipped with capacitive touch sensitive skin.

Software & Cloud
Embedded: C++, TinyML (micromlgen), arduinoFFT.

IoT Stack: MQTT (Aedes), Node-RED, InfluxDB, Grafana.

📊 Data Visualization & Logic
1. Cloud Telemetry Dashboard
The system reports linear and angular velocity in real-time. This data is processed through InfluxDB to provide historical trends and performance metrics.

<p align="center">
<img src="Screenshot_3.png" width="800" alt="Grafana Dashboard">


<i>Figure 2: Grafana Telemetry Dashboard showing Real-time Velocity Gauges</i>
</p>

2. Node-RED Orchestration
The backend uses a specialized logic flow to parse JSON payloads from the car and route them into the database bucket.

<p align="center">
<img src="Screenshot_2.png" width="800" alt="Node-RED Flow">


<i>Figure 3: Node-RED Backend Flow for Data Transformation</i>
</p>

3. Time-Series Queries (Flux)
Advanced data windowing and filtering are performed using the Flux language to ensure smooth visualization of sensor data.

<p align="center">
<img src="Screenshot_4.png" width="800" alt="InfluxDB Flux Query">


<i>Figure 4: InfluxDB Data Querying and Processing Logic</i>
</p>

🧠 TinyML Implementation
The core intelligence is a Support Vector Machine (SVM) model trained on 512-point FFT frequency vectors.

Accuracy: 100% precision in test environments.

Method: Cosine Similarity calculation on the edge for high-confidence classification.

📂 Repository Structure
/src/nano/: Arduino Nano code for reflex control.

/src/esp32/: ESP32 code for AI and MQTT.

/models/: Python training scripts and model.h.

/flows/: Node-RED JSON flow configurations.

👨‍💻 Prepared by
Mohammed Alaa Internet of Things Solutions Engineer in Training LinkedIn | GitHub
