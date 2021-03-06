# Title
Integration and Development of energy efficient service oriented IoT applications system using LoRaWAN and Unmanned Area Vehicles.

## IoT Drone
The Internet of Things allows people and things to be connected Anytime, Anyplace, with Anything and Anyone, ideally using Any path/network and Any service. Drones are an emerging form of new IoT devices, flying in the sky with full network connectivity. UAVs or drones work dynamically for such an IoT scenario that collects the data and communicates it to other devices that are out of the communication ranges.  Through edge computing embedded system drone data can be monitored and stored by cloud computing for IoT system. The unique benefits of the drone over IoT include deployment at remote locations, the ability to carry flexible payloads, reprogrammability during tasks, and ability to sense for anything from anywhere.

## Background
In present days one of the most significant challenges of UAV IoT netwrork is "Energy-aware applications for UAV". For having more energy efficient data transmission, LPWAN (Long Power Wide Area Network) has been integrated, which allows long communication with low power and that can prolong the flight time of drone and LPWAN includes LoRaWAN. LoRa devices and wireless radio frequency technology is a long range, low power wireless platform that has become crucial technology factor for IoT networks worldwide. For innovative IoT application, real-time air quality monitoring has been considered.

## Objectives
1. Air quality monitoring sensory data collection system acquisition.
2. Communication between Drone end node and application server through gateway and network server.
3. Sensors equipped drone that measures the air environmental quality data and sends the data of minimum 10 different locations via a LoRaWAN Interface located in the drone to a LoRaWAN Gateway. Manually driven drone takes data twice from each location in different flights.
4. Sensory data will be stored in an appropriate application server.
5. Customize data storage for long term.

## Harware Development for embedded IoT
Components, microcontroller and electrical connections were soldered, assembled and developed for the compatibility of embedded IoT. For this project hardware development of embedded IoT Drone, following components have been used:

### 1. Drone
I built an autonomous full stack IoT Drone from scratch for this project. Drone components and how to build an autonomous drone from grom ground level with full flight controller stack is illustrated in my another project https://github.com/Shakir74/Drone/blob/main/README.md
For edge computing as LoRa end node, the components of building an autonomous drone has been mentioned here: https://github.com/Shakir74/IoT_Drone/blob/main/Drone%20Building
 and after hardware development final IoT Drone view is as following
![alt text](https://github.com/Shakir74/IoT_Drone/blob/main/drone%20view.jpg)

2. **LoRa Microcontroller Board**: I used Seeduino LoRaWAN board for this project which is an Arduino development board with LoRaWan protocol embedded, in the field of IoT. Based on the communication module RHF76-052AM, LoRaWAN microcontroller board is compatible with LoRaWAN Class A/C and supports a variety of communication frequencies of EU863 band from 863 to 870 MHz.

3. **Air Quality Sensor**: For real-time air quality monitoring IoT application, air quality sensor v1.3 was functioned which has been responsive to a wide scope of harmful environmental gases, as carbon monoxide, alcohol, acetone, thinner, formaldehyde and so on.

4. **Raspberry Pi gateway**: For gateway purpose, Raspberry Pi 3 Model B was configured. To recieve drone data there were other modules which were bridged with Raspberry Pi including **Gateway module RHF0M301???868, PRI 2 Bridge RHF4T002, GPS (RHF76-052AM)**.

## Software Development for embedded IoT
1. **Arduino:** Arduino sketch of prototype device for the Arduino software development process to implement my introduced 'air quality monitoring' measurement technique in drone to collect measurements through connected sensors with drone and to transmit the measured data by LoRaWAN at a defined interval from my prototype IoT Drone. 

2. **Linux Gateway**: For wireless data transmitting, Gateway module embedded with Raspberry Pi 3 recieves Drone end node data and with Linux commands gateway module pushes packet forwarder to Network Server. Linux commands run in Raspberry Pi for connecting Gateway and Network Server.

3. **Network Server**: Loriot Network Server recieves the sensory measurements in a single message and decoded device data in JSON. With MQTT Process Handler, Loriot forwards JSNON messages to application server for data customization and in this project AWS cloud computing has been integrated.

4. **AWS Cloud Computing**: For data analysis, visualization, storage and serverless computing three AWS services were implemented in this project inclduing **AWS IoT Core, AWS LAmbda, AWS IoT Analytics**.

My embedded IoT Drone project's overall archietecture can be described in this following figure.  
![alt text](https://github.com/Shakir74/IoT_Drone/blob/main/LoRaWAN%20IoT%20UAV%20architecture%20in%20AWS%20cloud%20computing.jpg)

## Prototype features
The mentioned project objectives have been achieved and the prototype has following features.
1. Ability to reach any height as controlled by user.
2. Long Range using IOT Connectivity.
3. Measures gas parameters for air quality monitoring.
4. Get all data to online portal for analysis.
5. Live Data Monitoring.
6. Long Duration Monitoring.

## Used Cases
This prototype embedded IoT Drone can be used in these following cases.
1. Weather Forecasting.
2. Search and Rescue.
3. Pollution Monitoring.
4. Infrared Thermography.
5. Warehouse.
6. Agriculture.
7. Military Operations.
8. Wild Fire.
9. Others.

I have also worked on another Industrial IoT project where I developed 6axis industrial robot prototype towards Industry 4.0. The project details is here https://github.com/Shakir74/Inudustry-4.0-Robot
