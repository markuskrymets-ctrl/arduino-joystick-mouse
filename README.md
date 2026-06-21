# Arduino Joystick Mouse 

A DIY hardware-software project that turns an analog joystick into a fully functional PC mouse using Arduino and Python. The Python script reads raw coordinate data from the Serial port, filters it, and controls the Windows cursor in real-time.

## Features
- Dynamic Speed: Cursor movement speed scales smoothly depending on how far you tilt the stick.
- Hardware Deadzone: Built-in deadzone filtering to prevent any cursor drift or shaking when idle.
- Smart Clicking: Pressing down on the joystick performs a standard Left Click (LMB), while a quick double-click triggers a Right Click (RMB).

## Hardware Wiring
Connect your joystick module to the Arduino board using the following pinout:
- VRx > Analog Pin A0
- VRy > Analog Pin A1
- SW (Button) > Digital Pin 2
- GND > GND
- 5V > 5V

## Getting Started

### 1. Flash the Board
Open the .ino sketch located inside the mouse arduino folder using the Arduino IDE and upload it to your board.

### 2. Install Dependencies
Make sure you have Python installed. Then, install the required libraries via your terminal to enable serial communication and mouse simulation:
`bash
pip install pyserial pyautogui
