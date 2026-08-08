# ESP32 Ultrasonic Radar

An ESP32-based ultrasonic scanning system using an HC-SR04 ultrasonic sensor, an SG90 servo motor, and Processing for real-time radar-style visualization.

## Demo

![Demo](Media/Demo.gif)

## Overview

This project uses an ESP32 to control an HC-SR04 ultrasonic sensor mounted on a servo motor.

The servo scans across an angular range while the HC-SR04 measures the distance of objects. The ESP32 sends the angle and distance data over serial communication to Processing, which displays the measurements as a real-time radar-style visualization.

> Note: This is an ultrasonic scanning system, not an electromagnetic radar. The visualization is presented in a radar-style format.

## Hardware

- ESP32
- HC-SR04 Ultrasonic Sensor
- SG90 Servo Motor
- 2 kΩ Resistor
- 1 kΩ Resistor
- Breadboard
- Jumper Wires

## Wiring

![Wiring Diagram](Diagram/Wiring%20diagram.png)

### Pin Connections

| Component | ESP32 |
|---|---|
| HC-SR04 TRIG | GPIO 5 |
| HC-SR04 ECHO | GPIO 18 |
| Servo Signal | GPIO 23 |
| HC-SR04 VCC | 5V |
| HC-SR04 GND | GND |
| Servo VCC | 5V |
| Servo GND | GND |

The HC-SR04 ECHO signal is connected to GPIO 18 through a resistor voltage divider using 2 kΩ and 1 kΩ resistors.

## Software

- Arduino IDE
- Processing
- ESP32 Arduino Core
- ESP32Servo library

## Project Structure

```text
ESP32-Ultrasonic-Scanner/
├── ESP32/
│   └── Radar.ino
├── Processing/
│   └── Radar.pde
├── Diagram/
│   └── Wiring diagram.png
└── Media/
    └── Demo.gif
