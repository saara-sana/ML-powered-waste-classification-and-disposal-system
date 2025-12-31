# ML-powered Waste Classification and Disposal System

This project is an **AI-powered smart dustbin** that uses an ESP32-CAM and an Edge Impulse image classification model to detect the type of waste and automatically route it into different compartments using a servo motor, controlled by an Arduino UNO and visualized on an OLED display.

---

## Features

- Automated image-based waste detection and classification (for example, dry waste vs e‑waste).
- On-device inference on the ESP32-CAM using a deployed Edge Impulse model.
- Servo-controlled mechanism to divert waste into different bins based on prediction.
- Real-time classification result shown on an SSD1306 OLED display.

---

## Hardware Used

- Arduino UNO
- ESP32-CAM module
- I2C OLED Display (SSD1306)
- Servo motor
- Cardboard / enclosure for dustbin body
- Jumper wires and breadboard

---

## Software & Libraries

- Arduino IDE
- Edge Impulse Studio (for dataset collection, model training, deployment)
- Libraries:
  - `esp_camera`
  - `Eloquent ESP32 Camera` (for image capture and dataset collection)
  - `Wire`
  - `Adafruit_GFX`
  - `Adafruit_SSD1306`
  - `ESP32Servo`

---

## How It Works

1. The ESP32-CAM captures an image of the object placed near the dustbin opening.
2. The captured image is passed to the Edge Impulse model running on the ESP32-CAM to classify the waste type.
3. Based on the prediction (e.g., dry or electronic waste), the Arduino/ESP32 controls a servo motor to rotate the flap towards the corresponding compartment.
4. The OLED display shows the detected class and basic status messages in real time.

---

## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/saara-sana/ML-powered-waste-classification-and-disposal-system.git
