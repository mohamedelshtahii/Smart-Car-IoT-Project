Integrated AIoT Smart Car System 🏎️🤖
Autonomous Navigation | Edge AI Sound Recognition | Cloud Telemetry
This project demonstrates a high-level convergence of Embedded Systems, Machine Learning (TinyML), and Industrial IoT (IIoT). It features a dual-controller architecture capable of real-time environmental awareness and remote data visualization.

📸 System Overview
<p align="center">
<img width="850" alt="Hardware Setup" src="https://github.com/user-attachments/assets/253e6402-dc1e-40bb-ab9e-f83cb955e8f9" />


<i><b>Figure 1:</b> The Integrated Physical Hardware Assembly & Wiring Architecture.</i>
</p>

🚀 Key Features
Edge AI Acoustic Awareness: Real-time sound classification (Bike vs. Car) using a Support Vector Machine (SVM) model optimized for ESP32.

Reflexive Control: Arduino Nano manages mechanical stability and high-speed capacitive touch sensing.

IIoT Pipeline: Industrial-grade data path sending telemetry via MQTT to a Node-RED orchestrator.

Real-time Dashboards: Advanced time-series visualization using InfluxDB and Grafana.

Contextual Stability: Automatic servo engagement logic based on IMU (MPU6050) orientation to prevent jitter.

🛠️ Tech Stack & Architecture
1. Hardware Components
ESP32: The "System Brain" – handles AI inference and Wi-Fi/MQTT communication.

Arduino Nano: The "Reflex Controller" – dedicated to real-time sensor interrupts and servo PWM.

MPU6050: 6-Axis motion tracking for orientation and velocity estimation.

HC-SR04: Ultrasonic sensor for proximity mapping and proportional braking.

Custom Chassis: Features a capacitive touch-sensitive "skin" for human-robot interaction.

2. Software & Cloud Stack
Embedded Programming: C++, TinyML (via micromlgen), arduinoFFT for signal processing.

Backend & Analytics: MQTT (Aedes Broker), Node-RED, InfluxDB (Time-Series DB).

Frontend: Grafana for professional-grade telemetry dashboards.

📊 Data Visualization & Logic
1. Cloud Telemetry Dashboard
The system publishes linear and angular velocity. Data is aggregated in InfluxDB to compute historical trends and moving averages.

<p align="center">
<img width="850" alt="Grafana Dashboard" src="https://github.com/user-attachments/assets/1bf9a27a-c8dc-401b-b46c-083ab400f4c4" />


<i><b>Figure 2:</b> Grafana Telemetry Dashboard showing real-time velocity gauges and trends.</i>
</p>

2. Node-RED Orchestration
A specialized logic flow parses raw MQTT JSON payloads, extracts variables, and performs metadata tagging before storage.

<p align="center">
<img width="850" alt="Node-RED Flow" src="https://github.com/user-attachments/assets/5d39c056-0526-45cc-8230-b3f7802852f6" />


<i><b>Figure 3:</b> Node-RED Backend flow for seamless data transformation and routing.</i>
</p>

3. Time-Series Queries (Flux)
We utilize the Flux language for windowing and noise reduction, ensuring the dashboard displays clean, actionable data.

<p align="center">
<img width="850" alt="Flux Query" src="https://github.com/user-attachments/assets/5884611b-4307-4c6b-b2a3-34437fba1b8b" />


<i><b>Figure 4:</b> InfluxDB Flux logic for data querying and edge-case filtering.</i>
</p>

🧠 TinyML Implementation
The core intelligence resides in an SVM Model trained on frequency spectrums (FFT) to distinguish engine sounds.

<p align="center">
<img width="850" alt="TinyML Code" src="https://github.com/user-attachments/assets/ae0865c1-b522-4ef9-b38e-e794cf655b96" />
</p>

Precision: 100% achieved in testing using a Linear Kernel.

Inference: Uses Cosine Similarity to ensure high-confidence classification before triggering actions.

📂 Repository Structure
Bash
├── src/
│   ├── nano/     # Arduino Nano code (Servo control, Capacitive Touch)
│   └── esp32/    # ESP32 code (TinyML, MQTT, MPU6050)
├── models/       # Python training scripts (Jupyter) and model.h
├── flows/        # Node-RED JSON flow configurations
└── docs/         # Full Technical Report and Proximity Analysis
👨‍💻 Prepared by
Mohammed Alaa Internet of Things Solutions Engineer in Training LinkedIn | GitHub
