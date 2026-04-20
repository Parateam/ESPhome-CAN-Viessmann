# ESPhome-CAN-Viessmann
Integrates Viessmann Heatpump 252-A direct with CANBUS and ESPHOME to the HOMEASSISTANT dashboard 

May thanks for the inspiration and support. This solutuion is made with the help of:

https://github.com/open3e/open3e

https://github.com/maromme/esphome-vitoair


In 2024, i've installed a Viessman heatpump 252-A. I use HOMEASSISTANT und ESPHOME on an TRUENAS docker. I was not satisfield with the Viessmann Cloud and WLAN connection. I want my data inside my home, and control it via "VPN to home", not via cloud-services. 

This is my first project with CAN, and it works now since March 2026 perfect for me. I can use it fully integrated to HOMEASSISTANT with all possibilities of control and automations.

I dont't use many datapoints (DIDs), but the following sensors and controls are important for me:
<img width="1088" height="670" alt="WP_HA_CAN" src="https://github.com/user-attachments/assets/8425b88d-f16a-4fdb-9f0f-02f2f4c7283b" />

Hardware Setup:


<img width="287" height="297" alt="grafik" src="https://github.com/user-attachments/assets/9395fd14-5325-4eac-94af-1699963bb5a0" />
