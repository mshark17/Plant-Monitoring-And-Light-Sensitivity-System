# G4: Plant Monitoring and Light Sensitivity System

# Table of contents

* [Authors ](https://github.com/shalan/CSCE4301-WiKi/wiki/G4:-Plant-Monitoring-And-Light-Sensitivity-System#authors)
* [Project Proposal ](https://github.com/shalan/CSCE4301-WiKi/wiki/G4:-Plant-Monitoring-And-Light-Sensitivity-System#project-proposal)
* [Initial Design](https://github.com/shalan/CSCE4301-WiKi/wiki/G4:-Plant-Monitoring-And-Light-Sensitivity-System#initial-design)
* [Identified Components](https://github.com/shalan/CSCE4301-WiKi/wiki/G4:-Plant-Monitoring-And-Light-Sensitivity-System#identified-components)
* [Progress](https://github.com/shalan/CSCE4301-WiKi/wiki/G4:-Plant-Monitoring-And-Light-Sensitivity-System#progress)
* [Connections](https://github.com/shalan/CSCE4301-WiKi/wiki/G4:-Plant-Monitoring-And-Light-Sensitivity-System#Connections)
* [Video Demo](https://github.com/shalan/CSCE4301-WiKi/wiki/G4:-Plant-Monitoring-And-Light-Sensitivity-System#Video-demo)
* [Repository](https://github.com/shalan/CSCE4301-WiKi/wiki/G4:-Plant-Monitoring-And-Light-Sensitivity-System#repository)

#  Authors

| Name | Github |
-------|-------------
| Mariam Taha | [MariamMTaha](https://github.com/MariamMTaha) |
| Mostafa Sharkawy | [mshark17](https://github.com/mshark17)|
| Yara Ali |  [YaraYahia17](https://github.com/YaraYahia17) |
| Youssef Abouelenin | [youssefamr56](https://github.com/youssefamr56) |

# Project Proposal
Plant home owners often do not know how to care for their plants, either overwatering or underwatering them, or placing them in unsuitable light conditions. We aim to create a plant monitoring system to achieve optimal conditions for plants to grow. We looked through the previous projects list and felt that we could add new features and improve on the Plant Monitoring system. We hope to expand on previous semesters' work by adding a water sprayer, to solve overwatering and to regulate the plants temperature. This could be implemented on a wider scale to prevent plant death and fire as seen in Europe over the last few years.[^1](https://www.theguardian.com/environment/ng-interactive/2022/jul/26/how-europe-has-been-hit-by-record-fire-damage-and-temperatures) In addition, we will add a Light Sensor to activate an artificial light source for the plants in times of poor lighting, which will prove very beneficial as Sunlight is essential for the plants growth and vitality.[^2](https://royalcitynursery.com/the-importance-of-sun-exposure/)

# Initial Design
![Untitled Workspace](https://github.com/shalan/CSCE4301-WiKi/assets/64726796/5aa8df21-208d-4fa9-87af-0c05ae0f59a5)


# Identified Components

|Component | Link |
----- | ----
STM32 Nucleo-32 Board| [link](https://www.st.com/en/evaluation-tools/nucleo-l432kc.html)
Light Sensitivity Sensor| [link](https://www.ebay.com/itm/294324682385)
Soil Moisture Sensor | [link](https://www.amazon.eg/-/en/Soil-Moisture-Sensor-Water-level/dp/B0BBSJ5T4V/ref=asc_df_B0BBSJ5T4V/?tag=egoshpadde-21&linkCode=df0&hvadid=545257868396&hvpos=&hvnetw=g&hvrand=2362171226009322883&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9112362&hvtargid=pla-1885651757691&psc=1)
DHT22 AM2302| [link](https://ram-e-shop.com/product/sen-dht22/)
Light bulb | [link](https://www.amazon.eg/-/en/4pcs-Philips-Classic-Bulb-Yellow/dp/B09LSHCV3X/ref=asc_df_B09LSHCV3X/?tag=egoshpadde-21&linkCode=df0&hvadid=544932016266&hvpos=&hvnetw=g&hvrand=1049625250042749634&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9112362&hvtargid=pla-1470772828741&psc=1)
4 Channel Relay | [link](https://grobotronics.com/relay-module-4-channel.html?sl=en)
Electric Water Pumps | [link](https://www.amazon.eg/-/en/Micro-Submersible-Motor-Water-Pumps/dp/B0B7B42GD5/ref=asc_df_B0B7B42GD5/?tag=egoshpadde-21&linkCode=df0&hvadid=544990869016&hvpos=&hvnetw=g&hvrand=13876597576089108457&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9112362&hvtargid=pla-1792888376781&psc=1)

# Progress
## First Demo
For our first progress milestone, we integrated all 3 sensors needed; light, soil moisture, and temperature. All sensors appeared to be functioning correctly, apart from the light sensor that only indicated whether light was present or not but not the light intensity.

## Final Demo
We managed to fully integrate and develop the project. Our sensors are operating normally, we used an additional STM32 board as we had 2 sensors that required ADC(extra ADC chips were available, however issues were faced when trying to integrate it with the already existing system), then we used UART to transmit the readings to the main board to display the readings. We then set cases for when the motors and light bulb to operate. We used a 4 channel relay to deal with the power supply issues that we faced. We then engineered a makeshift water supply to water the plant and spray the leaves using straws, a tube, tape and mugs(check the final demo video to gain more understanding). Lastly, we hung a the light bulb to simulate the environment as best we could, given the circumstances. Overall, the system was functioning normally, with the slight issue that over time the main STM32 board stops receiving from the second STM32 and then needs to be reset to continue reading.  

# Video Demo
## First Demo
[First Demo](https://drive.google.com/file/d/1zvWaI1PCF2qrwXPCc2P7tzW1rws4Igpx/view?usp=sharing)

## Final Demo

https://github.com/shalan/CSCE4301-WiKi/assets/86316213/89bd78ab-0059-4834-b6df-f3b696a94424



# Connections
![conn](https://github.com/shalan/CSCE4301-WiKi/assets/86316213/75bd192f-5730-4406-be51-b9a27d3720d5)
![WhatsApp Image 2023-05-29 at 9 47 43 AM (1)](https://github.com/shalan/CSCE4301-WiKi/assets/98087465/2efb87e9-be88-47e0-b53d-401e789cfdb0)



# Repository
[Plant Monitoring And Light Sensitivity System](https://github.com/mshark17/Plant-Monitoring-and-Light-Sensitivity-System)

