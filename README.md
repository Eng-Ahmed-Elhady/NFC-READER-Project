🚀 Project Overview – NFC Reader System (Custom 4-Layer Design)

This project was a full hardware development challenge combining power electronics, RF design, embedded control, and EMI/EMC-aware PCB layout.
A special thanks to Altium Academy and Zach — I learned a lot from their content, and it greatly improved the quality of this design.
Proud to say the system is now fully functional, reliable, and ready for integration.
![1](https://github.com/user-attachments/assets/1af6b0ad-034a-45d4-8f13-23ac8a9d55ef)
![2](https://github.com/user-attachments/assets/98cfadd7-99c7-4991-8966-b6c9079e36d0)
![12](https://github.com/user-attachments/assets/7fe0dd74-a6e9-4c8b-85e1-1e256d57b9d7)![13](https://github.com/user-attachments/assets/0f9ee92e-6569-4a0d-876e-81a25110b3b3)
![14](https://github.com/user-attachments/assets/de3b1a52-fcd1-4c90-a8b1-30adce3c974e)![15](https://github.com/user-attachments/assets/7d801eeb-fbf9-474f-8951-78d1de779c65)
![11](https://github.com/user-attachments/assets/e848c3c6-72e6-4adc-9f00-4efbd1740db9)
![10](https://github.com/user-attachments/assets/2869670b-8374-4603-9088-b6efb0158d58)
![9](https://github.com/user-attachments/assets/3b20c25a-45e0-4ff9-afdb-0b67c5666329)
![8](https://github.com/user-attachments/assets/072c359a-f087-46de-87ac-e4ed91918d50)
![7](https://github.com/user-attachments/assets/a68588df-f7f3-42a9-8aa5-7a9d9f03d86e)
![6](https://github.com/user-attachments/assets/a11de505-5316-47b5-bbf1-7c42dd441f07)
![5](https://github.com/user-attachments/assets/6f877c56-4e86-409d-a762-7ccd8161ffeb)
![4](https://github.com/user-attachments/assets/da287179-07a8-4693-9246-dccf1644e164)
![3](https://github.com/user-attachments/assets/9fd63fa8-13a8-47f3-92c5-b697a2fab1b8)


⚡ 1. Power Architecture

The system receives a 24V input and regulates it down efficiently using:

Buck-Boost Converter

Buck Regulator

LDO

Each stage was selected to ensure stable output voltage, low ripple, and clean power delivery to all RF and MCU circuits.

🧠 2. Processing Unit – ESP32

The ESP32 acts as the main controller:

Communicates with the TRF7970A NFC Reader over SPI

Provides external UART interfaces through a dedicated connector

Integrated RESET and BOOT push buttons for convenient programming and debugging

Signal routing and isolation designed for optimal noise immunity

📡 3. NFC / RFID RF Section

A complete RF schematic was designed, including:

Antenna Matching Network

Tuning Circuit

TRF7970A Main RFID Circuit

The RF path was carefully engineered with controlled impedance and proper return-current handling.

🔧 4. External Control & Outputs

The board includes:

Relay driver for controlling an external motor

Input for an external push button

External status LED outputs

Motor activation only occurs after a valid ID is detected

🖥️ PCB Design – 4-Layer Professional Layout

Designed using Altium Designer, following strict high-performance hardware design rules:

Hierarchical schematic structure for clarity and maintenance

Proper track width and spacing for both power and RF routing

Full controlled-impedance profiles, calculated based on the official JLC04161H-3313 stackup

Crystal guard ring with no routing underneath to eliminate EMI coupling

Close placement of decoupling capacitors on every IC power pin

RF ground isolated from power ground, connected at a single defined point

Ground polygon pours and stitching vias to minimize return-current loops

Minimum 3× trace-width spacing between parallel traces to prevent crosstalk

Full compatibility with JLCPCB manufacturing rules and component sourcing from LCSC

All symbols and footprints were created directly from their datasheets

Proper thermal relief and heat-spreading areas for power regulators

Performed comprehensive ERC (Electrical Rule Check) and DRC (Design Rule Check) to ensure the design is error-free and manufacturing-ready

🎯 Final Result

A fully integrated, high-performance NFC Reader offering:
✔ Stable and reliable operation
✔ Clean and accurate RF behavior
✔ Excellent noise immunity
✔ Manufacturing-ready 4-layer layout
✔ Easy integration into larger embedded systems
