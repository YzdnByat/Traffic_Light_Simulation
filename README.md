# Smart Traffic Light Control System (4-Way Intersection)

This project implements a **smart traffic light control system** for a four-way intersection.  
The system supports **normal traffic flow**, **pedestrian control**, **emergency overrides**, and **adaptive timing based on traffic density**.  
It was fully designed in **C/Assembly for microcontrollers** and **simulated in Proteus**.

---

## 🎯 Objectives
- Manage traffic lights for a four-way intersection with **dynamic timing adjustment**.
- Enable **special conditions** such as:
  - Emergency vehicle priority.
  - Pedestrian crossing requests.
  - Adaptive timing based on traffic congestion (via sensors).
- Provide a **realistic simulation** in Proteus for testing functionality.

---

## ⚙️ System Inputs
- **Timing Control Keys**
  - Increase/Decrease green light duration.
- **Emergency Switch**
  - Immediate override for emergency vehicles (ambulance, police, fire truck).
- **Pedestrian Crossing Button**
  - Activates pedestrian-friendly signal cycle.
- **Traffic Sensors**
  - Detect number of vehicles and adjust timing dynamically.

---

## 💡 System Outputs
- **LED Traffic Lights** for each lane:
  - Green → Go
  - Yellow → Ready
  - Red → Stop
- **Pedestrian LED Indicators**
  - Walk / Don’t Walk signals.
- **Adaptive Timing**
  - Dynamic adjustment of green light duration (±2 seconds per press or based on sensors).

---

## 🔄 System Operation
1. **Normal Cycle**
   - Traffic lights cycle sequentially through 4 phases:
     - North–South Green, East–West Red
     - North–South Yellow, East–West Red
     - East–West Green, North–South Red
     - East–West Yellow, North–South Red
   - Default timings: Green = 12s, Yellow = 3s, Red = 12s.
2. **Emergency Mode**
   - Activated by emergency switch.
   - All lights reset to **give priority to emergency direction**.
   - Holds for 10 seconds before resuming normal cycle.
3. **Pedestrian Mode**
   - Triggered by crossing button.
   - Pauses vehicle lights and enables pedestrian signals.
4. **Adaptive Mode**
   - Sensors measure vehicle density.
   - Congested lanes receive extended green time.
   - Light timing auto-adjusts in real time.

---

## 🖥️ Simulation
- Designed and tested in **Proteus**.
- Components used:
  - Microcontroller (PIC/AVR/8051 depending on implementation).
  - LEDs for traffic lights.
  - Push buttons for pedestrian/emergency inputs.
  - Virtual traffic sensors.
- All modes (normal, emergency, pedestrian, adaptive) were verified.

---

## 📂 Repository Structure
