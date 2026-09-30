# AgriBot 

AgriBot is a Raspberry Pi based agricultural robot I worked on to automate a few common farming tasks. The robot is designed to cut unwanted grass, spray water when the soil needs it, and support automatic seeding.

## What It Does

- Cuts unwanted grass using a motor-driven cutting mechanism.
- Monitors soil moisture and sprays water when required.
- Measures temperature and humidity.
- Supports automatic seed dispensing.
- Uses Bluetooth for wireless communication.
- Uses an L298 motor driver to control the DC motors.

## Hardware

| Component | Purpose |
|---|---|
| Raspberry Pi | Main controller |
| Soil Moisture Sensor | Monitors soil moisture |
| Temperature Sensor | Measures temperature |
| Humidity Sensor | Measures humidity |
| L298 Motor Driver | Controls DC motors |
| DC Motors | Robot movement and mechanical operation |
| Bluetooth | Wireless communication |

## How It Works

The Raspberry Pi handles the sensor readings, motor control, Bluetooth communication, and the logic for the different agricultural functions.

The soil moisture sensor is used to check the condition of the soil. When watering is required, the water spraying system can be activated.

The DC motors are controlled through the L298 motor driver. The robot also has separate mechanisms for grass cutting and seed dispensing.

Bluetooth is used for wireless communication with the robot.

## System Flow

```text
                    +----------------------+
                    |     Raspberry Pi     |
                    |    Main Controller   |
                    +----------+-----------+
                               |
             +-----------------+------------------+
             |                 |                  |
             v                 v                  v
       Soil Moisture     Temperature &       Bluetooth
          Sensor           Humidity
             |               Sensors
             +-----------------+------------------+
                               |
                               v
                         Control Logic
                               |
              +----------------+----------------+
              |                |                |
              v                v                v
         Grass Cutting    Water Spraying   Automatic Seeding
              |
              v
        L298 Motor Driver
              |
              v
          DC Motors
```

## Main Functions

### Grass Cutting

The robot uses a motor-driven cutting mechanism to remove unwanted grass while operating in the field.

### Water Spraying

Soil moisture is monitored continuously during operation. When the soil becomes too dry, the watering mechanism can be activated.

### Automatic Seeding

The robot includes a seed-dispensing mechanism that is intended to place seeds as the robot moves.

### Environmental Monitoring

Temperature and humidity sensors are used to collect environmental readings during operation.

### Bluetooth Communication

Bluetooth provides wireless communication with the Raspberry Pi and allows the robot to be operated without a direct wired connection.

## Software

The Raspberry Pi is responsible for:

- Reading the sensors
- Monitoring soil moisture
- Controlling the DC motors
- Controlling the water spraying system
- Handling the seeding mechanism
- Managing Bluetooth communication
- Coordinating the overall robot operation

## Project Structure

The current repository is organized so that the implementation can be expanded as the project develops.

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
├── tests/
└── .gitignore
```

## Testing

I tested the main hardware sections individually before integrating them into the complete system.

The testing focused on:

- Soil moisture sensor readings
- Temperature and humidity readings
- DC motor operation
- L298 motor control
- Bluetooth communication
- Water spraying
- Grass-cutting mechanism
- Seed dispensing

## Technologies Used

**Raspberry Pi · Python · GPIO · Sensors · DC Motors · L298 · Bluetooth · Robotics · Agricultural Automation**

## What I Learned

Working on AgriBot gave me hands-on experience with Raspberry Pi GPIO, sensor integration, motor drivers, DC motor control, Bluetooth communication, and integrating multiple hardware modules into one robotic system.

The project also involved testing individual components first and then bringing them together into a working agricultural automation system.
