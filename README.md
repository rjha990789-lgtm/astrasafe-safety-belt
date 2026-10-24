🛡️ Smart Safety Belt

IoT-Based Women's Safety & Emergency Alert System

📌 About the Project

The Smart Safety Belt is an IoT-based safety solution designed to support women's personal safety through real-time sensor monitoring and emergency event reporting.

The system uses an ESP32-C3 microcontroller, an MPU6050 motion sensor, an SOS push button, and a NEO-6M GPS module. It combines hardware components with a Python USB bridge, Flask backend, and web dashboard to process emergency events and present available location information.

The project aims to provide a convenient way to trigger emergency alerts and support location sharing through an integrated hardware and software system.

⚙️ Hardware Components

Component| Description
ESP32-C3 Development Board| Main controller that processes sensor inputs and communicates with the computer
MPU6050 Sensor| Measures acceleration and angular motion for movement monitoring and fall-event detection
SOS Push Button| Allows the user to manually trigger an emergency event
NEO-6M GPS Module| Receives satellite signals to obtain geographical coordinates
USB Cable| Used for firmware uploading, power, and serial communication
Jumper Wires| Establish electrical connections between components
Breadboard| Optional platform for circuit assembly and testing

🔌 Circuit Connections

1. ESP32-C3 with MPU6050

MPU6050 Pin| ESP32-C3 Pin
VCC| Compatible power supply
GND| GND
SDA| GPIO 20
SCL| GPIO 21

The MPU6050 communicates with the ESP32-C3 using the I²C communication protocol, allowing the controller to read acceleration and gyroscope data.

2. ESP32-C3 with SOS Push Button

Push Button Terminal| ESP32-C3 Pin
Terminal 1| GPIO 4
Terminal 2| GND

The SOS button uses the internal pull-up configuration. When pressed, it generates a manual emergency event that can be transmitted through USB serial communication.

3. ESP32-C3 with NEO-6M GPS

GPS Pin| ESP32-C3 Pin
TX| GPIO 5 (ESP32-C3 RX)
RX| GPIO 6 (ESP32-C3 TX)
GND| GND
VCC| Compatible power supply

The GPS module communicates with the controller through UART serial communication. The ESP32-C3 reads GPS data and processes latitude and longitude when a valid location fix is available.

Verify the pin availability and voltage requirements of your specific ESP32-C3 board and GPS module before connecting.

🔄 Hardware Working Principle

1. System Initialization: The ESP32-C3 initializes the motion sensor, SOS button, and GPS communication interface.
2. Motion Monitoring: The MPU6050 measures acceleration and angular motion continuously.
3. Emergency Activation: Pressing the SOS button triggers a manual emergency event.
4. Fall-Event Detection: The firmware checks motion readings against a configured threshold to identify possible impact events.
5. GPS Location Acquisition: The NEO-6M receives satellite signals and provides geographical coordinates when a valid fix is obtained.
6. USB Serial Transmission: The ESP32-C3 sends emergency events and sensor telemetry to the connected computer.
7. Backend Integration: The Python USB bridge forwards supported information to the Flask backend.
8. Dashboard Display: The web dashboard presents available emergency-event information and location details.

🖥️ Hardware and Software Integration

The hardware works with the project's software components to create an integrated safety-monitoring system.

Component| Role
ESP32-C3 Firmware| Reads sensor inputs and handles emergency events
MPU6050| Provides motion and acceleration data
NEO-6M GPS| Supplies geographical coordinates when available
Python USB Bridge| Reads serial data and forwards supported events
Flask Backend| Processes incoming event information
Web Dashboard| Displays emergency events and available information

🧪 Hardware Testing

The hardware can be tested component by component before complete system integration.

- ESP32-C3: Verify firmware uploading and serial communication.
- SOS Button: Check whether pressing the button generates an SOS event.
- MPU6050: Verify sensor initialization and motion readings.
- GPS Module: Check GPS data reception and valid coordinates outdoors.
- USB Communication: Confirm that serial messages reach the computer.
- System Integration: Verify that supported emergency events reach the backend and appear on the dashboard.

🚀 Key Hardware Features

- Manual SOS emergency activation
- Motion monitoring using an accelerometer and gyroscope
- Firmware-based detection of possible fall events
- GPS-based geographical location acquisition
- USB serial communication with a computer
- Integration with a Python bridge and Flask web backend
- Support for displaying emergency information on a web dashboard

🔮 Future Enhancements

- Compact and comfortable wearable enclosure
- Improved motion-event detection
- Battery-level monitoring
- Enhanced GPS integration
- Integration of a verified SMS notification mechanism
- Further improvements to hardware reliability and system response

🏁 Conclusion

The Smart Safety Belt combines embedded hardware, motion sensing, GPS technology, and web-based software integration to support emergency-event reporting and location sharing. The project demonstrates how IoT technologies can be used to develop a wearable safety solution with a connected dashboard.

---

Project Category: Internet of Things (IoT) · Embedded Systems · Women's Safety

Main Controller: ESP32-C3

Communication: USB Serial · I²C · UART
