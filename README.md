# BandGapReference_Design_using_Sky130
This github repository is all about what does a bandgap reference is and how to design it using a opensource skywater130 PDK

Sub 1v BGR

Need For reference
The integrated circuit should work at all temparature zones. Like desert region or polar region, so we need a referenc evoltage independent of temparature so that we can compare it with another voltage that is dependent of temparature and we can display how much is the actual temparature.

How to generate a current independent of temparature variation

It is a reference circuit - Areference circuit generates a voltage or current of a known fixed absolute value, it is usually associated with interface circuit which usually needs to deal with output world.

One of the few absolute constants on an integrated circuit is the bandgap of silicon.
Many clever circuits have been developed to produce a voltage that is deterministically related to that constant.

Bandgap reference Principle:
*Diagram*
Proportional to absolute temparature (PTAT) circuit is used to cancel the temparature coefficient of the Vbe

PTAT Generator
The difference in Vbe of two BJTs biased with different current densities is proportional to absolute temparature.


* An integrated voltage reference is made by adding the forward bias voltage of pn junction to the difference in the forward voltages of two pn junctions biased at different current densities. Before adding them, these voltages are scaled so that their respective positive and negative temparature coefficient cancel precisely.


What is a bgr?
it is a voltage source with a output voltage of 1.12v and the name comes from the fact thaqt the silicon has a bandgap of 1.12ev and out of silicon substrate we build the trasistors which used in schematic to generate Vref that is equal to 1.12v. 
IF we are succesfull in generating a voltage of 1.2v it is said that the bgr has a TC (Temparature Coefficient = 0)

Why not zener Diode - 1. We want a reference less than 5v, because breakdown voltages of zener is difficult to find to have the required reference voltages.
2. It is simple to implement as we dont have zener diode which means we dont have noise associated with zener diode.


Compatibility of Bandgap Circuits with CMOS Technology
1. The diodes/BJTs required for a bandgap reference may be realized in a CMOS process technology using vertical well structure.
2. High current gain (Beta) is not required from these devices since they are genrally used as diodes.

Where used
1. standard reference ICs
2. data converter ICs like ADC and DAC
