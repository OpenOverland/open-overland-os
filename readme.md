# ESP32-based control board

Custom designed control board build around ESP32-S3 module.

![preview](esp32_c-board.png)

### Main features:

- Overcurrent, overvoltage, reverse polarity protection;
- ESP32-S3 as MCU with the in-built Wi-Fi and Bluetooth capabilities;
- Controls 2x LOCKs (Southco R4-EM-9P15-150);
- 4 digital inputs, protected (optical insulation);
- 2 analog inputs, protected (ESD);
- 12V input power indication;
- On-board RFID-module connector;
- Additional CAN-interface with the 120-Ohms termination jumper;
- Internal headers for I2C and UART interfaces;
- Battery voltage measurement circuit
- Transformed 3.3V power indication;
- Automotive-grade power supply (peak voltages resistant);


### Specification:

1. Board dimensions: 120 x 85 mm, 4x M3-mounting holes (3.2mm inner diameter);
2. XT30 header as main Power-input (up to 15 Amps);
3. Blade-fuse holder on the board (in light-green color);
4. 2x 6-pin Molex MicroFit 3.0 headers for a connection with the Locks;
5. JST-type connectors for digital and analog inputs, for CAN, UART and I2C interfaces;
6. Communication with the RFID-module is over SPI (RC522 module considered by default).

-------------

### RC522 vs. PN532

**RC522**

`Pros`

Very inexpensive (about 5$/pcs.).
Excellent for MIFARE Classic applications.
Easy to use.
Low power consumption.

`Cons`

Primarily supports ISO14443A.
No NFC functionality.
*Shorter reading distance.*
Many low-cost modules use poorly tuned antennas, reducing performance.


**PN532**

`Pros`

Full-featured NFC controller.
Supports all three NFC operating modes:
RFID/NFC Reader
Card Emulation
Peer-to-Peer
Compatible with Android smartphones.
Supports a wider variety of RFID/NFC card types.
*Generally offers better sensitivity and longer read range.*
Most breakout boards allow selecting SPI, I²C, or UART via jumpers or switches.

`Cons`

More expensive (about 8$/pcs.).
Slightly more complex to integrate.
*Higher power consumption.*



-------------

### Version history

**v2a**
This version is designed for each door (2x locks only)
