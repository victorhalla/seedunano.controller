# SeedUP Nano Controller
It is a shield that uses the ESP32 module in order to assist in the growth of plants indoors, acting as a lighting controller and a bridge for bluetooth sensors.

Many people want to plant indoors by placing pots next to the windows but most of the time they are not successful. The two main problems are the lack of lighting and water.

It will basicay work for self watering planter allowing to eliminate basic problems on indor grow like: lack of light, water and nutrients.

Using the well know Xiaomi Flora Bluetooth Sensor [https://xiaomi-mi.com/sockets-and-sensors/xiaomi-huahuacaocao-flower-care-smart-monitor/](https://xiaomi-mi.com/sockets-and-sensors/xiaomi-huahuacaocao-flower-care-smart-monitor/) the shield will be able to get important information about the plant environment and send alerts throuth the cloud to a smartphone device.


 ![SeedUp Nano Cloud](/docs/images/seedup_nano_cloud_v1.png "SeedUP Nano Cloud Diagram")

 This shield can easily support more than one plant pot due the factor multiple sensors can be used together and Relay will be cabable to support lights up to 220V/10A.

 ## Why Self Watering
 Although the idea of using pumps to irrigate plants is very good, the simple can often work much better. Usually a self-irrigating pot can withstand up to 10 days without the need for water. It is possible to buy or DIY project that are available in the internet.

 ## Xiaomi Flora Bluetooth Sensor
 This bluetooth sensor is cabable to monitor soil moisture (humidity), temperature, light, soil nutrients and battery level. Multiple sensors can be added to monitor different pot and/or plants.

 [Xiaomi Flora Manual](https://files.miot-global.com/files/plants_monitor/Plants_monitor-EN.pdf)

 ## Shield Block Schema
 The shield will be very simple using only 3 main blocks:
 
 1. DC Power supply from AC
 2. ESP32 Socket
 3. Relay

Project files are available at [EasyEDA](https://oshwlab.com/victor.halla/seedup-nano-controller)

![SeedUp Nano Board Top ](/docs/images/seedup_nano_board_top_v1.png "SeedUp Nano Board Top")

![SeedUp Nano Board Botton ](/docs/images/seedup_nano_board_botton_v1.png "SeedUp Nano Board Botton")

![SeedUp Nano Board 3D ](/docs/images/seedup_nano_board_3d_v1.png "SeedUp Nano Board #d")

 ## BOM

ID | Name | Designator | Footprint | Quantity | Manufacturer Part | Manufacturer | Supplier | Supplier Part
:-- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-:
1 | F1 | F1 | 3.6X10 | 1 | 300mA 250VAC | ReliaPro | LCSC | C12107
2 | F2 | F2 | 3.6X10 | 1 | 72*C Thermal Fuse | ReliaPro | LCSC | C12107
3 | 1000uF | C1 | CP_5X11MM | 1 | RVT0J102M0810 | HONOR | LCSC | C42851
4 | 470uF | C2 | CP_5X11MM | 1 | MV471M6R3F105R | CapXon | LCSC | C65208
5 | HLK-PM01 | U4 | PWRM-TH_HLK-PM01 | 1 | HLK-PM01 | HI-LINK | LCSC | C209903
6 | ESP32-DEVKITC-32D_ESP32-DEVKITC-32D | U1 | MODULE_ESP32-DEVKITC-32D | 1 |  |  |  | 
7 | FC-2012HRK-620D | LED1 | LED0805-RD | 1 | FC-2012HRK-620D | NATIONSTAR | LCSC | C84256
8 | SRA-05VDC-CL | K1 | RELAY-TH_SRA-X-CX | 1 | SRA-05VDC-CL | Ningbo Songle Relay | LCSC | C99666
9 | 1K | R1,R2 | R0603 | 2 | 0603WAD1001T5E | UniOhm | LCSC | C51218
10 | BC848BLT1G | Q1 | SOT-23-3_L2.9-W1.6-P1.90-LS2.8-BR | 1 | BC848BLT1G | ON | LCSC | C163725
11 | 1N4007-C181127 | D1 | SOD-123F_L2.8-W1.8-LS3.7-RD | 1 | 1N4007 | Hottech | LCSC | C181127
12 | KF128-7.5-3P | U2,U3 | CONN-TH_3P-P7.50_KF128-7.5-3P | 2 | KF128-7.5-3P | Cixi Kefa Elec | LCSC | C474955


 ## Software
 Objective is to create an environment composed of 4 important pieces:
 1. **SeedUP Nano Firmare** - capable setup Wifi credentials, search and get data from bluetooth sensors, send data to cloud, switch realy and update firmware over the air (OTA) 
 2. **SeedUP Cloud*** - receive data from SeedUP shield, show reports and send notifications to mobile app
 3. **SeedUP Mobile App*** - setup shield wifi credentials, type of plant and threshoulds
 4. **Home Assistant Integration*** - create a fully working integration with Home Assistant

*These software will have their own repositories here.

## Shield Details

**Shield** | **SeedUP Nano**
:-- | :-:
**Wifi** | 802.11b/g/n 
**Bluetooth** | 4.2 BT/BLE 
**Camera** | -
**Controllers**
-Relays | 1
**Sensors** | 1
-Bluetooth* | Yes 
**Dimensions** |
-Width | TBD
-Length | TBD

## Future Work
- [ ] Enclosure design
- [ ] Provide support for other bluetooth sensors
- [ ] Create a cheapper PCB instead of a shield
- [ ] Design own bluetooth sensor
