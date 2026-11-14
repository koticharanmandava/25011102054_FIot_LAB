# Foundations of Internet of Things (FIoT) – Laboratory

**Register Number:** 25011102054  
**Repository:** `25011102054_FIot_LAB`  
**Platforms:** 8051 Microcontroller and STM32 NUCLEO-F401RE

This repository contains the practical work completed for the Foundations of Internet of Things laboratory. It brings the 8051 and STM32 experiments together in one place, with source code, project files, circuit diagrams, generated build files (where included), and experiment-level documentation.

## Contents

- [About the Repository](#about-the-repository)
- [Repository Structure](#repository-structure)
- [8051 Experiments](#8051-experiments)
- [STM32 Experiments](#stm32-experiments)
- [Hardware and Software](#hardware-and-software)
- [How to Use the Projects](#how-to-use-the-projects)
- [Experiment Documentation](#experiment-documentation)
- [Notes](#notes)

## About the Repository

The laboratory work is organized by microcontroller platform and CAT (Continuous Assessment Task). Each CAT folder contains the task folders and files available for that assessment. Depending on the experiment, a folder may include:

- Embedded C source files
- Keil project files (`.uvproj` / `.uvprojx`)
- STM32CubeMX configuration files (`.ioc`)
- Circuit diagrams (`.png`)
- Build output or object files
- A README describing the objective, connections, implementation, and observations

The CAT overview below reflects the task folders currently present in this repository. It does not assume that a task exists when its folder or project files are not present.

## Repository Structure

```text
25011102054_FIot_LAB/
├── README.md
├── 8051/
│   ├── CAT2/
│   ├── CAT3/
│   ├── CAT4/
│   ├── CAT5/
│   │   ├── TASK5A/
│   │   ├── TASK5B/
│   │   │   ├── TASK5B.1/
│   │   │   ├── TASK5B.2/
│   │   │   └── TASK5B.3/
│   │   └── TASK5C/
│   ├── CAT6/
│   │   ├── TASK6A/
│   │   └── TASK6B/
│   └── CAT7/
│       ├── TASK7A/
│       ├── TASK7B/
│       └── TASK7C/
└── STM32/
    ├── CAT8/
    │   ├── TASK8A/
    │   ├── TASK8B/
    │   └── TASK8C/
    ├── CAT9/
    │   ├── TASK9A/
    │   └── TASK9B/
    ├── CAT10/
    │   ├── TASK10A/
    │   ├── TASK10B/
    │   └── TASK10C/
    ├── CAT11/
    │   ├── TASK11A/
    │   ├── TASK11B/
    │   └── TASK11C/
    ├── CAT12/
    │   ├── TASK12A/
    │   ├── TASK12B/
    │   └── TASK12C/
    └── CAT13/
        ├── TASK13/
        ├── TASK13A/
        └── TASK13B/
```

> Some task folders contain additional project and driver subdirectories. The tree above is a simplified overview.

## 8051 Experiments

The 8051 work uses the AT89S52 / 8051 architecture and focuses on GPIO, input devices, display interfacing, timers, PWM, motors, and serial communication.

| CAT | Task folders currently present | Experiment area |
|---|---|---|
| CAT2 | `TASK2B` project files | GPIO output control and LED blinking |
| CAT3 | `TASK3A` project files | Push-button input, debouncing, and LED pattern state control |
| CAT4 | `TASK4A` project files | 4×4 matrix keypad, 7-segment display, and LED control |
| CAT5 | [TASK5A](8051/CAT5/TASK5A/), [TASK5B.1](8051/CAT5/TASK5B/TASK5B.1/), [TASK5B.2](8051/CAT5/TASK5B/TASK5B.2/), [TASK5B.3](8051/CAT5/TASK5B/TASK5B.3/), [TASK5C](8051/CAT5/TASK5C/) | Timer 0 interrupts, software PWM, LED fading/breathing, and stepper motor control |
| CAT6 | [TASK6A](8051/CAT6/TASK6A/), [TASK6B](8051/CAT6/TASK6B/) | UART serial transmission and terminal character echo |
| CAT7 | [TASK7A](8051/CAT7/TASK7A/), [TASK7B](8051/CAT7/TASK7B/), [TASK7C](8051/CAT7/TASK7C/) | 16×2 LCD driver, cursor positioning, counter display, and keypad-based menu |

### 8051 highlights

- Digital input/output using 8051 ports
- Push-button handling and software debouncing
- LED patterns and state-based control
- Matrix keypad scanning
- 7-segment display interfacing
- Timer-based delays and interrupt handling
- Software PWM for LED brightness control
- Stepper motor sequence control
- UART communication with a serial terminal
- 16×2 character LCD interfacing

**CAT2–CAT4 folder note:** The current repository tree contains the CAT2 `TASK2B` project files, CAT3 `TASK3A` project files, and CAT4 `TASK4A` project files. Separate CAT2 Task 2A/2C and CAT3/CAT4 additional task folders are not listed as present, so they are not represented as completed tasks here.

## STM32 Experiments

The STM32 work uses the STM32 NUCLEO-F401RE development board (ARM Cortex-M4) and the STM32 HAL library. The experiments progress from GPIO control to serial communication, Wi-Fi connectivity, sensor acquisition, and cloud data transfer.

| CAT | Task folders | Experiment area |
|---|---|---|
| CAT8 | [TASK8A](STM32/CAT8/TASK8A/), [TASK8B](STM32/CAT8/TASK8B/), [TASK8C](STM32/CAT8/TASK8C/) | GPIO follow mode, debounced button toggle, and short/long press classification |
| CAT9 | [TASK9A](STM32/CAT9/TASK9A/), [TASK9B](STM32/CAT9/TASK9B/) | USART terminal character echo and LED command parser |
| CAT10 | [TASK10A](STM32/CAT10/TASK10A/), [TASK10B](STM32/CAT10/TASK10B/), [TASK10C](STM32/CAT10/TASK10C/) | STM32–ESP8266 UART bridge, Wi-Fi modem configuration, and provisioning state machine |
| CAT11 | [TASK11A](STM32/CAT11/TASK11A/), [TASK11B](STM32/CAT11/TASK11B/), [TASK11C](STM32/CAT11/TASK11C/) | Onboard LED, push-button state memory, and press-duration classification |
| CAT12 | [TASK12A](STM32/CAT12/TASK12A/), [TASK12B](STM32/CAT12/TASK12B/), [TASK12C](STM32/CAT12/TASK12C/) | BME280 I²C sensing, JSON payload creation, and HTTP/Node-RED data transfer |
| CAT13 | [TASK13](STM32/CAT13/TASK13/), [TASK13A](STM32/CAT13/TASK13A/), [TASK13B](STM32/CAT13/TASK13B/) | BME280 environmental sensing and ESP8266/MQTT cloud telemetry |

### STM32 highlights

- GPIO input/output configuration using STM32CubeMX and HAL
- Button debouncing and non-blocking timing with `HAL_GetTick()`
- USART communication and terminal command handling
- ESP8266 Wi-Fi modem control using AT commands
- I²C communication with the BME280 environmental sensor
- Temperature, humidity, and pressure data acquisition
- JSON formatting and HTTP POST communication
- MQTT-based telemetry publishing and cloud dashboard integration

## Hardware and Software

### Hardware used across the experiments

- AT89S52 / 8051 microcontroller board
- STM32 NUCLEO-F401RE development board
- LEDs, push buttons, matrix keypad, and 7-segment display
- 16×2 character LCD
- Stepper motor and ULN2003 driver
- USB-to-TTL serial adapter, where required
- ESP8266 / Wemos Wi-Fi module
- BME280 temperature, humidity, and pressure sensor
- ST-LINK debugger/programmer

Use the exact pin connections and components documented in the individual experiment folder before wiring a circuit. Hardware requirements vary by task.

### Software and development tools

- Keil µVision / MDK-ARM
- STM32CubeMX
- STM32 HAL drivers
- Serial terminal software (for example, PuTTY)
- Git and GitHub for version control

## How to Use the Projects

1. Open the repository and select the required platform: `8051` or `STM32`.
2. Open the relevant CAT folder and then the required task folder.
3. Read the task README, if present, for its objective, hardware connections, and implementation details.
4. Open the Keil project file (`.uvproj` or `.uvprojx`) in Keil µVision. For STM32 projects, use the included project configuration and `.ioc` file where available.
5. Check the target device, clock configuration, GPIO assignments, and peripheral settings before building.
6. Build the project and program the appropriate microcontroller using the supported programmer/debugger.
7. Connect the hardware according to the circuit diagram and verify the expected output.

Project settings and device configurations may differ between CATs. Use the configuration stored with the specific task rather than copying settings from another experiment.

## Experiment Documentation

The individual experiment folders contain the task-level documentation and supporting files. Where provided, the documentation covers:

- Experiment objective
- Hardware setup and pin connections
- Circuit diagram
- Program logic / working principle
- Source code and project configuration
- Output verification and inference

This root README serves as the combined index for both microcontroller platforms. Refer to each task folder for the detailed experiment-specific explanation.

## Notes

- The repository is maintained as an academic laboratory record.
- Do not assume that every CAT has the same number of tasks; use the folders actually present in each CAT.
- Generated build files are retained where they are part of the submitted project. They may be regenerated by the relevant IDE.
- Keep personal credentials, Wi-Fi passwords, API keys, and other secrets out of source files and documentation before making the repository public.
- Update this README when new CATs or task folders are added.

---

**Repository:** [25011102054_FIot_LAB](https://github.com/koticharanmandava/25011102054_FIot_LAB)  
**Maintained by:** 25011102054
