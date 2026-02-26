## WARNING
**Operating this project without an Amateur Radio Technician or General License is a Felony. For the record, I have my license.**


# PulseEcho

**PulseEcho** is a multi-band HF CW transceiver built on a Raspberry Pi with a touchscreen interface.  
It allows sending and receiving CW messages across shortwave bands, with real-time CW ↔ English translation.

## How to Use

1. Power on the Raspberry Pi and display.  
2. Type your message on the touchscreen or use a CW paddle.  
3. The software converts your input to CW and transmits it.  
4. Incoming CW is automatically decoded and displayed in English.  

## Why I Made This

I wanted a **custom, build-from-scratch HF transceiver** for nationwide CW communications without relying on pre-made kits.  
It also combines **modern touchscreen interaction with classic Morse code** for learning and practical use.

## BOM

| #  | Part                                     | Qty    | Notes / Purpose                         | Amazon Price | LINK                                                                                          |
|----|------------------------------------------|--------|-----------------------------------------|--------------|-----------------------------------------------------------------------------------------------|
| 1  | Raspberry Pi 4 Model B 4 GB              | 1      | Core controller                         | $74.79       | https://www.amazon.com/gp/product/B0CK3L9WD3/ref=ox_sc_act_title_1?smid=AJQ2XOOLXYM4U&psc=1   |
| 2  | 5 V 2 A AC Adapter                       | 1      | Powers Pi                               | $12.99       | https://www.amazon.com/gp/product/B0B7RWFH98/ref=ox_sc_act_title_11?smid=A3HM92FSF4SOPZ&psc=1 |
| 3  | Perfboard PCB                            | 1      | Prototype TX/RX circuits                | $7.99        | https://www.amazon.com/gp/product/B0DBZ1BXFZ/ref=ox_sc_act_title_12?smid=A1Z1ENBD0KSZ4W&psc=1 |
| 4  | Electrolytic Capacitor Kit               | 1      | Decoupling, TX/RX circuits              | $9.99        | https://www.amazon.com/gp/product/B0C1VBXCQM/ref=ox_sc_act_title_13?smid=A3FX7C4A9P37IQ&psc=1 |
| 5  | Resistor Kit                             | 1      | TX/RX circuits                          | $5.99        | https://www.amazon.com/gp/product/B0FSLNYFRN/ref=ox_sc_act_title_14?smid=A70ZGGVCFBL5S&th=1   |
| 6  | Inductor Kit                             | 1      | Filters, oscillators                    | $14.99       | https://www.amazon.com/gp/product/B0FRN87GFP/ref=ox_sc_act_title_15?smid=A2OL5L358EDX9Y&psc=1 |
| 7  | 2N3904 NPN Transistors                   | 1 pack | Signal-level amplification, oscillators | $6.99        | https://www.amazon.com/gp/product/B07T4ZJ76B/ref=ox_sc_act_title_16?smid=A2RFXKS6GNXFWP&psc=1 |
| 8  | 2SC2078 RF Transistors                   | 1 pack | CW TX final amplifier                   | $16.16       | https://www.amazon.com/gp/product/B0F21DVMKN/ref=ox_sc_act_title_10?smid=A3NO4ZE7H92QEA&psc=1 |
| 9  | Crystal Oscillator Kit                   | 1      | Frequency generation                    | $9.90        | https://www.amazon.com/gp/product/B0868VRS13/ref=ox_sc_act_title_17?smid=A2RFXKS6GNXFWP&psc=1 |
| 10 | Micro SD Card 32 GB (3-pack)             | 1      | Pi OS + firmware                        | $23.99       | https://www.amazon.com/gp/product/B07WZS298H/ref=ox_sc_act_title_18?smid=A21AQ316WNX0L1&th=1  |
| 11 | 3.5″ Touchscreen LCD                     | 1      | CW display & input                      | $25.99       | https://www.amazon.com/gp/product/B0FQHWM9NR/ref=ox_sc_act_title_19?smid=ADHH624DX2Q66&psc=1  |
| 12 | Pin Header Kit                           | 1      | Pi/PCB connections                      | $7.49        | https://www.amazon.com/gp/product/B0FCTSSLK9/ref=ox_sc_act_title_5?smid=A2OL5L358EDX9Y&th=1   |
| 13 | Hookup Wire Kit 22 AWG                   | 1      | Internal wiring                         | $15.89       | https://www.amazon.com/gp/product/B0FCTSSLK9/ref=ox_sc_act_title_5?smid=A2OL5L358EDX9Y&th=1   |
| 14 | Jumper Wires Kit                         | 1      | Short connections                       | $9.99        | https://www.amazon.com/gp/product/B0BTT31CBC/ref=ox_sc_act_title_7?smid=A3JRR1O4XCME47&th=1   |
| 15 | HF Antenna Wire 135 ft                   | 1      | TX/RX antenna                           | $39.99       | https://www.amazon.com/gp/product/B014ZT3BA2/ref=ox_sc_act_title_8?smid=A1GYQLJQ8G2Z7J&psc=1  |
| 16 | RG58 Coax 15 ft                          | 1      | Antenna feedline                        | $14.97       | https://www.amazon.com/gp/product/B099JZ176D/ref=ox_sc_act_title_9?smid=A1TE63QTMAEOQO&psc=1  |
| 17 | HF Low-Pass Filter Kit (5–30 MHz, 100 W) | 1      | TX harmonic filtering                   | $47.51       | https://www.amazon.com/gp/product/B0F9WTP2F4/ref=ox_sc_act_title_2?smid=A1WDLOZTHIX5J6&psc=1  |
| 18 | Enclosure 9.1 × 5.9 × 3.4″               | 1      | Mounting Pi, PCB, display               | $18.59       | https://www.amazon.com/gp/product/B0DX79M8B3/ref=ox_sc_act_title_3?smid=A2WO5FNI6I91SW&th=1   |
| 19 | M3 Nylon Standoff & Fasteners            | 1 kit  | Mount Pi, PCB, display inside enclosure | $7.19        | https://www.amazon.com/gp/product/B0G3XCGSNV/ref=ox_sc_act_title_4?smid=A3696X7CHTBXER&psc=1  |

**For a grand total of:** $384.59


## Wiring

See [`wiring/wiring_diagram.pdf`](wiring/wiring_diagram.pdf) for a wiring schematic of the system.

## Images

None yet...
