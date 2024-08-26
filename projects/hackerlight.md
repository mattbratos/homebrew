---
title: Hacker Light
description: Cool led lamp build with WLED, WS2812B and ESP32
date: 2024-08-01
---

# Hacker Light Project Guide

Build your own customizable LED lamp using WLED, WS2812B LEDs, and an ESP32!

## Table of Contents

1. [Introduction](#introduction)
2. [Components](#components)
3. [Hardware Setup](#hardware-setup)
4. [Software Setup](#software-setup)
5. [Assembly](#assembly)
6. [Usage](#usage)
7. [Customization](#customization)
8. [Troubleshooting](#troubleshooting)

## Introduction

The Hacker Lamp is a DIY project that combines the power of an ESP32 microcontroller with the versatility of WS2812B LED strips, all controlled by the feature-rich WLED firmware. This project allows you to create a fully customizable lamp with various lighting effects, controllable via Wi-Fi.

## Components

-   ESP32 development board
-   WS2812B LED strip (length depends on your design)
-   5V power supply (capacity depends on the number of LEDs)
-   Micro-USB cable
-   Lamp shade or enclosure (can be 3D printed or store-bought)
-   Jumper wires
-   Optional: capacitor (1000μF, 6.3V or higher) for power stabilization

## Hardware Setup

1. Connect the WS2812B LED strip to the ESP32:

    - Connect GND on the LED strip to GND on the ESP32
    - Connect 5V on the LED strip to the 5V output of your power supply
    - Connect DIN (Data In) on the LED strip to GPIO 2 on the ESP32

2. If using a capacitor, connect it between 5V and GND close to the start of the LED strip.

3. Connect the ESP32 to your computer using the Micro-USB cable.

## Software Setup

1. Install the Arduino IDE on your computer.

2. Add ESP32 board support to Arduino IDE:

    - Go to File > Preferences
    - Add `https://dl.espressif.com/dl/package_esp32_index.json` to Additional Board Manager URLs
    - Go to Tools > Board > Boards Manager, search for ESP32, and install

3. Install the WLED firmware:

    - Download the latest release from [WLED GitHub](https://github.com/Aircoookie/WLED/releases)
    - In Arduino IDE, go to Sketch > Include Library > Add .ZIP Library and select the downloaded WLED file

4. Configure and upload WLED:
    - Open the WLED sketch in Arduino IDE
    - Set the board to ESP32 Dev Module
    - Select the correct port
    - Upload the sketch to your ESP32

## Assembly

1. Place the ESP32 and power supply inside your chosen enclosure.
2. Attach the WS2812B LED strip to the inside of your lamp shade or enclosure.
3. Ensure all connections are secure and insulated.

## Usage

1. Power on your Hacker Lamp.
2. Connect to the "WLED-AP" Wi-Fi network from your phone or computer.
3. Open a web browser and navigate to `http://4.3.2.1`
4. Follow the setup wizard to connect your lamp to your home Wi-Fi network.
5. Use the WLED interface to control your lamp, change colors, and set up effects.

## Customization

-   Experiment with different LED arrangements in your lamp design.
-   Create custom effects using the WLED user interface.
-   Integrate with home automation systems like Home Assistant or Node-RED.

## Troubleshooting

-   If LEDs don't light up, double-check all connections and ensure proper power supply.
-   If Wi-Fi connection fails, try resetting the ESP32 and reconfiguring.
-   For more help, visit the [WLED Discord](https://discord.gg/KuqP7NE) or [WLED Forum](https://wled.discourse.group/).

Happy hacking!
