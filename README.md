# 🧩 AutiSense – Smart Assistant System for Children with Autism Spectrum Disorder

AutiSense is an assistive system designed to support children with Autism Spectrum Disorder (ASD) by detecting stress in real time and providing calming interventions.

The system combines a wearable stress-monitoring device, an interactive calming screen, and a mobile application used by specialists.

---

# 🧩 System Overview

AutiSense monitors physiological signals and detects emotional stress early, helping caregivers provide timely support during stressful situations or activity transitions.

The system consists of three main subsystems.

---

# 🧩 Wearable Stress Detection Device

A wearable wrist device used by the child to continuously monitor physiological signals.

### Hardware Components

* ESP32-C3 microcontroller
* MAX30102 heart rate sensor
* Galvanic Skin Response (GSR) sensor
* MPU6050 motion sensor
* WS2812 NeoPixel LED ring (visual countdown timer)
* Rechargeable lithium battery

The wearable processes sensor data locally and detects stress using a **baseline-based threshold algorithm**.

### Physiological Signals Used

* Heart Rate (HR)
* Galvanic Skin Response (GSR)
* Motion patterns

Motion analysis is used to distinguish between:

* Physical activity
* Stimming behavior
* Emotional stress

---

# 🧩 Interactive Calming Screen

An external interactive screen placed in the child's environment.

The screen is controlled using a **Raspberry Pi 3 Model B** and displays calming content when stress occurs.

### Supported Calming Modes

* Guided breathing exercises
* Calming videos
* Interactive coloring activity
* Visual relaxation content

A **Bluetooth speaker** provides soothing audio instructions and relaxing sounds.

---

# 🧩 Mobile Application

A mobile application developed using **Flutter** allows specialists to:

* Monitor real-time sensor data
* View detected stress levels
* Control the LED activity timer
* Select calming modes displayed on the interactive screen

The mobile application communicates with the system using **HTTP requests over a local Wi-Fi network**.

---

# 🧩 Stress Alert Notifications

When moderate or high stress is detected, the wearable device automatically sends alerts using a **Telegram Bot notification system**.

This ensures that specialists receive stress alerts even when the mobile application is not actively running.

A cooldown interval is applied between alerts to prevent notification flooding.

---

# 🧩 Stress Detection Method

AutiSense uses a **baseline-based threshold detection approach**.

The system first measures the child’s baseline physiological signals.

Stress is detected when:

* Heart rate increases above baseline thresholds
* GSR values rise relative to baseline
* Motion analysis confirms the change is not caused by physical activity

This method allows reliable real-time stress detection with low computational complexity suitable for wearable systems.

---

# 🧩 Technologies Used

### Hardware

* ESP32-C3
* MAX30102
* GSR sensor
* MPU6050
* WS2812 NeoPixel Ring
* Raspberry Pi 3

### Software

* Arduino (ESP32 firmware)
* Python (Tkinter GUI)
* Flask REST API
* Flutter mobile application
* Telegram Bot API

---

# 🧩 System Communication

Communication between system components is performed through:

* Wi-Fi (ESP32 ↔ Mobile App ↔ Raspberry Pi)
* HTTP APIs
* Bluetooth (Raspberry Pi ↔ Speaker)

---

# 🧩 Full Thesis

The complete graduation project documentation is available here:

📄 **[Read the Full Thesis](AutiSense.pdf)**

---

# 🧩 Authors

Computer Systems Engineering
Palestine Polytechnic University

Contact with us in LinkedIn:
- 👩‍💻 [Batool Shaheen](https://www.linkedin.com/in/batool-shaheen-14a583252/)
- 👩‍💻 [Raghad Darabee](https://www.linkedin.com/in/raghad-darabee-2b73b4220/)

