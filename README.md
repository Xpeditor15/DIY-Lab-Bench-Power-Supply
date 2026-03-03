# DIY-Lab-Bench-Power-Supply
A small 65W lab bench power supply that I've made using a modified laptop charger!

The .stl files are available inside and the power supply consists of four separate printed parts:
1. Bottom plate with ventilation holes
2. Top plate with fan mounting and ventilation
3. Front plate with mounting for power supply module
4. Back plate with port for AC input charger

The schematic for it will be added in the future!

Other than using a laptop charger, you can also use any other available power supply! 
Such as commercially available power supplies for CCTVs, ATX power supplies for PCs and etc. 

In this case, I'm using a stripped-apart laptop charger module, which outputs a maximum of 65W (19.5V at 3A). 
Instead of the DC barrel charging wire, I've instead directly soldered two 12-gauge wires onto the charger PCB. 

I've also added a 120mm x 120mm 12V fan for cooling purposes to cool the internals since the laptop charger gets considerably warm when using. 
Since the power supply outputs 19.5V, a 12V Micro-560 Pro buck module is used to step down the DC voltage to 12V. 
You can use any other available buck module, though its a good idea to avoid the LM-series buck converters since its relatively ancient and inefficient compared to newer options. 
It also has a slower switching frequency of roughly 150kHz, which may introduce higher output ripples (that may not matter for this application but its still good to keep that in mind for other projects).
Its always good practice to test the power supply you've gotten with an oscilloscope to make sure that it fits your project requirements.

A red pushbutton with built-in LED is used to switch the laptop power supply on and off. 
To power it on, a 5V Micro-560 Pro buck module is used to step-down the 19.5V from the power supply to a steady 5V. 
