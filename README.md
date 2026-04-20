# ESPhome-CAN-Viessmann
Integrates Viessmann Heatpump 252-A direct with CANBUS and ESPHOME to the HOMEASSISTANT dashboard 

Many thanks for the inspiration and support. This solutuion is made with the help of:

- https://github.com/open3e/open3e
- https://github.com/maromme/esphome-vitoair

In 2024, i've installed a Viessman heatpump 252-A. I use HOMEASSISTANT und ESPHOME on a TRUENAS in DOCKER. I was not satisfield with the Viessmann Cloud and WLAN connection. I want my data inside my home, and control it via "VPN to home", not via cloud-services. 

This is my first project with CAN, and it works now since March 2026 perfect for me. I can use it fully integrated to HOMEASSISTANT with all possibilities of control and automations.

I dont't use many datapoints (DIDs), but the following sensors and controls are important for me:
<img width="1088" height="670" alt="WP_HA_CAN" src="https://github.com/user-attachments/assets/8425b88d-f16a-4fdb-9f0f-02f2f4c7283b" />

Hardware Setup:
- ESP32 Board
- TJA1050 CAN driver

<img width="287" height="297" alt="grafik" src="https://github.com/user-attachments/assets/9395fd14-5325-4eac-94af-1699963bb5a0" />

The ESP32 has an integrated CAN controller and therefore doesn’t necessarily need an external controller. So, you only need the TJA1050 driver. 

The TJA1050 is powered with 5V, the input works with 3.3V level, but the RX to ESP32 MUST have 3.3V. So use 2 resistors (4.7kΩ and 10kΩ for an Voltage divider to 3.3V.

I use an Olimex POE ISO board with ethernet and POE power. 

The ESP32 has a own WEB-interface. So it is possible to have it stand-alone without HOMEASSISTANT to show and control!
<img width="924" height="368" alt="WP_WEB_CAN" src="https://github.com/user-attachments/assets/0086313d-84c5-4dcc-9331-f04f6b55698f" />


A little OT: In my situation, the same board has also:
- I2C connection to the LYNX DISTRIBUTOR from VICTRON to monitor the status of the fuses
- RS232 connection the the console port of my PYLONTECH US5000 batterys
All theese sensors are also avalible in HOMEASSISTANT.
