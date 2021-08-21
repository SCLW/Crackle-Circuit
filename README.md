### Crackle Circuits



| Project Titel:|  Crackle Circuit | 
| :--- | :--- |
|`Status` | Closed | 
|`Start Date` | February 2021| 
|`Project Completion` | March 2021 | 
|`Project Duration`| |
|`License`| CC-BY-4.0, MIT License |



<!--
short description:

Substituting the obsolete LM709 with discrete components, specifically transistors and resistors, ...
-->







In addition to sensors or other control elements like potentiometers, force-sensing resistors, or similar components, touching directly dedicated connection points in a circuit will also affect its behavior. The human body can add various parameters like resistance or capacitance. The conductivity of the human skin introduced into a circuit varies greatly just like the capacitance of the human body. Moisture (sweat), pressure or even the surroundings define the actual electrical values and make it difficult to predict their effect on a circuit. In this context, the crackle box should be mentioned as a remarkable example.



![Crackle_Box](https://github.com/SCLW/Crackle-Circuit/blob/main/img/Crackle_Box.jpg)
*Crackle Box. Photo: Till Kniola*
<br>
<br>

 
The crackle box is a touch-controlled electronic instrument, developed in the 70s by Michel Waisvisz (\*1949 Leiden † 2008 Amsterdam) at STEIM in Amsterdam. Its beginnings date back to the 60s. It's a battery operated small wooden case (14 x 8 x 3 cm), like a cigar box, a visible circuitboard with six distinctive touch points, ~1cm<sup>2</sup> each, and an on/off switch. Underneath the touch surface is a built-in loudspeaker. The vibrating air can pass through a number of holes in the PCB between the touch surface. The instruments produces random noise, clicks and plops or oscillates when touched with fingers. The circuit inside is just an op amp in an inverting configuration, while many circuit points and most pins of the op amp are made available on the outside of the device as conductive touch pads.
 

![LM709_TO-5](https://github.com/SCLW/Crackle-Circuit/blob/main/img/LM709_TO-5.jpg)
*LM709 TO-5 metal can packages*
<br>
<br>



 
The device makes use of the LM709/μA709 op-amp (originally National Semiconductor, then Texas Instruments), one of the earliest monolithic operational amplifiers, created by [Robert Widlar](https://en.wikipedia.org/wiki/Bob_Widlar "Bob Widlar"). Its design concept and performance were already surpassed by its successor LM741. While the ladder is still in production, the LM709 has been discontinued. Compared with modern op-amps, it lacked of an output buffer stage. This means it is not short circuit proof. Furthermore, the LM709 did not have an internal frequency compensation. External components need to be added to limit the op-amps bandwidth to prevent unwanted oscillation. Richard Kaußler made a detailed analysis of the LM709, which can be found [here](https://www.richis-lab.de/Opamp20.htm "LM709"). His [website](https://www.richis-lab.de/ "Richi´s Lab") (in German) is a good resource for in-depth information about the internal structure of various ICs.



![LM709_Die](https://github.com/SCLW/Crackle-Circuit/blob/main/img/LM709_Die.jpg)
*Die of an LM709 op-amp. Photo: Richard Kaußler*
<br>
<br>


 
The image on the left shows the [die](https://en.wikipedia.org/wiki/Die_(integrated_circuit)) of the LM709, embedded in a TO-5 package. On the right is a close up of the die. The die is called the integrated circuit made of silicon. The design of the crackle box focuses on the imperfections of the LM709 and its special features, particularly its external frequency compensation. Michel Waisvisz’s Crackle box is therefore an early example of circuit bending and unconventional use of electronic components. The crackle box had been reissued over the past decades as assembly kits and can still be ordered from STEIM on request.


![Crackle_Box_Circuit](https://github.com/SCLW/Crackle-Circuit/blob/main/img/Crackle_Box_Circuit.jpg)
*LM709 pin out and schematic of Michel Waisvisz’s crackle box*
<br>
<br>


<br>
<br>

As mentioned above, the LM709 is out of production and most modern op amps are internally frequency compensated and achieve a high stability during performance. For the crackle box, the LM709 can't be substituted with other op amps. Which means it also addresses the problem of obsolescence in the field of historical electronic instruments. One approach to circumvent this problem is to look closer into the LM709. The internal schematic can be found in its data-sheet.


![Crackle_Discrete](https://github.com/SCLW/Crackle-Circuit/blob/main/img/Crackle_Discrete.jpg)
*Schematic with LM709 equivalent internal circuit*
<br>
<br>



For most applications, building an integrated circuit with discrete parts leads to a significant degradation of its performance. Because the dedicated parts within an IC are produced precisely to the needs of the circuit. 


![Crackle_Circuit_Prototype](https://github.com/SCLW/Crackle-Circuit/blob/main/img/Crackle_Circuit_Prototype.jpg)
*Breadboard with discrete components substituting the LM709*
<br>
<br>



Since the crackle box doesn't rely on a precise operation but rather on randomness, standard transistors can be used. Both schematics presented here omit the push-pull speaker driver using two complementary pairs of transistors. Substituting the obsolete LM709 with discrete components, specifically transistors and resistors, brings an equivalent crackle circuit into being.

![Crackle_Circuit_Prototype](https://github.com/SCLW/Crackle-Circuit/blob/main/img/Crackle_Board.jpg)
*Crackle board*
<br>
<br>


Download BOM [here](https://github.com/SCLW/Crackle-Circuit/tree/main/BOM "BOM Crackle Circuit")

Download Gerber files [here](https://github.com/SCLW/Crackle-Circuit/tree/main/Gerber "Crackle Circuit Gerber Files")

