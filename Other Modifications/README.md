# Other Modifications

Modifications were needed to tune this thing and make it print way nicer. Outside of updating to klipper and running it off of an Orange Pi, here are the modifications:

- All metal hotend (It's 2023, get the PTFE out of the melt zone)
- ABL (3D Touch knockoff)
- Silicone bed "springs"
- Rigid shaft couplings between the stepper and the Z lead screws
- Oldham couplings for the Z lead screws
- Thrust Bearings to support the Z lead screws

---

## All Metal Hotend

I found  some parts on Amazon that had close enough dimensions. I think they are a long way from good, but no worse than the stock setup.  I'll look around for hotend upgrades and update when I find something better.

- [Some random Titanium Alloy Therman Heat Break](https://www.amazon.com/dp/B07JD2S4GK)
- [Some cheap nozzles that are long enough to meet the heatbreak in the heater block](https://www.amazon.com/dp/B0C283TNWK)

---

## Automatic Bed Leveling and Probing

The knockoff kind of BL Touch that the Klipper documentation warns you about. It doesn't resond to the self test or some of the other diagnostic stuff, but it works.  You can see the setup in [the config file](../Klipper%20Config/printer.cfg). Print [this crappy mount if you want](Touch%20Mount.3mf). I may redesign later, but probably only if this one breaks or I take off the useless metal shroud it's attached to (more likely).

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