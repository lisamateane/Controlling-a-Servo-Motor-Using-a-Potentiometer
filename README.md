# Controlling a Servo Motor Using a Potentiometer

## Overview
This project demonstrates how to control the angular position of a servo motor in real time using a potentiometer as an analog input on an Arduino Uno. It covers reading an analog voltage with `analogRead()`, converting that value into a usable angle with `map()` and driving a servo motor using the Servo library.

## Repository Contents
- **Lab report** — Full write-up including the aim, apparatus, procedure, circuit diagram, code and conclusion.
- **Servo_Potentionmeter_control1.jpeg / Servo_Potentionmeter_Control2.jpeg** — Photos of the breadboard wiring.
- **Servo_Potentionemter_Control_Code.png** — Screenshot of the Arduino sketch.
- **Demo video** — Recording of the servo responding live to the potentiometer.

## How It Works
The potentiometer's wiper connects to analog pin A1, and its outer legs connect to 5V and GND, so turning it changes the voltage read at A1. That reading (0–1023) is mapped to a servo angle (0–180°) and written to the servo, which is connected to digital pin 9.

## Key Learning Point
`map()` is what bridges analog input and servo output — without remapping the 0–1023 analog range down to 0–180, the value passed to `myservo.write()` would be out of range and the servo wouldn't move correctly.
