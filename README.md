🧺 Remote Controlled Washing Machine (Wokwi Simulation)
-----------------------------------------------------------------------------

## 📌 Project Overview
-----------------------------------------------------------------

This project simulates a **Gesture Controlled Washing Machine** using an Arduino Uno in Wokwi.

Since real gesture recognition (camera + AI) is not supported in Wokwi, push buttons are used to simulate gesture inputs.

The system allows:
- Mode selection (Mixed, Whites, Quick)
- Start
- Pause
- Stop
- LED motor simulation
- LCD display feedback

---

## 🛠 Components Used
-----------------------------------------------------------------------------

- Arduino Uno
- I2C 16x2 LCD Display
- 4 Push Buttons
- 1 LED (Motor Indicator)
- 220Ω Resistor
- Breadboard
- Jumper Wires

---

## 🔌 Pin Connections

-----------------------------------------------------------------------------

### Buttons

| Button | Function | Arduino Pin |
|---------|----------|-------------|
| Button 1 | Mode Select | 6 |
| Button 2 | Start | 7 |
| Button 3 | Pause | 8 |
| Button 4 | Stop | 9 |

All buttons use `INPUT_PULLUP` mode.

---

### LED
-----------------------------------------------------------------------------

| LED Pin | Arduino |
|----------|----------|
| Anode | Pin 10 |
| Cathode | 220Ω Resistor → GND |

---

### I2C LCD
-----------------------------------------------------------------------------

| LCD Pin | Arduino |
|----------|----------|
| GND | GND |
| VCC | 5V |
| SDA | A4 |
| SCL | A5 |

I2C Address: `0x27`


## ⚙️ Features
-----------------------------------------------------------------------------

### 🌀 Wash Modes
- MIXED
- WHITES
- QUICK

Mode changes cyclically using Button 1.

### ▶ Machine States
- STARTED → LED ON
- PAUSED → LED Blinking
- STOPPED → LED OFF

### 📟 LCD Display
- Line 1: Selected Mode
- Line 2: Machine State

---

## 🧠 How It Works
-----------------------------------------------------------------------------

1. User selects wash mode.
2. User presses Start.
3. LED simulates motor operation.
4. Pause causes LED blinking.
5. Stop turns off the system.


## 🎓 Educational Purpose
-----------------------------------------------------------------------------

This project demonstrates:
- Embedded system design
- State management
- Input handling with INPUT_PULLUP
- I2C communication
- Basic washing machine logic simulation

---

## 🔮 Future Improvements
-----------------------------------------------------------------------------


- Add washing timer
- Add buzzer for completion
- Automatic wash cycle (Wash → Rinse → Spin)
- Add water level simulation
- Integrate real gesture recognition using OpenCV + Arduino (hardware version)

Platform: Wokwi Simulation  
-----------------------------------------------------------------------------
