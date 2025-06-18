# Smart Automated Wheelchair

**A next-generation IoT-enabled indoor navigation wheelchair leveraging voice commands, mobile control, and precise grid-based movement.**

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Getting Started](#getting-started)
4. [Folder Structure](#folder-structure)
5. [Usage](#usage)
6. [Media](#media)
7. [License & Acknowledgments](#license-acknowledgments)

---

## Project Overview

This prototype combines an ESP32 microcontroller, stepper motors, ultrasonic sensing, and cloud services (Firebase & Blynk) to create an assistive Smart Wheelchair:

* **Voice Control** via Web Speech API: Say "forward", "left", "ward one" etc.
* **Mobile App** built on MIT App Inventor: Button-driven and emergency-stop interface.
* **Ward Modes** (1 & 2): Predefined waypoint arrays for different indoor zones.
* **Real-Time Feedback**: Live position, orientation & alerts displayed on Blynk and logged to Firebase.

## Features

* **Remote Navigation**: Forward/back, turns, stop, reset, return-to-start.
* **Obstacle Avoidance**: Ultrasonic sensor halts on objects ≤10 cm ahead.
* **Grid-Based Precision**: 30×30 virtual grid, odometry & trigonometric updates.
* **Smart Monitoring**: Low-battery, connectivity, sensor fault alerts.
* **Modular Design**: Easily extendable with AI, SLAM, computer vision.

## Getting Started

1. **Clone the repo**

   ```bash
   git clone https://github.com/Navya-Devv/smart-wheelchair.git
   cd smart-wheelchair
   ```
2. **Install Dependencies**

   * Arduino IDE with ESP32 board packages
   * AccelStepper, Firebase Arduino libraries
3. **Configure Firebase**

   * Create a Realtime DB, set rules to allow read/write for authenticated users
   * Copy your `firebaseConfig` into `src/config.h`
4. **Upload Firmware**

   * Open `src/main.ino` in Arduino IDE
   * Select the ESP32 board & COM port
   * Upload
5. **Mobile App**

   * Import `.aia` file into MIT App Inventor
   * Set your Firebase path in `FirebaseDB1` component
6. **Run**

   * Power the wheelchair hardware
   * Open the dashboard on Blynk or use voice/mobile commands

## Folder Structure

```
smart-wheelchair/
├─ src/                   # Arduino firmware
│  ├─ main.ino
│  └─ config.h
├─ web/                   # Website assets
│  └─ index.html          # Project site + code editor
│  └─ code.html           # Full code view page
├─ media/                 # Placeholder for images & videos
│  ├─ wheelchair.jpg
│  └─ demo.mp4
└─ README.md              # This file
```

## Usage

1. **Web Interface**: Open `web/index.html` in a browser to view project details and code editor.
2. **Code Reference**: Click **View Source Code** or navigate to `web/code.html` to paste/view firmware.
3. **Media**: Place your own `media/wheelchair.jpg` and `media/demo.mp4` in the `media/` folder to see live updates.

## Media

* **Image**: `media/wheelchair.jpg` shows the wheelchair in action.
* **Video**: `media/demo.mp4` demonstrates voice and mobile control.

## License & Acknowledgments

* **License**: MIT License
* **Faculty Mentors**: Dr. Srividya M S, Dr. Suma B Rao, Dr. Hemanthkumar B
* **Team Members**: Navya Madiraju (1RV23CS148), Navami Lokesh (1RV23CS147)
* **Based on**: MainEL4thSem.pdf report from RV College CSE Dept.
