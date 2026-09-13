<img width="1280" height="640" alt="git (1)" src="https://github.com/user-attachments/assets/8920b256-2ba8-4988-b824-5351134eb4bd" />



#  🎯


## Basic Details
### Team Name: Saltymeter


### Team Members
- Team Lead: Jils Shaiju - NSS College Of Engineering
- Member 2:  Neha Ann Philip - NSS College Of Engineering

### Project Description
We wanted to build something that would be useless to us, what's more useless than a "thanthoni" robot.

### The Problem (that doesn't exist)
We are solving the problem of the non - existent drama in our lives. 

### The Solution (that nobody asked for)
We create more drama!!!!

## Technical Details
### Technologies/Components Used
For Hardware:
- Components used: Arduino Uno, Motors, Motor drivers, IR Sensors, Ultrasonic sensors, OLED, Buzzer, Castor wheel, Wheel, Battery, Jumper wire, Chassis, Ultrasonic sensor, Switch.
- Specifications:
  Has eyes that move according to movement of bot
  Has a voice that screams if we block him or pick him off the ground
  
- List tools required:
  Screwdriver
  Soldering iron/Desoldering pump
  Double sided tape
  Foam board

### Project Documentation
For Hardware:
# Schematic & Circuit
Circuit(circuit.jpg)
## Connection summary

**Power**
- Arduino 5V → +5V rail → OLED, HC-SR04, and all 4 IR sensors' VCC pins
- Arduino GND → GND rail → shared by every component, including the L298N and battery negative (critical: logic and motor grounds must be common)
- 6–12V battery pack → L298N 12V input (separate high-current supply for the motors, isolated from the Arduino's own 5V regulator)

**OLED display (I2C)**
- SCL → A5, SDA → A4 — the only two data lines needed since I2C is a shared bus protocol

**HC-SR04 ultrasonic**
- TRIG → D12 (Arduino sends the trigger pulse out)
- ECHO → D13 (Arduino reads the return pulse to time it)

**IR sensors (4x)**
- Each has a single digital OUT line → D2 (front-left), D3 (front-right), D4 (rear-left), D11 (rear-right)

**Buzzer**
- SIG → A0 (driven directly by `tone()`, no VCC pin needed for a passive piezo)
- GND → rail

**L298N motor driver**
- ENA/ENB (D5/D6) → PWM speed control for motor A and B
- IN1–IN4 (D7–D10) → direction control (two pins per motor set the H-bridge polarity)
- OUT1/OUT2 → left motor, OUT3/OUT4 → right motor

The overall logic: the Arduino reads the ultrasonic + IR sensors to sense its surroundings, drives the L298N to move the motors, and updates the OLED "face" and buzzer to reflect its current behavior — all sharing one common ground so the signal and motor power domains stay electrically referenced to each other.

# Build Photos

mid_build.jpg
final.jpg


### Project Demo
# Video
https://drive.google.com/file/d/1V81yFddnMm4QLCRS0BBo7YzeTtytqExa/view?usp=drive_link

---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProjects--26-26?link=https%3A%2F%2Ftinkerhub.org%2Fevents%2F1M8ORET9A1%2Fuseless-projects-3.0)



