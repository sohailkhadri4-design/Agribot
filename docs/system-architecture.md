# AgriBot System Architecture

## Functional Blocks

### Controller
Raspberry Pi coordinates sensing, decision logic, Bluetooth communication, and actuator control.

### Sensors
- Soil moisture sensor
- Temperature sensor
- Humidity sensor

### Actuation
- DC motors
- L298 motor driver
- Grass-cutting mechanism
- Water-spraying mechanism
- Automatic seed-dispensing mechanism

### Communication
Bluetooth is used for wireless communication with the robot.

## Control Flow

```text
Sensors
   |
   v
Raspberry Pi
   |
   +--> Soil condition decision --> Water spraying
   |
   +--> Motor control -----------> Robot movement
   |
   +--> Grass-cutting control ---> Grass cutting
   |
   +--> Seeding control ---------> Automatic seeding
   |
   +--> Bluetooth <--------------> Remote communication
```

The exact GPIO assignments, sensor models, Bluetooth protocol, moisture threshold, motor-control logic, and seeding mechanism should be documented from the actual implementation.
