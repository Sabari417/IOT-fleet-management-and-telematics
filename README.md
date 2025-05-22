# GPS Data Logger with TM1637 and SD Card

This Arduino sketch logs real-time GPS data to a microSD card and displays the speed on a TM1637 4-digit 7-segment display.

## Features
- Logs: Latitude, Longitude, Altitude, Speed, Course
- Displays current speed on TM1637
- Creates daily `.csv` logs on SD card
- Adaptive logging interval based on movement
- Uses: TinyGPS++, TM1637Display, SD, TimeLib

## Hardware Requirements
- Arduino Nano/Uno
- NEO-6M GPS module
- SD card module
- TM1637 4-digit display
- Jumper wires, breadboard

## Output Format (CSV)
