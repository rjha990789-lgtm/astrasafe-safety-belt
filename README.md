IoT-Based Smart Women’s Safety Belt

Project Overview

The IoT-Based Smart Women’s Safety Belt is a wearable safety system designed to help women request emergency assistance quickly. The system combines wearable sensors, GPS integration, USB serial communication, and a web-based dashboard to provide an expandable personal safety solution.

The prototype uses an ESP32-C3 microcontroller, an SOS push button, an MPU6050 accelerometer and gyroscope sensor, and a NEO-6M GPS module.

Objectives

- To provide a quick emergency alert mechanism using an SOS push button.
- To detect possible falls using an MPU6050 sensor.
- To obtain geographical coordinates through the GPS module when a valid GPS fix is available.
- To transmit emergency events from the ESP32-C3 to a Python-based USB bridge.
- To display emergency alerts and related information on a Flask-based web dashboard.
- To maintain emergency history and manage trusted contacts.

Hardware Components

- ESP32-C3 Microcontroller
- SOS Push Button
- MPU6050 Accelerometer and Gyroscope Sensor
- NEO-6M GPS Module
- USB Connection
- Wearable Belt or Enclosure
- Power Supply

Software and Technologies

- Python: USB serial bridge and communication handling
- Flask: Web application and backend
- HTML, CSS and JavaScript: Web dashboard interface
- USB Serial Communication: Transfers emergency events from the microcontroller to the Python bridge
- GPS Integration: Supports geographical location information when valid GPS data is available

System Working

1. The ESP32-C3 monitors the SOS button and sensor readings.
2. When the SOS button is pressed or a potential fall is detected, an emergency event is generated.
3. The event is transmitted through USB serial communication to a Python-based USB bridge.
4. The Python bridge forwards the event to the Flask web application.
5. The dashboard records and displays the emergency event for the associated user account.
6. When valid GPS coordinates are available and transmitted, the dashboard can display the location on a map.
7. If GPS data is unavailable, a recently saved browser or phone location may be used. Predefined coordinates may also be used in demo mode and are labelled as demonstration data.

Dashboard Features

- User authentication
- Device pairing and connectivity status
- SOS emergency alerts
- Potential fall-event alerts
- GPS location display when valid coordinates are available
- Emergency history
- Trusted-contact management
- Battery information when available

Current Prototype Limitations

- Live location display depends on the availability of valid GPS data or another supported location source.
- Browser or phone location may be used as a fallback if available.
- Demonstration coordinates are not real-time GPS locations.
- Battery information is displayed only when available from the device or application.
- Automatic SMS notifications to trusted contacts are planned for future development and are not currently available in this prototype.

Future Scope

- Integration of a suitable GSM module or SMS service.
- Automatic emergency SMS notifications to trusted contacts.
- Sending emergency location details when valid coordinates are available.
- Improvements in fall-detection accuracy.
- Battery monitoring and power optimization.
- Further testing and improvements to wearable design and reliability.

Safety Note

This project is a prototype intended to demonstrate a personal safety solution. It should not be considered a replacement for emergency services or a guaranteed safety device. Its effectiveness depends on hardware operation, communication availability, location data, and software reliability.

Conclusion

The IoT-Based Smart Women’s Safety Belt demonstrates how wearable sensors, a microcontroller, USB serial communication, GPS integration, and a Flask-based dashboard can work together to support emergency event reporting. The prototype provides a foundation for future improvements, including automated SMS notifications and more reliable location sharing.

Project Status

Prototype under development. Features and integrations may change as development progresses.