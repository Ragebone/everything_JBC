# Everything JBC

Everything there is to know about JBC soldering equipment. 

## Systems
An overview over the different JBC Systems.


### 105
- [Cartrige Pinout Source](http://adgd.ru/2021/01/04/jbc-soldering-cartridges-pinouts/)
- C105 for NT105 and NP105 Nano Soldering tools
- Those cartriges might be compatible with T2010?
NOTE C105116 is awesomely fine, maybe i need to get that. 

### 115
- C115 for NT115, NP115 and AN115 Nano Soldering tools

### 120
- C120 for PA120 or AM120 Micro Tweezers

### 130
- C130 for AP130 Solder Feed Iron 

### 210
- C210 for T210 Precision handles
- [Cartrige Pinout Source](http://adgd.ru/2021/01/04/jbc-soldering-cartridges-pinouts/)

### 245
- C245 for T245 Handles
- C245E Extended Life Tips Cartrige range for T245 Handles
- 24V
- Detection probably through cartrige resistance. 
- 3 Contacts
- Up to 160W ? 
- Common 75W
- Pinout: TODO
- Handle plug pinout: 5 blue, 1 green, 2 red
- Resistance-Measurments
- Tip diameters: 1.5mm, 3mm, 4.5mm
- Cartrige length: > 100 mm
- [Cartrige Pinout Source](http://adgd.ru/2021/01/04/jbc-soldering-cartridges-pinouts/)

### 250
- C250 for ALE250 and AP250 Irons
- C250E

### 360
- C360 for DS360 micro desoldering iron

NOTE C360001 0r C360011  is very interesting for replacing AM4 pins cince there is a 0.6mm hole with a "0.4mm max pin diameter".


### 470
- C470 for T470 and HT470 HD Thermal Tweezers
- Handle plug pinout: 5 blue, 1 green, 2 red
- Detection probably through cartrige resistance. 

### 420
- C420 for HT420 and AT420 Thermal Tweezers
- Handle plug pinout: 1 green, 2 red, 3 blue, 4 brown, 5 yellow, 6 330 Ohm resistor to green. 
http://adgd.ru/2020/02/16/jbc-ht420-a-teardown/

### 560
- C560 for DR560 desoldering iron

NOTE C560001 0r C560011  is very interesting for replacing AM4 pins cince there is a 0.6mm hole with a "0.4mm max pin diameter".

### 2010
- 24V
- 2 Contacts
- Up to 70W ? 
- Common 50W
- Pinout: TODO
- Handle plug pinout: 5 blue, 6 blue,  1 green, 2 red
- Resistance-Measurments
- Tip diameters: 1.5mm, 3.5mm
- Cartrige length 65.27mm on this specific one
- Heatingelement diameter 2.3mm

### 2210
### 2045
### 2245

## Pinouts

## Problems around compatibility

Not all JBC systems are compatible with each other.


### JBC Advance AD 2000 Case-Study

[Related EEVBLog Forum entry](https://www.eevblog.com/forum/repair/jbc-ad2200-soldering-station/)

This stations came to me with the following handle.
TODO Add picture
Handle: 2010 Advanced version 1 78850
With a 2010 Cartrige  78171

All of this poses a problem with the cartrige only being two contacts instead of the modern and common 3.
Resistance of the cartrige seems to be toward 2.7 Ohms measured with my crappy DMM.
This cartrige line is also out of production for multiple years limiting replacments and choice.

If the C210 is actually wired up internally as is described here, the system should be technically fully compatible with the AD2000.
It should just need the fitting C210 handle, a cartrige and possibly the modification to the handle or station to make the pinouts the same. 


[EEVBlog Forum thread "solution"](https://www.eevblog.com/forum/testgear/jbc-2010-cartridge-availability/)
```
Hi everyone,

Last week i've found and bought an old jbc ad 2000 soldering station. I've tried to use a T245 type handle, i've had the same problem as mentioned above, at 350 degrees (C) setting tip temperature was only about 200 degrees.

I've opened it up, checked the pcb, i've found out that the controller chip was actually a 28 pin pic mcu.

When i followed the the track from positive thermocouple pin of the handle on pcb, i've found the thermocouple amplifier (op07) The positive feedback resistor (at the left) of it was 1M Ohm. Amplified output was connected to one of pic mcu's adc channels.

I've attached a k-type temperature tester to tip of the iron, powered the station, at max setting tip temp was 190 degrees (C), TC amp->pic adc input voltage was 4,5V Dc.

I've paralled the feedback resistor with 1Meg resistor. With new feedback ratio, at maximum setting  tip temperature was 350 degrees.

That was my quick and painless solution, i hope if someone  still (or will) have the same problem uses it.
```
