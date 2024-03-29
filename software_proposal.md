# Software Implementation
To see MPLAB X IDE Setup refer to [Appendix H](Appendix_H.md).

## System Design and Functionality

### Main Loop

This software implementation satisfies user needs and product requirements by taking input from the sensors and putting appropriate output to the motor, as well as publishing information to the user about the status of the product. As stated previously, when users purchase a product intended to sense various elemental variables, they expect them to not only work well, but also work as intended. Our intention was originally to determine wind speed and wind direction utilizing an anemometer. However, this never came to pass, as we were unable to get the anemometer working properly. The device was also intended to only activate when it was in water. It would do this by detecting the voltage between 2 pins set up on the board. If it was above a certain amount, the system would allow for motor activity, if not, then it will continue to check for moisture. With our final design we intended for it to simply check for wind speed, and remove direction out of design entirely. If wind speed was high enough, the sail would open /rotate, allowing for travel. If the speed dipped below our threshold (i.e. 500) it would close again. 

<figure class="image">  
<p align="center">  
<img src="https://user-images.githubusercontent.com/122958638/235569244-8bc45ac6-4cdd-4256-b22c-aed43a2da448.png" width="35%"><br>
</p>
</figure>

<p align="center">
Figure 10.1: Main Loop
</p>

### Interrupts, Initialization, and Printing to MQTT

Our main loop was the main portion of code in our system. However, as can be seen below, we had other parts to our code such as initializing our system. This part of the diagram simply displays the process of initialization, as well as where any of our functions were defined. Our "Controller Implementation" block shows where we enable our interrupt handler as well as where it was called. Finally, our "Process Message" block shows what is printed to the MQTT server, as well as what order it completes it in.

<figure class="image">  
<p align="center">  
<img src="https://user-images.githubusercontent.com/122958638/235570092-c396d4f1-c7b6-48f4-a750-9d0621e78560.png" width="20%"><br>
</p>
</figure>

<p align="center">
Figure 10.2: Initialization Block
</p>

<figure class="image">  
<p align="center">  
<img src="https://user-images.githubusercontent.com/122958638/235570490-6f32986c-952f-425d-a895-7da8fd62a953.png" width="20%"><br>
</p>
</figure>

<p align="center">
Figure 10.3: Controller Implementation
</p>

<figure class="image">  
<p align="center">  
<img src="https://user-images.githubusercontent.com/122958638/235570772-86a09699-21bd-4e64-a17c-0f4306f3be81.png" width="35%"><br>
</p>
</figure>

<p align="center">
Figure 10.4: Process Message
</p>

## Changes to Software Design
Over of the course of the semester, we ran into many issues. This was usually only associated with hardware. Either it did not work or would immediately fry if we put slightly too much power into it. As a result, we had to change out the hardware, or sometimes even change the design of the board. In turn, we had to alter the code to match whatever new components we had put on. Our 5 biggest changes to our diagram are as follows.

1. In our main loop, we completely removed the "Determine direction of wind" state. Changing the anemometer to use a hall effect sensor had a hand in that.
2. We rearranged the order of events to check the wind speed before checking if the device is in water, as opposed to having moisture be the first state after interrupts.
3. We added another block in to represent system initialization. This was more to show exactly what was being initialized, as well as what functions were being declared.
4. We added a block for enabling interrupts as well as our interrupt service routine.
5. Finally, we actually went more into detail to show what the functions would look like in the code for a better understanding (i.e. "EUSART1_Initialize();")

## Changes for the Future

If we were to create a second version of our software design, it would probably be best to go more into depth about what we are printing to the MQTT server. For example, we wouldn't be printing the characters “jj” or “ii”, but the actual values we are reading from our sensors. Of course this could be changed easily by simply saying what is actually being printed, as the rest of the Process Message block is accurate to how we were printing our values. It would also help to actually determine what the value of 500 means in our main loop, as it does not describe what this number actually means. In terms of wind speed. It would help to add functions to actually be able to calculate the rotational velocity of the anemometer and translate that to wind speed, so it could be called later on without having to type the calculations in the main loop and thus also improving readability. More debugging LEDs would also help to show what parts of our code are not working and when Wifi is slow or disconnected. The team would also work to minimize delays and use timers and interrupts more frequently in our code. As for our protocol design, it is about as simple as it is going to get and keeping it that way ensures that there will not be too many complications around it in the future. 
