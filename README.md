🚀 Project Overview – NFC Reader System (Custom 4-Layer Design)

This project was a full hardware development challenge combining power electronics, RF design, embedded control, and EMI/EMC-aware PCB layout.
A special thanks to Altium Academy and Zach — I learned a lot from their content, and it greatly improved the quality of this design.
Proud to say the system is now fully functional, reliable, and ready for integration.
![1](https://github.com/user-attachments/assets/ef365b71-7e87-4151-ad20-b4324946f2ff)
![7](https://github.com/user-attachments/assets/56e7d4a9-5d39-4d75-8043-9c97bb8ff87b)
![2](https://github.com/user-attachments/assets/d1a28052-b670-440f-9f8b-fb3f1ee51532)
[1.bmp](https://github.com/user-attachments/files/23566632/1.bmp)
![15](https://github.com/user-attachments/assets/a17ccc2d-ba52-469a-8457-b824774fdbae)
![14](https://github.com/user-attachments/assets/a44fdc80-2d4a-4524-86c8-ae7f22750bdc)
![13](https://github.com/user-attachments/assets/6ac7f47d-77b0-4ab2-ae15-2d82e8ee7e19)
![12](https://github.com/user-attachments/assets/7c49cac9-0fce-461b-8166-3bf1bcbb442b)
[11.bmp](https://github.com/user-attachments/files/23566630/11.bmp)
![10](https://github.com/user-attachments/assets/7c79b822-1406-4e13-920b-8eef21e1991c)
![9](https://github.com/user-attachments/assets/b3365e32-65c8-4621-b977-2ca1d16c7cfd)
![8](https://github.com/user-attachments/assets/f2631eb7-3fea-4a2f-b0bc-2f21b0c911ee)
[7.bmp](https://github.com/user-attachments/files/23566628/7.bmp)
![6](https://github.com/user-attachments/assets/8ea6f610-5be9-4f05-949c-e885ac7f413c)
![5](https://github.com/user-attachments/assets/69100c4e-6935-4a01-a53e-7f0cf486e5dd)
![4](https://github.com/user-attachments/assets/fe77fb29-622c-488f-a477-a103e4a139f7)
![3](https://github.com/user-attachments/assets/adb94978-369f-4f26-81ec-eedc36cc3209)


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
