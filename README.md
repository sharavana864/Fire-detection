
# 🔥 Fire & Gas Detection System with Arduino

## 📌 Project Overview
This project is an IoT-based fire and gas detection prototype using an **Arduino Uno**. It monitors:
- **Temperature** using a TMP36 sensor
- **Gas leakage** using an MQ gas sensor  
If fire/gas is detected, it:
- Sounds a **buzzer**
- Opens **two servo-controlled doors**
- Shows an **LCD alert**
- Activates an **RGB LED** (red for danger, green for safe)

---

## 🧠 Features
- 🚨 Alerts for fire/gas
- 🔄 Reset mechanism using a push button
- 📟 Real-time display on 16x2 LCD
- ⚙️ Automatic servo door control
- 🎨 RGB LED indicators (safe/danger)

---

## 🧰 Hardware Requirements
- Arduino Uno
- MQ gas sensor (connected to A1)
- TMP36 temperature sensor (connected to A0)
- 2x Servo motors (D10 & D11)
- RGB LED (Red: D9, Green: D8)
- 16x2 LCD display (D2-D7)
- Buzzer (D12)
- Push button (D13)
- Breadboard, jumper wires, resistors

---

## 🔌 Pin Configuration

| Component         | Arduino Pin |
|------------------|-------------|
| TMP36 Temp       | A0          |
| MQ Gas Sensor    | A1          |
| Buzzer           | D12         |
| Servo 1          | D11         |
| Servo 2          | D10         |
| RGB LED (Red)    | D9          |
| RGB LED (Green)  | D8          |
| LCD RS           | D7          |
| LCD Enable (E)   | D6          |
| LCD D4-D7        | D2-D5       |
| Push Button      | D13         |

---

## 💻 How It Works
- Reads **temperature** from TMP36 and **gas level** from MQ sensor.
- If `temperature > 37°C` or `gas level > 700`, the system:
  - Turns **red LED** on
  - Activates **buzzer**
  - Opens **servo doors**
  - Shows **"DANGER!! VACATE Building"** on LCD
- Push button on D13 resets the system to safe state.
- **Danger Condition**:
DANGER!!
VACATE Building!
![Screenshot 2025-07-02 190327](https://github.com/user-attachments/assets/d34b7c8f-7388-407b-bda6-5e41a9bec8cd)![Screenshot 2025-07-02 185238](https://github.com/user-attachments/assets/f256beb1-516e-4255-9ad8-80ed4bcfebcd)



# 🛠 Future Improvements
- Send alerts to phone using Blynk/IFTTT
- Add real-time monitoring on web/mobile app
- Add smoke sensor for better accuracy
- #CODE in 'fire.io'
---

## 📟 LCD Output

- **Safe Condition**:
- SAFE 29.30C
Gas Conc.: 110
