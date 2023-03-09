# ECE 306: Introduction to Embedded Systems

Source code and technical documentation for this project are available upon request.

## Overview

The goal of the project was to design a remote controlled car, write software to control the vehicle over a Wi-Fi connection, and allow for autonomous ability to detect and respond to a black line over a high contrast white surface. Software was written in C within the IAR Embedded Workbench IDE to control the input/output peripherals of the TI-MSP430 microcontroller. This software included code and algorithms that implemented a handful of features, such as a buffer to help process an incoming stream of ASCII characters over UART communication, an interrupt handler responsible for reading ADC voltages detected by an infrared LED paired with infrared detectors, and a switch statement that interpreted user commands to autonomously follow a black line or manually control the vehicle in a chosen direction for a specified duration of time.

Through designing this car, valuable skills were learned such as reading datasheets, using pulse-width modulation, setting up ports for peripherals, setting up clocks, understanding power usage, and the mechanics of controlling the car over the internet (IoT).

<p align="center">
  <img src="https://i.imgur.com/EDarf19.png" width="519" height="446" />
</p>



## Black Line Detection

The mechanism that detects a black electrical tape line consists of an IR detector/emitter board mounted underneath the chassis, and a C function that manipulates vehicle movement based on the amount of light being picked up by the IR sensors. Therefore, a higher ADC voltage being read by these sensors would indicate that the color black is being detected, which occurs when these sensors are driven directly over black electrical tape. Depending on whether either of these sensors detect an ADC value that strays away from the black line, the vehicle is programmed to correct itself and move back towards the line. 



<p align="center">
  <img src="https://i.imgur.com/t1lcPeH.jpg" width="609" height="454" />
</p>


