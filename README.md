# SkataBase – Hardware

Hardware development repository for **SkataBase**, a skateboard motion tracking and analytics platform.

This repository contains the electronic hardware design files, PCB layouts, component libraries and manufacturing documentation for the SkataBase SkateIMU device.

The device is designed to capture skateboard motion and orientation data using an onboard IMU, enabling trick detection, session tracking and performance analysis.

## Project Overview

SkateIMU is a compact, skateboard-mounted motion tracking device built around an ESP32 microcontroller and a 9-axis inertial measurement unit (IMU).

The hardware is being developed to provide reliable motion data acquisition during skateboarding, with particular emphasis on detecting and analysing individual skateboard tricks.

### Key Features

- 9-axis motion sensing (accelerometer, gyroscope and magnetometer).
- ESP32-C6-based embedded processing.
- SPI communication with the IMU.
- Bluetooth Low Energy (BLE) data transmission.
- Rechargeable LiPo battery operation.
- Compact PCB and enclosure designed for skateboard mounting.
- Modular hardware architecture to support future revisions.

## Hardware Architecture

| Component | Description |
|---|---|
| Microcontroller | Seeed Studio XIAO ESP32-C6 |
| IMU | ICM-20948 9-axis sensor |
| IMU Interface | SPI |
| Wireless Communication | Bluetooth Low Energy |
| Power Source | Rechargeable LiPo battery |
| Battery Capacity | 350 mAh (prototype target) |
| PCB Design | KiCad |

### System Architecture

The XIAO ESP32-C6 handles IMU data acquisition, sensor fusion and BLE communication.

The ICM-20948 provides accelerometer, gyroscope and magnetometer measurements. These measurements are processed by the firmware and transmitted to the Android application for visualisation and analysis.


## Development Status

**Current stage: PCB development and prototyping**

The initial proof of concept has successfully demonstrated:

- Real-time IMU data acquisition.
- SPI communication between the ESP32-C6 and ICM-20948.
- Madgwick sensor fusion for orientation estimation.
- BLE data transmission to the Android application.
- Successful preliminary skateboard testing.
- Reliable operation during skateboard impacts.

The project is now progressing towards a custom PCB and mechanically integrated enclosure.

### Upcoming Development

- [ ] Finalise schematic and component selection.
- [ ] Complete PCB layout and design rule checks.
- [ ] Validate power management and battery monitoring.
- [ ] Prototype momentary-button power control and deep-sleep operation.
- [ ] Manufacture initial PCB revision.
- [ ] Validate SPI sampling and BLE operation on the custom PCB.
- [ ] Design and manufacture 3D-printed enclosure.
- [ ] Perform extended skateboard field testing.

## Design Tools

| Tool | Purpose |
|---|---|
| KiCad | Schematic capture and PCB design |
| PlatformIO | Firmware development |
| Git | Version control |
| 3D CAD | Mechanical enclosure development |

## Manufacturing

Manufacturing files will be maintained alongside the relevant hardware revision.

Expected outputs include:

- Gerber files.
- NC drill files.
- Bill of Materials (BOM).
- Component placement / Pick and Place files.
- Assembly documentation.

Manufacturing outputs should be associated with a specific hardware revision to maintain traceability.

## Hardware Revisions

Hardware revisions will be tracked independently of firmware and Android application versions.

| Revision | Description | Status |
|---|---|---|
| Prototype 0 | Breadboard and breakout-board proof of concept | Completed |
| PCB Rev 1 | Initial custom PCB integrating ESP32-C6 and IMU | In development |

## Related Repositories

SkataBase is organised into separate repositories to keep hardware, firmware and application development independent.

- **Hardware:** This repository – KiCad designs and manufacturing files.
- **Firmware:** ESP32 firmware, sensor fusion and BLE implementation.
- **Android:** Android application for device configuration, data collection and analysis.
- **Project Hub:** Overall project documentation and links to all repositories.