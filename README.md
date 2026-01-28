# communication protocol
A communication protocol is a set of rules that defines how two or more devices exchange data, including data format, timing, synchronization, addressing and error checking, and in microcontrollers like the PIC16F877A it is mainly implemented using serial protocols such as UART, SPI and I²C; UART is an asynchronous protocol using TX and RX pins with a defined baud rate and a frame structure of start bit, data bits and stop bit and is commonly used for PC, Bluetooth and GSM communication, SPI is a fast synchronous full-duplex protocol using SCK, MOSI, MISO and SS lines and is used for devices like SD cards and high-speed memory, while I²C is a multi master and multi slave  communication protocol using SDA and SCL with device addressing that allows multiple peripherals like RTCs, EEPROMs and sensors to share the same bus.
## UART
UART (Universal Asynchronous Receiver Transmitter) is a serial communication protocol used to exchange data between two devices without a clock signal, where data is transmitted one bit at a time at a fixed baud rate such as 9600 or 115200, and each data frame consists of a start bit, typically 8 data bits, an optional parity bit and one or two stop bits; in the PIC16F877A microcontroller, UART is implemented using the built-in USART module with TX on RC6 and RX on RC7, and it is commonly used to interface with PCs, Bluetooth modules, GSM modems and other serial devices.
### features
* Uses asynchronous serial transmission (no clock line required).
* Requires only two wires: TX (transmit) and RX (receive).
* Data is sent in the form of frames: start bit, data bits, optional parity bit, stop bit.
### applications
* Connecting PIC microcontrollers to a PC or laptop for data logging and debugging.
* Interfacing with Bluetooth modules (HC-05, HC-06) for wireless control projects.
* Communication with GSM modules for SMS and call-based systems.
* Interfacing with GPS receivers to read location data.
* Sending sensor data to serial displays or terminals.
## 12C

I²C (Inter-Integrated Circuit)  is multi master and multi slave  communication protocol that uses SDA (data) and SCL (clock) lines to connect multiple devices on the same bus, where each slave has a unique address and communication is controlled by a master device; it supports half-duplex data transfer, allows many peripherals like RTCs, EEPROMs, LCD modules and sensors to share just two pins of the PIC16F877A, uses pull-up resistors on both lines, and is ideal for short-distance, low-speed communication inside embedded systems.
Address based communication.
### features
 * Uses only two wires: SDA (data) and SCL (clock).
 * Supports multiple slave devices on the same bus using unique addresses.
 * Works in master–slave mode with the master controlling communication.
 * Allows half-duplex data transfer.
### applications
 * Interfacing Real Time Clock (RTC) modules like DS1307 / DS3231.
 * Connecting EEPROM memory devices for data storage.
 * Reading data from sensors such as temperature, pressure and humidity sensors.
 * Driving I²C LCD displays and OLED modules.
## spi
SPI (Serial Peripheral Interface) is a high-speed synchronous serial communication protocol used for short-distance communication between a master and one or more slave devices, where data transfer occurs in full-duplex mode using four main lines: SCK (clock), MOSI (master-out slave-in), MISO (master-in slave-out) and SS (slave select); it offers very fast data rates, simple hardware design, and is widely used in PIC16F877A to interface devices such as SD cards, EEPROM/Flash memory, ADC/DAC converters, displays and sensors.
### features
 * Uses synchronous communication with a dedicated clock line (SCK).
 * Supports full-duplex data transfer (send and receive simultaneously).
 * Very high speed compared to UART and I²C.
 * Requires four main lines: MOSI, MISO, SCK and SS.
 * Works in master–slave architecture.
### applications
 * Interfacing SD cards for data logging systems.
 * Connecting EEPROM and Flash memory chips.
 * Communication with high-speed ADC and DAC converters.
 * Driving TFT, OLED and graphic LCD displays.
## simplex
Simplex communication is a type of data transmission in which information flows in only one direction, meaning one device is always the transmitter and the other is always the receiver, with no possibility of sending data back; common examples include a keyboard sending data to a computer, a TV broadcast station transmitting signals to televisions, and sensor-only output devices sending data to a microcontroller.
example:
* Keyboard
* TV broadcast station
## half duplex
Half-duplex communication is a mode of data transmission in which both devices can send and receive data, but not at the same time; communication happens in one direction at a time, so when one device is transmitting the other must wait, and examples include walkie-talkies, where only one person can speak at a time, and protocols like I²C, where the master and slave share the same data line alternately.
example:
 * Walkie-talkies
 * I²C communication between microcontroller and sensors
## full duplex
Full-duplex communication is a mode of data transmission in which both devices can send and receive data at the same time, allowing continuous two-way communication, and common examples include UART communication between a PC and microcontroller, SPI protocol where MOSI and MISO work simultaneously, and telephone conversations where both people can speak and listen at the same time.
example:
 * Telephone calls
 * UART with separate TX and RX lines
 * SPI communication
 * Ethernet networking


 

