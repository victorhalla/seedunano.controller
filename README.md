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

 ## Shield Block Schema
 The shield will be very simple using only 3 main blocks:
 
 1. DC Power supply from AC
 2. ESP32 Socket
 3. Relay

 ## Software
 Objective is to create an environment composed of 3 important pieces:
 1. **SeedUP Nano Firmare** - capable setup Wifi credentials, search and get data from bluetooth sensors, send data to cloud, switch realy and update firmware over the air (OTA) 
 2. **SeedUP Cloud*** - receive data from SeedUP shield, show reports and send notifications to mobile app
 3. **SeedUP Mobile App*** - setup shield wifi credentials, type of plant and threshoulds

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
 ⋅⋅* Enclosure design
 ⋅⋅* Provide support for other bluetooth sensors
 ⋅⋅* Create a cheapper PCB instead of a shield
 ⋅⋅* Design own bluetooth sensor
