# ESP32-CAM Face Recognition

A project to implement face recognition using the ESP32-CAM module.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
  - [Setting Up the ESP32-CAM](#setting-up-the-esp32-cam)
  - [Install the ESP32 Board Package](#install-the-esp32-board-package)
  - [Install Required Libraries](#install-required-libraries)
  - [Connect the ESP32-CAM to FTDI Programmer](#connect-the-esp32-cam-to-ftdi-programmer)
  - [Upload the Code](#upload-the-code)
- [Usage](#usage)
  - [Power Up the ESP32-CAM](#power-up-the-esp32-cam)
  - [Access the Web Interface](#access-the-web-interface)
  - [Face Recognition](#face-recognition)
- [Configuration](#configuration)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

This project demonstrates how to set up and use the ESP32-CAM module for face recognition. The ESP32-CAM is a low-cost development board with a camera, suitable for IoT applications.

## Features

- Real-time face detection
- Face recognition
- Easy setup and configuration
- Web-based interface for viewing camera feed

## Hardware Requirements

- ESP32-CAM module
- FTDI programmer (for uploading code)
- Breadboard and jumper wires
- Optional: External antenna for better Wi-Fi range

## Software Requirements

- Arduino IDE or PlatformIO
- ESP32 Board Package
- Required libraries: ESP32, ESPAsyncWebServer, AsyncTCP, ArduinoJson

## Installation

### Setting Up the ESP32-CAM

#### Install the ESP32 Board Package

1. Open the Arduino IDE.
2. Go to `File > Preferences`.
3. Add the following URL to the "Additional Board Manager URLs" field:
   ```
   https://dl.espressif.com/dl/package_esp32_index.json
   ```
4. Go to `Tools > Board > Board Manager`.
5. Search for "ESP32" and install the latest version.

#### Install Required Libraries

1. In the Arduino IDE, go to `Sketch > Include Library > Manage Libraries`.
2. Search for and install the following libraries:
   - ESPAsyncWebServer
   - AsyncTCP
   - ArduinoJson

#### Connect the ESP32-CAM to FTDI Programmer

1. Connect the ESP32-CAM's pins to the FTDI Programmer as follows:
   - `U0T` → `TX`
   - `U0R` → `RX`
   - `GND` → `GND`
   - `5V` → `VCC`
2. Connect `GND` to `IO0` to put the ESP32-CAM in flashing mode.

#### Upload the Code

1. Open the provided sketch (e.g., `ESP32_CAM_Face_Recognition.ino`) in the Arduino IDE.
2. Select the correct board and port from `Tools > Board` and `Tools > Port`.
3. Click on the upload button.

## Usage

### Power Up the ESP32-CAM

1. Once the code is uploaded, disconnect `IO0` from `GND`.
2. Press the reset button on the ESP32-CAM.

### Access the Web Interface

1. Open a serial monitor to find the IP address assigned to the ESP32-CAM.
2. Open a web browser and enter the IP address to access the camera feed.

### Face Recognition

- The web interface will show the camera feed with detected faces highlighted.
- Follow the on-screen instructions to register faces.




