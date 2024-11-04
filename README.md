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

Our microntroller has the voltage range from 1.7 V to 3.6 V so we can power it through 3.3V of STlink, but this needs to be used carefully especially if the microcontroller is going to be powered externally.
