# Other Modifications

Modifications were needed to tune this thing and make it print way nicer. Outside of updating to klipper and running it off of an Orange Pi, here are the modifications:

- All metal hotend (It's 2023, get the PTFE out of the melt zone)
- [Even better hotend solution](#v6-cheap-clone-hotend)
- [ABL (3D Touch knockoff)](#automatic-bed-leveling-and-probing)
- [Silicone bed "springs"](#springs)
- [Rigid shaft couplings between the stepper and the Z lead screws](#z-axis)
- [Oldham couplings for the Z lead screws](#z-axis)
- [Thrust Bearings to support the Z lead screws](#z-axis)

---

## All Metal Hotend

#### I have a [new solution](#v6-cheap-clone-hotend)

~~I found  some parts on Amazon that had close enough dimensions. I think they are a long way from good, but no worse than the stock setup.  I'll look around for hotend upgrades and update when I find something better.~~

- ~~[Some random Titanium Alloy Therman Heat Break](https://www.amazon.com/dp/B07JD2S4GK)~~
- ~~[Some cheap nozzles that are long enough to meet the heatbreak in the heater block](https://www.amazon.com/dp/B0C283TNWK)~~

~~You may also want to print [new 4010 Ducts](4010%20Duct%20Replacement.3mf). I only made these because I broke one of the existing ducts.  If you want to use it, you'll need to print it as is and a mirror for the left side.~~

---

## V6 (cheap clone) Hotend

I changed the hotend. The modifications I previously did where lackluster. I got tired of repairing and when it fell apart this time I just decided to replace.  I came across an old [YouTube from ModBot](https://www.youtube.com/watch?v=cXx1_OsDcIc) where he put an E3Dv6 on an older Two Trees coreXY.  Inspired by the mount he found, [I designed my own](V6%20Mount) and purchased a [cheap V6 clone from Amazon](https://www.amazon.com/dp/B0BR7Z63H8).

*UPDATE 2025-01-30: *I noticed that the bare plastic version where the M3 cut the threads was a little wobbly. It still printed, but I needed an excuse to make something. So I added a version with threaded inserts for the main body that holds the heatsink. You'll need 4 M3x6x5 threaded inserts.

---

## Automatic Bed Leveling and Probing

The knockoff kind of BL Touch that the Klipper documentation warns you about. It doesn't respond to the self test or some of the other diagnostic stuff, but it works.  You can see the setup in [the config file](../Klipper%20Config/printer.cfg).

Print [this crappy mount if you want](Touch%20Mount.3mf). ~~I may redesign later, but probably only if this one breaks or I take off the useless metal shroud it's attached to (more likely).~~

Offsets for crappy mount:  
x_offset: -33  
y_offset: 25  
z_offset: 3.00  


Or, when that one breaks becasue it's crap and you want to remove the useless metal shroud so you can see what's going on, you can [print this mount](Touch%20Mount%20-%20Back.3mf). It screws to the back of the print head where the rear shroud was attached. You will need longer M3 screws (I used M3x10mm, but 8mm would work too).

Offsets for less crappy mount:\
x_offset: 0\
y_offset: 25\
z_offset: 3.1


Both mounts are likely compatible with other Touch probes like the BL and Creality, but I have not tested.

- [3D Touch](https://www.amazon.com/dp/B09M9V8Y4Y "trust me, bro.")

---

## Springs

Probably not necessary, but I like them and they are cheap. I did have to make [some little spacers](SiliconeBedMountSpacers.3mf "put them on the bottom") to go under the Silicone springs becasue they were not tall enough.

- [3D Printer Heat Bed Leveling Parts](https://www.amazon.com/dp/B093Y89KS9)

---

## Z Axis

I was having a lot of trouble with z wobble and high pitch squeaking noise as the z axis moved so I looked at a bunch of videos and other stuff. Below is a list of what I did to change address the issue.
Starting from the bottom and working my way up, I put thrust bearings under the coupler to get the weaight of the Z assembly off the motors. They are held in place with a [little print](NEMA17_Thrust_Bearing_Holder.3mf) that fits over the heads of the motor mount screws.
Next up was replacing the flexible coupler. Using a flexible coupler to account for misaligned and wavy lead screws is low effort and does more to just allow the Z-axis to move than it does to correct the issue. I replaced with rigid shaft couplers. BUT only do this if you are addressing the lead screw binding with a different method (like oldham or wobblex).
Finally on the lead screw I added Oldham Couplers. Almost went with the WobbleX, but this thing called an Oldham showed up in search results and is like half the price so I gave it a try. I found [an adapter](https://www.printables.com/model/376711-sp-5-oldham-coupling-adapter) by [UNIT_normal](https://www.printables.com/@UNIT_normal_528315) on printables.

- [Thrust Bearings](https://www.amazon.com/gp/product/B07QLTXJDH "Maybe unneceary, but they are cheap.")
- [Rigid Shaft Coupling](https://www.amazon.com/dp/B08ZJ854Z6 "They don't do yoga")
- [Oldham](https://www.amazon.com/dp/B0BQMWC1VG "Named for leftovers past their prime.")