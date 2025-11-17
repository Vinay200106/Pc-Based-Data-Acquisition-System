# PC-Based Data Acquisition System with Fault Alerts
An embedded system project using LPC2148 that monitors temperature via LM35 sensor, timestamps data using RTC, logs it to a PC via UART, and provides real-time fault alerts if temperature exceeds a threshold.
## Overview
This project implements a PC-based data acquisition system using the LPC2148 microcontroller. It continuously monitors temperature using the LM35 sensor, timestamps readings via the on-chip RTC, and sends the data to a PC using UART communication. When the temperature exceeds a defined threshold (e.g., 45°C), the system triggers a fault alert via an LED or buzzer and logs the alert.
### Features
1.📡 Real-time temperature monitoring using LM35
2.⏰ Timestamping using RTC
3.📟 Real-time data display on 16x2 LCD
4.⌨️ Time editing through keypad and external interrupt
5.🖥️ Data logging via UART to Serial Terminal
6.🚨 Fault alert with LED/Buzzer
7.✅ Clear display formatting for normal and alert messages

#### Requirements

#Hardware

1.LPC2148 Microcontroller
2.LM35 Temperature Sensor
3.16x2 LCD Display
4.4x4 Keypad
5.Push Button (for interrupt)
6.LED or Buzzer (for alert)
7.MAX232 (for UART communication)

## Software
1.Embedded C
2.Keil µVision (Compiler)
3.Flash Magic (Flashing Tool)
4.Serial Terminal (e.g., Tera Term / RealTerm / PuTTY)
#####  Workflow
System Initialization: UART, RTC, ADC, LCD, Keypad, and external interrupt setup.
Monitoring: Temperature is read via ADC and timestamped.
Data Logging: Formatted output sent to PC and displayed on LCD.
Fault Detection: If temperature > 45°C, triggers alert and logs as [ALERT].
Time Editing Mode: Activated via external interrupt. User can edit time using the keypad.
