# IoT Gas Detection System
Final project for *EEL5739 — IoT Security and Privacy*\
This design is a secure system that monitors gas levels in a research facility, e.g. a lab that incorporates gas-powered equipment. A MQTT broker hosted by Amazon Web Services (AWS) is used to establish a  secure communication channel via SSL certificate encryption. Multiple IoT devices can be deployed for scalable detection capacity. Security challenges and risks are throughly detailed in a risk assessment.

[**TODO: add images and in-depth explanation of system functionality**]

## Overview


## MQTT Broker


## SSL Encryption
Towards the latter end of the course, we were introduced to the AWS IoT Core, which allows users to easily deploy IoT networks that communicate over MQTT, HTTPS, or LoRaWAN. Devices connect to an AWS public endpoint and establish communication with the MQTT broker.\
Prior to deployment, each node is registered with the IoT Core. Each device is given identifying information in the form of a SSL certificate and the Private key to decrypt all messages received from the broker. This information is loaded per device along with the Certificate Authority (CA) Certificate to secure all communications between the broker and device.\
Using SSL encryption prevents snooping and Man-in-the-middle (MITM) attacks from occuring. Traditionally MQTT messages are sent unencrypted, allowing anyone to read the contents of the message sent. This provides malicious actors with ample choices of attack vectors on this attack surface. A MITM attack could easily be implemented by intercepting messages sent and editting the payload to inject malicious code. Alternatively, attackers could drop packets or flood either the devices or broker to inhibit functionality.

## ESP32 Transmitter


## ESP32 Receiver


## Files
The coding portion of the project that I contributed is included in this directory as a zip file. This zip contains the PlatformIO project files along with supplementary code used to deploy a receiver node on an ESP32 device.\
The report and presenstation created for this project are also included, however all identifying information has been removed for privacy reasons.
- [ESP32_Receiver.zip](/iot-gas-detection-system/ESP32_Receiver.zip)
- [Final Report](/iot-gas-detection-system/FinalReport.pdf)
- [Final Presentation](/iot-gas-detection-system/FinalPresentation.pdf)
