# DIY-Lab-Bench-Power-Supply
A small 65W lab bench power supply that I've made using a modified laptop charger!

The .stl files are available inside and the power supply consists of four separate printed parts:
1. Bottom plate with ventilation holes
2. Top plate with fan mounting and ventilation
3. Front plate with mounting for power supply module
4. Back plate with port for AC input charger
5. Standoff feet for ventilation


Other than using a laptop charger, you can also use any other available power supply! 
Such as commercially available power supplies for CCTVs, ATX power supplies for PCs and etc. 

In this case, I'm using a stripped-apart laptop charger module, which outputs a maximum of 65W (19.5V at 3A). 
Instead of the DC barrel charging wire, I've directly soldered two 12-gauge wires onto the charger PCB. 

I've also added a 120mm x 120mm 12V fan for cooling purposes to cool the internals since the laptop charger gets considerably warm when in use. 
Since the power supply outputs 19.5V, a 12V Micro-560 Pro buck module is used to step down the DC voltage to 12V to power the cooling fan.
You can use any other available buck module, though its a good idea to avoid the LM-series buck converters since its relatively ancient and inefficient compared to newer options. 
It also has a slower switching frequency of roughly 150kHz, which may introduce higher output ripples (that may not matter for this application but its still good to keep that in mind for other projects).
Its always good practice to test the DC-DC converters you've gotten with an oscilloscope to make sure that it fits your project requirements.

A red pushbutton with built-in LED is used to switch the laptop power supply on and off. 
It is connected to the input side of the laptop charger. 
To power the internal LED, a 5V Micro-560 Pro buck module is used to step-down the 19.5V from the power supply to a steady 5V. 
However, a regular switch without the built-in LED indicator can also be used, in which case the Micro-560 module would not be required anymore.

Two banana ports are used as the output connectors, as this is what's commonly found on other lab bench power supplies. 

The power supply module used is a XY-SK150S adjustable buck-boost power supply, with a maximum power output of 150W (6-36V input voltage, 0-40V output voltage, 0-8A output current). 
There are many other such power supply module, though the majority of it are **buck** modules, which means that they can only supply an output voltage **lower** than the input voltage supplied. 
Since the laptop charger I'm using can only supply 19.5V, that means that the maximum output voltage of the power supply would probably be about 18V (since the output voltage of such buck converters are typically 1-2V smaller than the input), which isn't very helpful since some applications may require the power supply to give 24V and higher.
The power supply comes with several features such as constant current and constant voltage features for accurate adjustments of voltage and current. 
It also has several safety features such as anti-reverse polarity and supports lithium battery charging (with under-voltage, over-voltage, over-current protection and etc, [refer to the manual here](https://manuals.plus/ae/1005008906878438))
If you are certain that your applications would require less than 150W, then you can also go for similar models such as the XY-SK120S (with a maximum power output of 120W), XY-SK80 (with a maximum power output of 80W and does not have a TFT display). 
I've decided to go with the 150W model as this would allow me to replace my laptop charger with a power source of bigger output power without having to change the power supply module. 

# Components:
1. 120mm x 120mm 12V cooling fan
2. 12V Mini-560 Pro Buck Converter
3. 5V Mini-560 Pro Buck Converter
4. Red Pushbutton with internal LED
5. Red and Black Banana Plugs (Female)
6. XY-SK150S Adjustable Buck-Boost Power Supply
7. Heat Shrinks of Varying Sizes
8. PLA 3D filament

<div align="center">

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/f7ccc004-a680-4aa5-9b45-016438eef96c" width="700"><br>
      <sub><b>Figure 1:</b> Circuit Schematic of the Power Supply</sub>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/95dcf6d1-8fc5-4e13-9051-462cd69e71c4" width="700"><br>
      <sub><b>Figure 2:</b> Picture of the front of the power supply</sub>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/d2b2ed69-b4e4-42af-a2b1-a9da1d40fdb7" width="700"><br>
      <sub><b>Figure 3:</b> Picture of the top of the power supply</sub>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/9e8af5b8-cf24-4819-9dfe-44928e1cf1a4" width="700"><br>
      <sub><b>Figure 4:</b> Picture of the back of the power supply</sub>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/c57a191f-8aef-49fa-8b5a-26fd8949fd1e" width="700"><br>
      <sub><b>Figure 5:</b> Picture of the internals of the power supply</sub>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/a9aa4723-c2f7-4f53-94b5-f92835d812d8" width="700"><br>
      <sub><b>Figure 6:</b> Picture of the power supply</sub>
    </td>
  </tr>
</table>

</div>
