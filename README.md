# Sensorless BLDC Motor Control System

## Overview
This project demonstrates a sensorless control system for a Brushless DC (BLDC) motor using Arduino. The design leverages back electromotive force (BEMF) detection for commutation, eliminating the need for physical sensors. It includes speed control functionality using hardware buttons and PWM modulation for precise motor control.

## Unique Value Proposition
This controller provides a low-cost, efficient solution for BLDC motor control. By using sensorless technology:
- **Cost is minimized** by removing external sensors.
- **Reliability improves** due to fewer physical components.
- **Energy efficiency** is enhanced through precise commutation.

---

## Features
- **Sensorless Commutation**: Tracks rotor position using BEMF signals.
- **PWM Speed Control**: Dynamic speed adjustments with hardware buttons (`SPEED_UP` and `SPEED_DOWN`).
- **Flexible Configuration**: Adjustable duty cycle limits (`PWM_MIN_DUTY`, `PWM_MAX_DUTY`, `PWM_START_DUTY`).
- **Startup Sequencing**: Smooth motor startup with a gradual duty cycle ramp.

---

## Setup Instructions

### Connections
1. Connect the motor phases to Arduino PWM pins:
   - Phase A: Pin 9
   - Phase B: Pin 10
   - Phase C: Pin 11
2. Attach buttons to analog input pins:
   - Speed Up: A0
   - Speed Down: A1

### Software Setup
1. Update the constants in the code to match your motor's specifications:
   - `PWM_MAX_DUTY` (default: 255)
   - `PWM_MIN_DUTY` (default: 50)
   - `PWM_START_DUTY` (default: 100)
2. Compile and upload the code to your Arduino.

---

## Usage Instructions
1. Power the system and ensure the motor connections are secure.
2. Press `SPEED_UP` to increase motor speed.
3. Press `SPEED_DOWN` to decrease motor speed.
4. Observe stable operation as the BEMF-driven commutation adjusts motor phases.

---

## Competitive Analysis
This solution outperforms traditional systems by:
- Removing dependency on external sensors.
- Reducing overall cost while maintaining performance.
- Offering scalability for various motor types and applications.

