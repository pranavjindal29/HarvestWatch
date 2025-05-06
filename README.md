# Harvest Watch - IoT and ML for Agriculture    

## 🌱 Overview

Plant diseases pose a serious threat to food security and the agricultural economy. Traditional manual inspection methods are labor-intensive, time-consuming, and often too slow to prevent damage. Our project introduces an intelligent smart farming system that combines **Machine Learning (ML)** and **Internet of Things (IoT)** technologies to assist farmers in monitoring their crops and detecting plant diseases early and accurately.

This repository contains the code, models, and documentation for our **Final Year B.Tech Project**, developed collaboratively by a team of 5 students.  
**Contributor Focus: Pranav Jindal — Developed the ML model for plant disease detection.**

---

## 🚀 Features

### 🔍 Plant Disease Detection
- **CNN Model (GoogLeNet / Inception_V3)** trained on the [PlantVillage Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease).
- 54,304 images across 14 crop species and multiple diseases.
- Integrated using **TensorFlow Lite (TFLite)** for on-device inference.
- Farmers can upload or scan plant images using the Android app to receive instant results.

### 🌿 Disease Remedies and Suggestions
- Disease-specific recommendations for fertilizers, pesticides, and organic treatments.
- Empowers farmers with actionable insights to improve crop health.

### 📡 Real-Time Farm Monitoring (IoT)
- **ESP8266-based sensor node** connected with:
  - **DHT11** sensor for temperature and humidity.
  - **Soil moisture sensor** for irrigation insights.
- Sends live data to **ThingSpeak** cloud via WiFi.
- Built-in LED indicators for sensor operation and data transmission status.

### 🔐 Authentication and Scalability
- **Firebase Authentication** with Google Sign-In for secure user access.
- Scalable backend architecture for user and data management.
- Future scope includes MQTT-based real-time communication and OTA updates.

---

## 📱 Tech Stack

| Component | Technology |
|----------|-------------|
| Frontend | Android (Java/Kotlin) |
| ML Model | CNN (Inception_V3), TensorFlow, TFLite |
| IoT | ESP8266, DHT11, Soil Moisture Sensor, Arduino IDE |
| Cloud | ThingSpeak (IoT), Firebase (Auth & Database) |
| Backend Integration | HTTP APIs, Future: MQTT |

---

## 🧠 Machine Learning Model

- **Model Architecture**: GoogLeNet (Inception_V3)
- **Framework**: TensorFlow
- **Conversion**: TensorFlow Lite (.tflite) for mobile deployment
- **Training Dataset**: [PlantVillage](https://www.kaggle.com/datasets/emmarex/plantdisease)
- **Accuracy**: Achieved high precision in classifying diseases from image inputs.

**Pranav Jindal** led the ML module development, including:
- Data preprocessing and augmentation
- Model training and evaluation
- Conversion to TFLite format

---

## 🧪 How to Run

### ML Model (Standalone)
1. Clone the repo:
    ```bash
    git clone https://github.com/yourusername/HarvestWatch.git
    ```
2. Navigate to the model directory and run:
    ```python
    python train_model.py
    ```
3. Convert to TFLite:
    ```python
    python convert_to_tflite.py
    ```

### Android App
1. Open the project in Android Studio.
2. Connect your Android device or use an emulator.
3. Run the app and use the camera/gallery to test plant disease detection.

### IoT Node
1. Upload `iot_sensor_code.ino` to ESP8266 using Arduino IDE.
2. Monitor real-time data on ThingSpeak.
3. Check LED indicators for data transmission.

---

## 📸 Screenshots

> Add screenshots/gifs here of the app UI, disease detection in action, and IoT dashboard.

---

## 🔭 Future Scope

- Implement MQTT for faster real-time data streaming.
- Expand plant disease classes and improve detection accuracy.
- Add OTA (Over-the-Air) updates for ESP8266 firmware.
- Integrate local language support for farmers.

---

