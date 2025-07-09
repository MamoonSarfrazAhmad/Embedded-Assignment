# Raspberry Pi Sense HAT Sensor Display 

# Introduction

This project demonstrates how to interface the **Raspberry Pi Sense HAT** with a Raspberry Pi using Python. The primary objectives of the lab are:

- To scroll a custom message on the Sense HAT's 8×8 LED matrix.
- To read environmental data (temperature, humidity, and pressure) and display it live on the LED matrix.

The project highlights the basics of embedded systems programming, including SSH setup, sensor interfacing, and actuator output using Python.


##  Setup Instructions

###  Hardware Required
- Raspberry Pi 3 or 4 (any model with 40-pin GPIO header)
- Raspberry Pi Sense HAT (connected to the GPIO pins)
- MicroSD card with Raspberry Pi OS
- Network access (Wi-Fi or Ethernet)
- Computer with SSH client (e.g., PuTTY on Windows)

### Software Installation on Raspberry Pi

```bash
sudo apt update
sudo apt install sense-hat
```

### Access via SSH (Headless Setup)

If using a headless Raspberry Pi (no monitor):
1. Enable SSH: Place an empty file named `ssh` (no extension) in the `/boot` directory of the SD card.
2. Boot Raspberry Pi and find its IP address via router or network scan.
3. Connect using PuTTY:
    - Host Name: `<your-pi-ip>` (e.g., 192.168.0.112)
    - Port: 22
    - Username: `pi`
    - Password: `raspberry` (default)


##  How to Run the Code

### Scroll Message Script

```bash
python3 sense_led.py


```

![2](https://github.com/user-attachments/assets/8c9d2ca4-8924-4bf6-9ec9-0582f921cf14)


> This displays a scrolling red message: `"Hello, Mamoon!"`

###  Sensor Display Script

```bash
python3 sense_sensor.py

```
![h](https://github.com/user-attachments/assets/678e12ad-6063-46b9-aaf2-c19ae21a7400)


> This script continuously displays temperature, humidity, and pressure on the LED matrix. Press `Ctrl + C` to exit.


##  Files Included

- `sense_led.py`: Displays a red scrolling message.
- `sense_sensor.py`: Shows live environmental sensor values.


##   Results Preview

###  LED Matrix – Text Scroll

![p](https://github.com/user-attachments/assets/82315064-c34c-45bb-9df2-d4ef2809b74f)


###   LED Matrix – Sensor Readings

![l](https://github.com/user-attachments/assets/e1fd06fb-1018-4e1d-9a7d-5e7265901fab)

