# ML-powered Waste Classification and Disposal System

This project is an **AI-powered smart dustbin** that uses an ESP32-CAM and an Edge Impulse image classification model to detect the type of waste and automatically route it into different compartments using a servo motor, controlled by an Arduino UNO and visualized on an OLED display. [web:286][web:324]

---

## Features

- Automated image-based waste detection and classification (for example, dry waste vs e‑waste). [web:286][web:324]  
- On-device inference on the ESP32-CAM using a deployed Edge Impulse model. [web:286]  
- Servo-controlled mechanism to divert waste into different bins based on prediction. [web:286]  
- Real-time classification result shown on an SSD1306 OLED display. [web:286]  

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

- Arduino IDE [web:286]  
- Edge Impulse Studio (for dataset collection, model training, deployment) [web:286]  
- Libraries:
  - `esp_camera`
  - `Eloquent ESP32 Camera` (for image capture and dataset collection) [web:289]
  - `Wire`
  - `Adafruit_GFX`
  - `Adafruit_SSD1306`
  - `ESP32Servo`

---

## How It Works

1. The ESP32-CAM captures an image of the object placed near the dustbin opening. [web:286]  
2. The captured image is passed to the Edge Impulse model running on the ESP32-CAM to classify the waste type. [web:286]  
3. Based on the prediction (e.g., dry or electronic waste), the Arduino/ESP32 controls a servo motor to rotate the flap towards the corresponding compartment. [web:286]  
4. The OLED display shows the detected class and basic status messages in real time. [web:286]  

---

## Getting Started

1. Clone this repository:
git clone https://github.com/saara-sana/ML-powered-waste-classification-and-disposal-system.git
2. Open the project in Arduino IDE. [web:286]  
3. Install the required libraries listed above via Library Manager or manually. [web:287]  
4. Flash the ESP32-CAM sketch with the Edge Impulse inference code and upload the Arduino control sketch. [web:286]  
5. Assemble the hardware as shown in the circuit diagram (link in repo or documentation) and power the system. [web:286]  

---

## Future Improvements

- Add more waste classes (e.g., biodegradable, plastic, metal) by collecting a larger dataset and retraining the model. [web:288]  
- Integrate IoT features like bin-fill level monitoring and cloud logging using Wi‑Fi/MQTT. [web:288]  
- Improve enclosure design for better durability and real-world deployment. [web:288]








