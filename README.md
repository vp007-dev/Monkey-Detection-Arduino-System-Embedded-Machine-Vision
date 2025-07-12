# 🐒 ESP32-CAM AI Monkey Detection Embedded Vision System

> **Real-time motion and monkey-size detection using ESP32-CAM for wildlife alert systems.**

![ESP32-CAM Monkey Detection Banner](./assets/banner.png) <!-- Replace with your banner image path if available -->

---

## 🚀 Project Overview

This project implements a **lightweight embedded vision system** using **ESP32-CAM** to detect:

- **Motion** in the camera feed
- **Approximate object height** to differentiate between **monkeys and humans**
- **Trigger digital output signals** for alarms, relays, or communication with an Arduino or IoT network.

It is designed for **forest edge farms, rooftop solar farms, or wildlife monitoring** where monkeys cause damage and need to be detected without complex AI servers.

---

## 🎯 Features

✅ Motion detection using grayscale frame differencing  
✅ Object height-based classification (monkey vs human)  
✅ Digital output trigger pin for alarms or Arduino integration  
✅ Ultra-low-cost implementation using ESP32-CAM  
✅ Easy to deploy and modify for other small animal detection tasks

---

## 🛠️ Hardware Required

| Component       | Quantity | Notes |
|-----------------|----------|-------|
| **ESP32-CAM (AI Thinker)** | 1 | Main vision module |
| FTDI programmer | 1 | For flashing ESP32-CAM |
| Arduino Uno/Nano (Optional) | 1 | For controlling relay or external devices |
| Relay module    | 1 | For siren/alarm triggering |
| Power supply 5V 2A | 1 | For stable ESP32-CAM operation |
| Connecting wires | - | Jumper wires (male-to-female) |

---

## 📝 How It Works

1. ESP32-CAM captures grayscale frames continuously.
2. Calculates **pixel-wise difference** with the previous frame.
3. If:
   - **Motion pixels exceed threshold** and
   - **Estimated object height < human height**,  
   it triggers the digital output pin.

4. The **trigger pin** can:
   - Directly activate a relay (with optocoupler driver), or
   - Send a signal to an Arduino for extended automation logic.

---

## 💻 Setup Instructions

1. **Clone this repository**

```bash
git clone https://github.com/yourusername/esp32-cam-monkey-detection.git
cd esp32-cam-monkey-detection
