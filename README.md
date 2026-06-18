# Autonomous Medical Dispenser Robot

## Overview

The **Autonomous Medical Dispenser Robot** is a low-cost embedded robotic system designed to automate medicine delivery inside hospital wards. The robot follows a predefined black line track, stops automatically at marked patient stations, opens the medicine compartment assigned to that patient, and then continues to the next station.

The project aims to reduce the workload of nurses while ensuring timely and accurate medicine delivery using simple and affordable hardware components.

---

# Features

## 1. Autonomous Line Following

The robot continuously follows a black line using six IR sensors mounted underneath the chassis. Sensor readings are processed by an Arduino Nano to control the left and right motors for smooth navigation.



## 2. Automatic Station Detection

Each patient's bed location is represented by a special black station marker.

When all six sensors detect black simultaneously, the robot recognizes the station, stops automatically, and prepares to dispense medicine.



## 3. Patient-Specific Medicine Dispensing

The robot contains two medicine compartments controlled by SG90 servo motors.

* At Station 1 → Compartment 1 opens.
* At Station 2 → Compartment 2 opens.

The compartment remains open for 2 seconds before closing automatically.



## 4. Safety Feature

If the robot loses the black line completely, it immediately stops moving instead of wandering randomly.

This prevents collision and ensures safe operation inside hospital wards.



# Hardware Components

| Component                                 | Quantity |
| ----------------------------------------- | -------- |
| Arduino Nano                              | 1        |
| L298N Motor Driver                        | 1        |
| 1100 mAh LiPo Battery                     | 1        |
| XL6009 Adjustable Step-Up Boost Converter | 1        |
| TT Gear Motor                             | 2        |
| Mini SG90 Servo Motor                     | 2        |
| IR Sensor Array (6 Sensors)               | 1        |
| Breadboard                                | 1        |
| Jumper Wires                              | Multiple |
| Wheels                                    | 2        |
| Free Roller Caster                        | 1        |
| PVC Board (3 mm, 2 ft × 2 ft)             | 1        |
| Door Angle Brackets                       | 2        |

---


# Working Principle

1. The robot starts moving after the start switch is pressed.

2. Six IR sensors continuously detect the black line.

3. Arduino Nano processes sensor values and adjusts the left and right motors to stay on the path.

4. When all sensors detect black simultaneously, the robot identifies a station marker.

5. The robot stops immediately.

6. The station counter increases.

7. Depending on the station number:

* Station 1 → Servo 1 opens Compartment 1.
* Station 2 → Servo 2 opens Compartment 2.

8. The compartment remains open for 2 seconds.

9. The compartment closes automatically.

10. The robot resumes movement toward the next station.

11. If no line is detected, the robot stops completely for safety.

---

# Technologies Used

* Arduino Nano
* Embedded C/C++
* Arduino IDE
* IR Sensor Based Line Following
* L298N Motor Driver
* SG90 Servo Motor Control
* Autonomous Navigation

---

# Future Improvements

* Support more patient beds using additional servo channels.
* RFID-based patient identification.
* Bluetooth or WiFi monitoring.
* Mobile application integration.
* Medicine inventory management.
* Voice or buzzer notification when medicine is delivered.
* LCD display showing patient information.

---

# Applications

* Hospital medicine delivery
* Smart healthcare automation
* Elderly care centers
* Nursing assistance
* Indoor autonomous service robots

---


