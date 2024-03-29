## Product Requirements
### Objectives
The goal of this project is to plan, design, and develop a mobile weather sensing station with a motorized control response to demonstrate for companies, professionals, and peers. As well as create a GitHub website for personal portfolios to demonstrate application of embedded systems to future prospects.
### Stakeholders
#### Users:
Rural Dwellers - Those in remote locations may not have accurate weather forecasts or data. With this mobile weather station device, they can respond accordingly to accurate data, or have an automatic system to do so.

Miners - Those in harsh industrial environments need to keep workers safe from high pollution, heatstroke, and humidity.
#### Manufacturers:
Manufacturers - They will decide the process of manufacturing and the materials needed to make the design. 
#### Sellers:
Sellers - They will be in charge of how the product is distributed to the users and the marketing behind the product. 

#### Use Cases
_Use Case 1:_ 

34-year-old Steven works as an engineer at WeatherFlow. This year he decided to attend the Innovation Showcase at ASU to review some of the products. Steven is looking for products that sense changes in weather, such as temperature, humidity, and wind speed. He wants these variables to display his phone. He is looking for ideas to bring back to his company.

_Use Case 2:_ 

56-year-old John is a farmer who is used to using various sensors to detect changes in weather. However, he's never known how these sensors work. He’s heard a couple things such as the differences between serial and analog sensors, but he’s never actually known what they meant. He heard that ASUs Innovation Showcase has products that fit this exact description. So, he decided to attend it this year to get a little more insight as to how the equipment he commonly uses works. 
### Converting Use Needs into Specifications
Below are the design aspects which our team derived from benchmarking and  user needs. After compiling and ranking the user needs, inspiration was drawn from categories and simplified into the various design aspects below. The top ranked user needs with the highest frequency would become product requirements.
### Design Aspects
#### 1. Hardware/Product Design
1.1 - The device shall include at least 1 motor/linear actuator with bidirectional control ability using serial-based (I2C or SPI) motor control

1.2 - The device’s size shall be handheld

1.3 - The device’s weight shall be less than 10lbs

1.4 - The materials for the device shall be durable and be able to withstand constant use

1.5 - The device shall allow for high user interaction through the multiple functions

1.6 -  The device shall be designed to prevent damage from valuable/fragile components

1.7 - The device hardware material shall be durable and be able to withstand minor impacts and high levels of interaction (lifecycle of at least one year)

1.8 - The device design shall allow for easy repair

#### 2. Software/Functionality
2.1 - The project ECAD software shall be Cadence

2.2 - The project shall include at least one switching voltage regulator

2.3 - The system logic-level voltage shall be 3.3V

2.4 - The project shall include at At least 2 serial sensors and one serial actuator using SPI or I2C.

2.5 - The project shall include at least one example each of UART, SPI, and I2C.

2.6 - The project shall use the 8 or 16-bit Microchip PIC families & ESP32.

2.7 - The maximum board dimensions shall be 100x100mm.

#### 3. Interactivity & User Experience
3.1 - The device shall work right away without much input from the user.

3.2 - The device shall seamlessly connect to the microcontroller.

3.3 - The device’s user interface shall be intuitive to all users.

3.4 - The device shall include multiple reading points to sense multiple environmental conditions.

#### 4. Customization
4.1 - The device should allow space for integration into the user’s environment.

4.2 - The device should be adaptable to a wide variety of situations.

#### 5. Manufacturing
5.1 - The maximum project budget is $60 per team member.

5.2 - The position of the components shall not change after assembly.

5.3 - The device shall be designed to consist of the least amount of parts possible.

5.4 - The device shall be designed and created to allow for easy maintenance and use accessibility.

#### 6. Safety
6.1 - The device shall have no sharp edges.

6.2 - The device shall have low energy requirements of 3.3 V to prevent risk.

6.3 - Handheld and lightweight to ensure safety.

6.4 - Functionality must be safe to use for one with no technical knowledge. 

6.5 - Any tools used to modify the device must not require a power supply.

### Open Questions
* How can we design a product that is engaging and attracts attendants at the innovation showcase?
  * The product should have a prototype that is visually appealing to attract visitors. 
  
* How would the Wifi element be incorporated into our weather sensing design?
  * Yes, the ESP32 was a critical part of the design and allowed us to receive data over Wifi. 
  
* Can we prioritize safety while still creating a product design that fits all other user needs? 
  * Of course, safety is a high priority and there were not any user needs that prohibited the team from incorporating it into the design.  
  
* Will there be room to expand upon our design once it is finished?
  * Yes, the team wanted to add a weather vane and GPS or tracking system to the boat as well. 
  
* In what ways can we incorporate a motor into a temperature/humidity sensor design?
  * The motor was used to adjust the direction of the sail on the boat. 
  
* How will the device utilize all project requirements while still being unique from other class designs? 
  * The device created was the only boat-related project out of the entire class, making it unique. 

### Assessing Designs
To ensure designs meet the criteria above, they must be assessed. The manner in which they will be assessed is each design aspect category being weighted as follows: 30%: Durability/Hardware, 30%: Usability/User interaction, 25%: Accuracy, and 15%: Convenience/Safety. Then, each sub-aspect will be assessed by each team member on completion on a scale of 1-3, where 1 is failure, 2 is partial success, and 3 is success. Upon averaging each team member's decisions the design assessment will be finished. At this point, design changes and adaptations will be discussed to increase the score of a design if the team chooses. This will ensure the final product meets requirements.
