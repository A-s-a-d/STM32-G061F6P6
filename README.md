# Wiring an STM32 G061F6P6(TSSOP20) using STlink V2 clone
![image](https://github.com/user-attachments/assets/25eb72fc-86b9-43b3-acb7-3cee7a94a600)

I'm going to use the STlink V2 clone to program the microcontroller, any other programmer should work in same way.
The STlink V2 clone has 10 pins : 
|Pin N°|Pin Function|
|:---:|:---:|
|1| RESET|
|2| GND|
|3| SWIM|
|4| +3.3V|
|5| +5V|
|6| SWDIO|
|7| GND|
|8| SWCLK|
|9| +3.3V|
|10| +5V|

The microntroller has the following pin out : 

![image](https://github.com/user-attachments/assets/99e4d364-efce-471a-b7d3-4f58dbd48f90)

Our microntroller has the voltage range from 1.7 V to 3.6 V so we can power it through 3.3V of STlink, but this needs to be used carefully especially if the microcontroller is going to be powered externally.i'm planning to power my microcontroller externally so i'll be only using 3 of the pins of STlink V2 clone. Those pins being : GND, SWDIO, SWCLK. 

## Powering
I'm going to use a USB C breakout board with 5V, D+, D- and GND pin and then regulate that voltage to 3.3V to power the microcontroller. in this configuration we will not be using the programmers 3.3V.
to do this i'm going to be using the LT1117 lineaire adjustable voltage regulator that will provid stable 3.3V.

Here is the diagram of our power circuit : 
![image](https://github.com/user-attachments/assets/fa44504f-524a-4e61-b9a7-b70b364e04fb)
![image](https://github.com/user-attachments/assets/f617318d-1e61-489a-99f6-ee54f0ec2787) 
![image](https://github.com/user-attachments/assets/1c3fdedb-12ef-4def-916e-59a98fa382ea)

As we can see that this circuit allows us to provid up to 900mA of power at 3.3V which should be enough for our STM32 and other low power components like LEDS,...etc.



