# System Architecture and Hardware Specifications

## 1. Firmware Architecture & MCU Specifications

### Core Specifications
* **MCU:** STM32H7 Dual Core
* **External Storage:** Flash SPI Octo/Quad (8MB)
* **OS:** FreeRTOS
* **Connectivity Services:** Web Server
* **Bootloader:** Bootloader OTA
  * Secure Boot
  * Secure OTA

### Network, Protocols & I/O
* **Protocols:** FTP / SCP, MQTT
* **Network Stack:** LwIP
* **Interfaces:** USB, [BOOT0 header]

### Firmware Setup & Access Control
* **System Operations:** SETUP / Configuration
* **Role-Based Access Control (RBAC):**
  * `ADMIN`: Write / Read Configuration (W R Config)
  * `USER`: Setup / Read
  * `VIEWER`: Read Only
  * `ROOT`: —
* **Security:** Authentication
* **File System:** LittleFS (Config — Logging)
* **Timekeeping:** RTC (Coin Cell + STM32)

---

### Software Stack Layers (SOLID Principles)

```
+---------------------------------------+
|                 APP                   |
+---------------------------------------+
|              MIDDLEWARE               |  <--
+---------------------------------------+
|                 BSP                   |
+---------------------------------------+
|               DRIVERS                 |
+---------------------------------------+
|                  HW                   |
+---------------------------------------+
```

---

## 2. Hardware Requirements (Main Controller)

### Power & Communication Interfaces
* **Main System Controller**
* **Power Supply Unit (PSU):** 24V DC
* **Serial Interface:** 2x RS485 (< 230k baud rate)
* **Temperature Sensing:** 2x PT100 (Range: 0 - 90°C)
* **Backup Power / Safety:** Battery NO — CAPACITOR early warn
* **Analog Inputs:** 4x 4-20mA INPUT
* **Network Interfaces:** 2x Ethernet RJ45

### Peripherals, Driver Outputs & Safety I/O
* **Configurable Analog Output:** 1x Έξοδος (4-20mA ή 0-20V)
* **Actuator Drivers:** 2x Solenoid output (24V, 1A)
  * *Specification:* High Side Current Sense (▲)
* **Digital Inputs:** 4x OPTO INPUTS
* **Power Isolation:** 1x DC-DC ISOLATED (1W)
* **Emergency System:** 1x Dedicated Input Hardware Control (for emergency stop (?))
* **Low-Power Lighting Drivers:** 3x 2A 24V MOSFET (High side PWM for RGB LED)
* **High-Power Lighting Driver:** 1x POWER MOSFET (6-7A, 24V) για LED προβολέα *(for floodlight LED)*
* **Digital Outputs:** 4x OPTO OUTPUT (Open Collector)

---

### System Design Designations
* **Output Protection:** OUTPUTS PROTECTED
* **Project Date:** 20 Okt 26
* **ECAD Software Platform:** KiCad
