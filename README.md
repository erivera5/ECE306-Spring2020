# ECE 306: Introduction to Embedded Systems

In the interest of preserving the academic integrity of current or future ECE 306 students, the code listings for this project may not be made available for public online viewing. These files are contained in a private repository.

## Overview

The goal of the project was to design a IOT controllable RC car, and write software to control the vehicle over a Wi-Fi connection and autonomously follow a black electrical tape line. Software was written in C, within the IAR Embedded Workbench IDE, to control the input/output peripherals of the TI-MSP430 microcontroller. This software included code and algorithms that implemented a handful of other features, such as traveling in a specified shape, manually configuring the MSP430's UART baud rate, and even a menu system displayed on the LCD screen mounted on the vehicle.

<p align="center">
  <img src="https://i.imgur.com/EDarf19.png" width="519" height="446" />
</p>



## Black Line Detection

The mechanism that detects a black electrical tape line consists of an IR detector/emitter board mounted underneath the chassis, and a C function that manipulates vehicle movement based on the amount of light being picked up by the IR sensors. Therefore, a higher ADC voltage being read by these sensors would indicate that the color black is being detected, which occurs when these sensors are driven directly over black electrical tape. Depending on whether either of these sensors detect an ADC value that strays away from the black line, the vehicle is programmed to correct itself and move back towards the line. 



<p align="center">
  <img src="https://i.imgur.com/t1lcPeH.jpg" width="504" height="378" />
</p>

## Demonstration

The end result which shows this embedded system navigating through an IoT course can be viewed here:

https://www.youtube.com/watch?v=MdTlc8b6d9U&t=4s

