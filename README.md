# 325BCE
Low Buck DIY Euclidean Pattern Generator

Does the world really need another Euclidean Pattern Generator?<br>
Of Course Not!<br>
Will that stop me from making one?<br>
Of Course Not!<br>

This module is an inexpensive DIY Arduino Nano based module. Of course it could easily be built with an ATMEGA 328p or other similar IC, but you would need to add the crystal and associated parts.<br>

Depending on where you source the Nano, it should run less than $12 not counting a panel. <br>

Standard Disclaimer<br>
This is a DIY project, and you assume all responsibility for the use and construction of it.<br>

There are a lot of websites that explain Euclidean patterns, so I will not go into an explanation here.<br>

The module has a clock and reset input, along with a pulse output.<br>
There are three pots that change the number of steps, the number of pulses, and the offset.<br>
There is also a change LED that blinks each time a knob is turned to a new position<br>

There are three CV in jacks. The CV present at these jacks is added to the knobs. Any voltage less than 0 will be treated as zero and anything higher than 5V will be treated as 5V. So if you have the pulses knob at 0 and put 2.5V on the CV in, it is the same as the knob being at about the middle.<br>

There is a 2x5 pin header that lets you set options using jumpers.
By default, the module outputs 10ms pulses. This can be changed with the jumpers or in software.<br>

The steps go from 1 to 16<br>
The pulses go from 0 to 16<br>
The offset has two modes. In the first mode, the offset goes from 0 to the number of steps -1. In the second mode, the offset is either 0 or 1, so it just shifts the pulse by one.<br>

A few design notes:
In keeping with the low budget, this design uses 5.1v Zener diodes to protect the inputs to the microprocessor instead of a more robust solution using an opamp, etc... I have tested the CV inputs with 20vpp for an extended period of time with no issues, but keep this in mind. <br>
