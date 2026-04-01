# OLED Keyboard

A custom mechanical keyboard project featuring per-key OLED displays for dynamic legends, status information, and highly personalized layouts.

## Overview

OLED Keyboard is an experimental custom keyboard platform where each key can display its own icon, label, layer state, shortcut, or custom graphics.  
The goal of this project is to explore the intersection of keyboard design, multi-panel display integration, power distribution, and user interaction.

This project combines:

- custom PCB design
- embedded firmware development
- OLED display integration
- keyboard matrix scanning
- USB communication
- dynamic key rendering

Depending on the firmware mode, each key can show:

- key labels
- shortcuts
- symbols
- macros
- layer indicators
- application-specific legends
- simple animations or status feedback

## Motivation

Traditional keyboards are static: the legend printed on a keycap never changes.  
This project explores a more flexible and expressive approach where each key can adapt visually to:

- active layer
- language layout
- software context
- macro profile
- user preferences

The idea is to make a keyboard that is not only functional, but also programmable, informative, and visually unique.

## Features

- Per-key OLED displays
- Fully custom PCB
- Mechanical key switches
- Dynamic legends and layer indication
- Custom embedded firmware
- USB connectivity
- Macro and shortcut support
- Potential support for animations and contextual UI

## Hardware

Current hardware exploration includes:

- microcontroller: RP2040 / other MCU platform
- multiple OLED displays
- keyboard matrix scanning
- power distribution for many small displays
- SPI display communication
- optional rotary encoder support
- USB interface

> The exact hardware architecture may evolve as the project progresses.

## Architecture

The project is roughly divided into the following blocks:

1. **Keyboard matrix**  
   Detects key presses using rows and columns.

2. **Display subsystem**  
   Drives the OLED displays and refreshes per-key content.

3. **Firmware layer engine**  
   Handles keymaps, layers, macros, and display content generation.

4. **USB HID interface**  
   Sends keyboard events to the host computer.

5. **Power management**  
   Ensures stable power delivery for the MCU, switches, and all displays.

## Challenges

This project involves several interesting engineering challenges:

- driving many OLED displays efficiently
- balancing refresh rate and power consumption
- routing high-density display interconnects on PCB
- scaling SPI/I2C buses
- memory usage for icons/fonts/framebuffers
- firmware architecture for real-time input + rendering
- mechanical integration and assembly

## Project Status

This project is currently in active development.

Current focus areas include:

- hardware architecture exploration
- PCB design
- display driving strategy
- firmware prototyping
- validation of power and signal integrity constraints

## Repository Structure

```text
.
├── docs/            # Design notes, architecture, ideas, references
├── hardware/        # Schematics, PCB files, manufacturing outputs
├── firmware/        # Embedded firmware source code
├── images/          # Photos, renders, screenshots, diagrams
├── tools/           # Helper scripts, generators, utilities
└── README.md
```

## Assembly

![screen](images/oled_keyboard_v2.0_2.jpg)

![screen](images/oled_keyboard_v2.0_1.jpg) 
