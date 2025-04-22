# Smart Dustbin

This repository contains the final report (compiled in IEEE format) and Arduino code for the Smart Dustbin project, developed as part of the ES-116 course: Principles and Applications of Electrical Engineering at the Indian Institute of Technology, Gandhinagar.

## 🚀 Project Overview

The Smart Dustbin is a low-cost, Arduino-based system designed to promote hygienic and efficient waste disposal. It uses two ultrasonic sensors, a servo motor, and a 16×2 LCD to enable automated lid opening and real-time fill-level monitoring. The bin opens automatically when a hand is detected near the lid and calculates how full the bin is by measuring the distance to the waste surface. The fill percentage is displayed clearly on the LCD and printed to the Serial Monitor every 3 seconds.

## 🛠️ Components Used

- **Arduino Uno R3**  
- **2 × HC-SR04 Ultrasonic Sensors**  
- **SG90 Servo Motor**  
- **16×2 LCD (JHD162A)**  
- **10 kΩ Potentiometer**  
- **Breadboard & Jumper Wires**  
- **5 V USB Power Bank**  

## 💡 Working Principle

1. **Lid Operation**  
   - The top ultrasonic sensor detects hand proximity (Trig → D4, Echo → D5).  
   - If distance < 20 cm, the servo (signal on D6) opens the lid, holds for 3 seconds, then closes.

2. **Fill-Level Monitoring**  
   - The bottom ultrasonic sensor measures the distance from bin top to waste surface (Trig → D2, Echo → D3).  
   - Fill percentage = `map(binHeight - distance, 0, binHeight, 0, 100)`.  

3. **Display & Logging**  
   - A 16×2 LCD (pins 10, 11, 12, 13, A0, A1) shows only the percentage (e.g., “47%”).  
   - Serial Monitor prints the fill percentage every 3 seconds (`millis()` based timing).

## 📄 Report

Access the complete technical report in IEEE format:  
https://iitgnacin-my.sharepoint.com/:b:/g/personal/24110282_iitgn_ac_in/EeSjzIu5JNhKoLHzWBxxz3EB8pSsDugghVHgaDaEm5E0ag?e=BgOj1G&authuser=0

## 🎥 Demonstration Video

Watch our project demonstration on YouTube:  
https://www.youtube.com/watch?v=9y_q_Hd5wCc&authuser=0
## 👏 Acknowledgment

We thank our course instructor, Arup Lal Chakraborty, and the IIT Gandhinagar laboratory staff for their guidance and support throughout this project.

