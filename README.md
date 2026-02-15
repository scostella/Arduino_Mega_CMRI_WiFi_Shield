# Arduino Mega CMRI WiFi Shield

The **Arduino Mega CMRI WiFi Shield** is a custom expansion board designed to **plug directly into an Arduino Mega 2560**, organizing digital and analog I/O into structured panel‑based connectors while integrating an **ESP8266 ESP‑01** module to provide WiFi connectivity.

When used with the **Arduino CMRI Library**, this shield allows the Arduino Mega to emulate a **CMRI node** supporting both input and output operations over a network connection.

---

## Overview

The Arduino Mega CMRI WiFi Shield serves as the central interface between an Arduino Mega 2560, auxiliary I/O modules, and a WiFi network. The shield groups Arduino pins into standardized connectors for clean wiring and expansion while enabling wireless CMRI communication via an onboard ESP8266 ESP‑01.

This design is intended for modular CMRI systems where distributed I/O and network connectivity are required.

---

## Key Characteristics

- Plugs directly into an **Arduino Mega 2560**
- Groups digital and analog I/O into **16 sets of 4 pins**
- Compatible with the **Arduino CMRI Library**
- Supports both CMRI **input and output** operations
- Integrated **ESP8266 ESP‑01** socket for WiFi connectivity
- Designed to interface with auxiliary modules in this series
- Passive signal routing (no onboard I/O drivers)

---

## Assembled Board

![Arduino Mega CMRI WiFi Shield](./Arduino%20Mega%20CMRI%20WiFi%20Shield.jpg)

The image above shows the rendered Arduino Mega CMRI WiFi Shield PCB as it plugs directly into an Arduino Mega 2560.

---

## Board Layout and Function

### Panel Header Grid

Just offset to the **left of the center of the board** is a **4 × 4 grid of 4‑pin headers**.

- Each 4‑pin header represents a **designated panel** in the Arduino Mega CMRI WiFi sketch
- Together, these headers group Arduino digital and analog pins into **16 panel connections**
- The pin groupings map directly to CMRI node definitions in software

This layout is designed to integrate cleanly with the auxiliary modules developed for this system, including those listed in the **Reference Projects** section. The standardized grouping simplifies wiring and ensures consistent mapping between hardware modules and CMRI configuration.

---

### Power Input

On the **left side of the board** is a **single 3‑pin header** supplying:

- **12 V**
- **5 V**
- **Ground**

This header provides power to both the Arduino Mega and the shield, allowing a single power entry point for the CMRI node.

---

### ESP8266 WiFi Integration

The shield includes a **single 2 × 4 socket** for an **ESP8266 ESP‑01** module.

- The ESP‑01 is installed **after programming**
- Once installed, it enables WiFi connectivity for the CMRI node
- Communication between the Arduino Mega and ESP8266 is handled entirely in firmware

This configuration allows the Arduino Mega to communicate with **JMRI or other network‑based CMRI control systems** over WiFi.

---

### Status Indicators

The board includes **two onboard LEDs**:

- **Power LED**  
  Indicates that the Arduino Mega and shield are powered

- **CMRI Connection LED**  
  Indicates when **JMRI or another network‑based CMRI control system** is connected to the emulated CMRI node

These LEDs provide immediate visual feedback on system power and network status.

---

## Intended Use

This shield is well suited for:

- CMRI‑based model railroad layouts
- Distributed CMRI I/O nodes
- Control panels and indicators
- Integration with auxiliary CMRI modules
- WiFi‑enabled CMRI systems using JMRI or similar software

---

## Limited Liability and Disclaimer

This project is provided as an **open‑source hardware design** and is offered **as‑is**, without warranty of any kind.

By using this design, documentation, or any assembled hardware provided by the author, you agree to the following:

- You assume **all responsibility** for proper electrical design, wiring, installation, and use
- The author makes **no guarantees** regarding suitability for any specific application
- The author shall not be held liable for:
  - Damage to equipment
  - Electrical failures
  - Personal injury
  - Property damage
  - Losses resulting from improper use, installation, or modification

Use of this project or any associated hardware constitutes acceptance of these terms.

---

## Availability and Purchase

Fully **assembled and tested** Arduino Mega CMRI WiFi Shield boards are available.

- **Price:** $35 USD per board  
- **Shipping:** Additional, based on destination  
- **Contact:**  
  📧 scostella@seancostella.com  

Please contact the author for current availability, lead times, and shipping details.

---

## Reference Projects

This project integrates with the Arduino CMRI ecosystem. The following projects provide related hardware, firmware, and configuration support:

- **Arduino Mega CMRI WiFi**  
  Arduino sketch for Mega 2560 to operate as CMRI Node with an ESP8266-ESP01 providing WiFi connectivity.
  https://github.com/scostella/Arduino_Mega_CMRI_WiFi

- **ESP8266 WiFi Setup Utility**  
  ESP sketch to program the ESP8266-ESP01 to work with the Arduino Mega 2560 and connection configuration for your WiFi network.
  https://github.com/scostella/ESP8266WiFiSetup

- **Arduino Mega CMRI WiFi Shield**  
  KiCad design for a shield for the Arduino Mega 2560 facilitating easy integration with the ESP8266-ESP01 and the CMRI modules listed below.
  https://github.com/scostella/Arduino_Mega_CMRI_WiFi_Shield

- **Arduino Accessory Controller**  
  KiCad design for a board to control accessories up to 1 amp.
  https://github.com/scostella/Arduino-Accessory-Controller

- **Arduino IR Sensor Module - 8 Port**  
  KiCad design for a board to use TCRT5000 IR module to sense object presence which can also be used in the Arduino Mega CMRI WiFi module to group sensors to create virtual block detection.
  https://github.com/scostella/Arduino_IR_Sensor_Module_-_8_Port

- **Arduino Tortoise Controller with Feedback - 8 Port**  
  KiCad design for a board to control Circuitron Tortoise Slow Motion Switch machines and provide feedback on switch position either controlled internally by the voltage applied to the tortoise or an external signal.
  https://github.com/scostella/Arduino_Tortoise_Controller_with_Feedback_-_8_Port

- **Arduino Light Controller**  
  KiCad design for a board to control low amperage lighting and other loads (<10ma) using the Arduino's 5V source.
  https://github.com/scostella/Arduino-Light-Controller

These projects may be used together to form a complete CMRI‑controlled lighting and I/O system.

---

## Repository Contents

```text
/
├── 3V3VoltageRegulator.kicad_sch               # 3.3V Regulated Power Module
├── Arduino Mega CMRI WiFi Shield.jpg           # Rendered image of assembled board
├── Arduino Mega CMRI WiFi Shield.kicad_pcb     # KiCad PCB Layout
├── Arduino Mega CMRI WiFi Shield.kicad_prl     # KiCad Project Settings
├── Arduino Mega CMRI WiFi Shield.kicad_pro     # KiCad Project
├── Arduino Mega CMRI WiFi Shield.kicad_sch     # KiCad Schematic
├── ArduinoReset.kicad_sch                      # Arduino Reset module
├── ESP8266ESP01WiFi.kicad_sch                  # ESP8266ESP01WiFi module
├── LogicLevelShifter.kicad_sch                 # 5V-3.3V Logic Level Shift module
└── README.md