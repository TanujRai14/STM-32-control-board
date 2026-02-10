# STM32 Custom Control PCB

## Overview
This repository contains the **hardware and firmware design** for a full-fledged custom PCB based on an **STM32 microcontroller**, developed using **KiCad** for schematic & PCB design and **STM32CubeIDE** for firmware development.

The board is designed for **motor control and communication-heavy applications**, featuring support for **encoders, PWM motor drivers, I²C, UART, CAN**, and robust power and signal routing with extensive via usage and shared planes.

---

## Features

### Microcontroller
- STM32 series microcontroller (configured via STM32CubeMX)
- Optimized pin mapping for peripherals and future expansion
- SWD interface for programming and debugging

### Motor & Encoder Support
- Multiple **PWM outputs** for motor control
- **Quadrature encoder inputs** using hardware timers
- Proper timer and pin allocation to avoid peripheral conflicts

### Communication Interfaces
- **I²C** for sensors and peripherals
- **UART** for debugging, logging, or external modules
- **CAN bus** for robust industrial communication
- All interfaces routed with correct impedance, grounding, and protection considerations

### Power Management
- Dedicated power domains for logic and motor sections
- Decoupling capacitors placed close to MCU power pins
- Proper grounding strategy using shared ground planes
- Bulk capacitance for motor current transients

### PCB Design
- Designed in **KiCad**
- Multi-layer PCB with:
  - Ground and power planes
  - Extensive via stitching for EMI reduction
  - Proper trace width calculation for high-current paths
- Clear separation between noisy (motor) and sensitive (MCU/communication) sections

---

## Repository Structure
