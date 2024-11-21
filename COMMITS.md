# POWER CONSUMPTION MONITORING SYSTEM OVERVIEW
<img width="1103" alt="general-diagram" src="https://github.com/user-attachments/assets/7974267b-00f0-41fb-8ff0-f4c4d21e98f6">

LOAD SPECS:
- V_load: $24[V] \div 48[V]$
- I_load: $-3[A] \div 25[A]$

MONITORING SYSTEM SPECS:
- V_monitor: $9[V] \div 17[V]$
- Normally open relay connected in series with the load
- Hall effect sensor chosen from the _Allegro ACS781xLR_ family

## ASSIGNMENT
I have to develop an overconsumption monitoring system (**monitor**) to perform plauysibility checks of a secondary system (**load**).
The system must ensure that the load power supply is interrupted as soon as a consumption greater than 500W is detected.
I decide to divide the development of the board into the following steps:
- Measure the instantaneus power consumption.
- Compare the instantaneus power consumption with the maximum allowed threshold.
- Interrupt the load's power supply when the power consumption exceeds 500 W using the realy.
- Ensure that the circuit cannot supply the load again, after the suplly has been interrupted once for a overconsumprion, until the whole system is turned off and back-ON.
