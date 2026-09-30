# AgriBot 🌱🤖

A Raspberry Pi based agricultural robot designed to automate selected farm operations including unwanted grass cutting, water spraying based on soil conditions, and automatic seed placement.

## Project Overview

AgriBot combines environmental sensing, motor control, and Bluetooth communication on a Raspberry Pi to support basic agricultural automation.

### Core functions

- 🌱 **Unwanted grass cutting** using DC motors and an L298 motor driver.
- 💧 **Water spraying** when soil moisture indicates that watering is needed.
- 🌾 **Automatic seeding** to place seeds as the robot moves through the field.
- 📡 **Bluetooth communication** for wireless robot control and communication.
- 🌡️ **Environmental monitoring** using temperature and humidity sensors.
- 💧 **Soil monitoring** using a soil moisture sensor.

## Hardware

| Component | Role |
|---|---|
| Raspberry Pi | Main controller |
| Soil moisture sensor | Monitors soil moisture |
| Humidity sensor | Measures ambient humidity |
| Temperature sensor | Measures temperature |
| DC motors | Robot movement / mechanical actuation |
| L298 motor driver | Drives the DC motors |
| Bluetooth | Wireless communication |

## System Architecture

```text
                 +----------------------+
                 |      Raspberry Pi     |
                 |   Main Controller     |
                 +----------+-----------+
                            |
          +-----------------+------------------+
          |                 |                  |
          v                 v                  v
  Soil Moisture       Temperature &       Bluetooth
     Sensor             Humidity           Module
          |              Sensors               |
          +----------------+------------------+
                           |
                           v
                    Decision / Control
                           |
              +------------+------------+
              |                         |
              v                         v
        L298 Motor Driver        Agricultural Actions
              |                  - Grass cutting
              v                  - Water spraying
          DC Motors              - Automatic seeding
```

## Operating Concept

1. The Raspberry Pi reads the soil moisture and environmental sensor data.
2. Soil moisture information is used to determine when watering is required.
3. The motor driver controls the DC motors used by the robot.
4. The robot can perform grass-cutting operations.
5. The irrigation system sprays water when the soil condition requires it.
6. The seeding mechanism supports automatic seed placement.
7. Bluetooth provides wireless communication with the robot.

## Software

The Raspberry Pi is the central controller. The software should be organized around sensor acquisition, decision logic, motor control, agricultural actions, and Bluetooth communication.

Suggested structure:

```text
Agribot/
├── README.md
├── src/
│   ├── sensors/
│   ├── motor_control/
│   ├── bluetooth/
│   └── agribot_controller.py
├── hardware/
├── docs/
├── images/
└── tests/
```

## Safety and Testing

Before operating the robot, test each actuator independently and verify:

- Motor direction and stop control.
- L298 connections and power supply.
- Sensor readings under dry and moist soil conditions.
- Water spraying trigger logic.
- Bluetooth communication range and command handling.
- Seed dispensing mechanism.
- Emergency stop / safe motor shutdown behavior.

> **Implementation note:** This repository currently documents the system architecture and project requirements. Firmware/software implementation should be added from the actual project source rather than being fabricated.

## Skills Demonstrated

**Raspberry Pi · Python · GPIO · Sensors · DC Motor Control · L298 · Bluetooth · Robotics · Agricultural Automation · Embedded Systems**

## Project Goals

The project demonstrates how a Raspberry Pi can integrate sensing, wireless communication, motor control, and automation into a practical agricultural robotics platform.
