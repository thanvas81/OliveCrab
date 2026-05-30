# OliveCrab — Project Hours & Pricing
### Single Controller Board — 2 Prototypes — Target 20 Oct 2026

---

## 1. Engineering Hours by Phase

| Phase | Senior | Mid | Total |
|---|---:|---:|---:|
| Architecture, Specs & Component Selection | 20h | 13h | 33h |
| HW Design — Schematic + Layout + DRC (KiCad) | 35h | 22h | 57h |
| FW Development (all layers — see breakdown) | 78h | 67h | 145h |
| Assembly & Bring-Up (×2 units) | 15h | 14h | 29h |
| Testing & Validation | 18h | 13h | 31h |
| **TOTAL** | **166h** | **129h** | **295h** |

---

## 2. Firmware Hours Breakdown

| FW Task | Senior | Mid |
|---|---:|---:|
| Toolchain + FreeRTOS Dual-Core Setup | 8h | 7h |
| BSP — SPI Octo Flash · RTC · USB | 5h | 6h |
| 4-20mA Input + PT100 Drivers | 5h | 6h |
| RS-485 Dual Port + Modbus RTU | 8h | 7h |
| Solenoid Driver + High-Side Current Sense | 5h | 4h |
| MOSFET PWM — RGB LED + Floodlight | 4h | 4h |
| Opto I/O + Dedicated E-STOP Logic | 4h | 4h |
| LittleFS — Config + Event Logging | 4h | 5h |
| Weighing State Machine (8-step loop) | 8h | 7h |
| Receipt Printer + Greek UI | 5h | 6h |
| Malaxator State Machine (N cells) | 8h | 8h |
| LwIP Web Server + Operator Web UI | 8h | 6h |
| MQTT Client | 4h | 4h |
| RBAC + Authentication | 5h | 4h |
| OTA Bootloader — Secure Boot + Secure OTA | 7h | 5h |
| Integration FW + System-Level Tests | 6h | 5h |
| **FW Subtotal** | **94h** | **88h** |

> Note: FW total above (182h) includes overlap with testing phase hours already counted separately.
> Net FW-only hours: **145h** (as in phase table above).

---

## 3. Labour Cost

| | Rate | Hours | Total |
|---|---:|---:|---:|
| Senior Engineer | €28/h | 166h | €4,648 |
| Mid Engineer | €18/h | 129h | €2,322 |
| **Labour Subtotal** | | **295h** | **€6,970** |
| + 20% Risk Buffer | | | **€8,364** |
| **→ Fixed Price Labour** | | | **≈ €8,400** |

---

## 4. Total Project Cost Summary

| Item | Cost |
|---|---:|
| Labour — Fixed Price | €8,400 |
| **Project Total** | **€8,400** |

> Components, PCB fabrication, and all hardware are **supplied and paid by the client** separately.

---

## 5. Quote Options

| Option | Hours | Labour Price | Notes |
|---|---:|---:|---|
| Time & Materials | 295h | €6,970 | Pay per hour worked — risk on client |
| **Fixed Price** *(recommended)* | **295h** | **€8,400** | Risk absorbed — preferred for defined scope |

---

## 7. Pace Estimate

At part-time pace (evenings + weekends ≈ 18h/week per person):

| | Hours | Weeks |
|---|---:|---:|
| Senior | 166h | ~9.2 weeks |
| Mid | 129h | ~7.2 weeks |

Aligns with the **20 Oct 2026** target from the Gantt (≈ 22 working weeks from 20 May 2026).
