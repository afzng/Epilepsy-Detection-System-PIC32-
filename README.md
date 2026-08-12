# Epilepsy Detection System (PIC32)

A C project that is primarily based around using PIC32 to detect rapid motion that would be categorised as an epileptic attack. This code requires the use of a PIC32 microprocessor and an ADXL 335 accelerometer. 
The program implements the use of a loop over the program run period to convert the accelerometer's reading from analog to digital through an endless ADC, whilst simultaneously checking for amount of rapid changes in motion over a small period of time through an interrupt.
If the program detects an attack, then a signal would be sent to a LED to go off. After a period of time, the LED will turn off if the system detects no more peaks in motion.

# Key Features

## 1. Custom System Configurations

* The code comes with pre-defined system configurations to determine the sample rate, peak motion, and amount of peaks before attack detection. This can be adjusted as accelerometer may differ in function and sensitivity. Hence the option to change these values are there and can be adjusted based on your own testing runs.

## 2. Interrupt Function

* In order to save CPU power and program efficiency. The program uses an interrupt function over the function, such that the program is not running a loop constantly which heavily would slow down the computing time. Hence the interrupt helps with the efficiency of the program.
