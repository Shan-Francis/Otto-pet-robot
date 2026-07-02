# 🤖 Otto DIY - Obstacle Avoidance Robot

A simple obstacle-avoiding robot built using the **Otto DIY Plus**, an **Arduino-compatible** robot with four servo motors and an ultrasonic distance sensor.

The robot continuously walks forward. When it detects an obstacle within **15 cm**, it reacts by jumping, walking backward, turning left, and then continuing its journey.

---

## Hardware Required

* Otto DIY Plus Robot
* Arduino Nano (or compatible)
* 4 × Servo Motors
* HC-SR04 Ultrasonic Sensor
* Piezo Buzzer
* Battery Pack
* Otto DIY Chassis

---

## Pin Configuration

| Component          | Arduino Pin |
| ------------------ | ----------- |
| Left Leg Servo     | D2          |
| Right Leg Servo    | D3          |
| Left Foot Servo    | D4          |
| Right Foot Servo   | D5          |
| Ultrasonic Trigger | D8          |
| Ultrasonic Echo    | D9          |
| Buzzer             | D13         |
| Assembly Mode      | D7          |

---

## How It Works

1. The robot starts in its home position.
2. It continuously walks forward.
3. The ultrasonic sensor measures the distance ahead.
4. If an object is detected within **15 cm**, the robot:

   * Plays a surprise sound
   * Jumps
   * Plays another sound
   * Walks backward three steps
   * Turns left three times
5. The robot resumes walking forward.

---

## Software Requirements

* Arduino IDE
* Otto DIY Library (Version 9)

Install the required library before uploading the sketch.

---

## Installation

1. Clone this repository.

```bash
git clone https://github.com/yourusername/otto-obstacle-avoidance.git
```

2. Open the project in the Arduino IDE.
3. Install the Otto DIY Library.
4. Select your Arduino board and COM port.
5. Upload the sketch.

---

## Project Structure

```text
Otto-Obstacle-Avoidance/
│
├── Otto_avoid.ino
├── README.md
└── Images/
    ├── robot.jpg
    └── circuit_diagram.png
```

---

## Demo Behavior

```text
Start
   │
   ▼
Walk Forward
   │
   ▼
Measure Distance
   │
   ├── Distance ≥ 15 cm
   │      │
   │      ▼
   │  Continue Walking
   │
   └── Distance < 15 cm
          │
          ▼
      Play Sound
          │
          ▼
         Jump
          │
          ▼
   Walk Backward ×3
          │
          ▼
      Turn Left ×3
          │
          ▼
    Continue Walking
```

---

## Future Improvements

* Right/Left direction selection based on available space
* OLED display for distance information
* Bluetooth remote control
* Wi-Fi control using ESP8266/ESP32
* Line-following mode
* Voice command support
* Mobile app integration

---

## License

This project is open-source and follows the licensing terms of the Otto DIY project (GPL v2).

Please retain the original copyright notice when redistributing or modifying the source code.
