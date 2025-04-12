# 👻 PEACEKEEPER: Paranormal Entity Awareness & Communication Environment Keeper

**An Arduino-based ghost monitoring and village alert system** built during a hackathon *(GhostHacks Hackathon - Penn State Abington)* to help restless spirits and nearby villagers find peace. The PEACEKEEPER uses environmental sensors to detect potential ghostly presences and alerts villagers of paranormal threats in real time!

---

## 🧠 Project Idea
In a world haunted by the unknown, **PEACEKEEPER** watches over the living and senses the unrest of the dead. If strange activity is detected, it triggers alarms and visual signals, warning nearby villagers of entities like **poltergeists**, **residual ghosts**, and more.

---

## 🧰 Hardware Used
- Elegoo Uno R3
- DHT11 Temperature & Humidity Sensor  
- HC-SR04 Ultrasonic Distance Sensor  
- Red LED (danger)  
- Blue LED (cold spot warning)  
- Passive Buzzer (audio alert)  
- Jumper wires, breadboard  

---

## 📊 How It Works

| Sensor | Behavior | Ghost Type |
|--------|----------|------------|
| 🌡️ **DHT11** | Detects sharp **drops in humidity/temperature** | **Funnel or Residual Ghost** |
| 📏 **Ultrasonic Sensor** | Detects **nearby movement** or presence | **Poltergeist or Shadow Figure** |

- **Sudden humidity rise** → 🔵 Blue LED + high-pitched buzzer (1000 Hz) = ⚠️ Possible ghost cold spot
- **Movement under 6 cm** → 🔴 Red LED + scary buzzer (500 Hz) = 🚨 Danger zone!
- All data is sent via **Serial output** for real-time graphing in Processing

---

## 💡 Features
- Real-time environmental monitoring
- Audio-visual feedback for alerting nearby "villagers"
- Expandable with AI ghost classification or scary sound generation 👀

---

## 👾 Sample Output
```
Temp: 23.4°C | Humidity: 56.2% | Distance: 9.4 cm
Temp: 23.0°C | Humidity: 57.8% | Distance: 5.7 cm → [ALERT!]
```

---

## 👻 Future Ideas
- AI-based ghost personality generator or classifier
- Sound analysis for EVP-style detection
- Villager fear response detection using voice/emotion analysis
- Smooth integration with Processing for ghost graphing
- OLED display with ghost descriptions and warning status

---

## 💻 Built With
- Arduino IDE
- Team spirit *(wink wink 😉)*

---

## ✨ Authors
- Raksha Kumaresan & Aishi Garimella
