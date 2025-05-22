# GPS Data Logger with TM1637 and SD Card

This Arduino sketch logs real-time GPS data to a microSD card and displays the speed on a TM1637 4-digit 7-segment display.

## Features
- Logs: Latitude, Longitude, Altitude, Speed, Course
- Displays current speed on TM1637
- Creates daily `.csv` logs on SD card
- Adaptive logging interval based on movement
- Uses: TinyGPS++, TM1637Display, SD, TimeLib

🔌 Hardware Requirements & Wiring
🧰 Components List
Component         	 Quantity	          Description
Arduino Nano /Uno	       1	            Main microcontroller board
NEO-6M GPS Module	       1	            Acquires real-time GPS coordinates
TM1637 4-Digit Display	 1	            Displays speed in km/h
Micro SD Card Module 	   1	            Logs data to .csv file
Micro SD Card (FAT32) 	 1	            At least 1GB, properly formatted
Jumper Wires	           ~              15	For all interconnections
Breadboard (optional)	   1	            Easier prototyping
LED (optional)	         1	            For SD write activity indication

📡 NEO-6M GPS Module ↔ Arduino
GPS Module Pin	Arduino Pin
VCC            	5V
GND	            GND
TX	            D9
RX	            D8

Uses: SoftwareSerial gpsInput(9, 8);

🖥️ TM1637 Display ↔ Arduino
TM1637 Pin	 Arduino Pin
CLK          	A0
DIO	          A1
VCC	          5V
GND          	GND

Uses: TM1637Display display(A0, A1);

💾 SD Card Module ↔ Arduino
SD Module Pin     	Arduino Pin
VCC                  	5V
GND	                  GND
MISO                 	D12
MOSI	                D11
SCK	                  D13
CS (SS)	              D10

Uses: SD.begin(10);

🔴 Optional LED (SD Write Indicator)
LED Pin	Arduino Pin
Anode (+)	D7
Cathode (-)	GND (with 220Ω resistor)
