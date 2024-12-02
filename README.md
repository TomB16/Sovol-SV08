I've included my SV08 configs for anyone who wants a starting place.  The configs supplied with the SV08 are essentially unusable.  These configs have printed a ton of stuff.  I have two SV08 and they are working about 50% of the time.

Many in the Sovol community prefer mainline klipper.  It can be installed using the excellent resource at: https://github.com/Rappetor/Sovol-SV08-Mainline


Here is how I bring up an SV08, once it has new firmware.

- PROBE_CALIBRATE
- Print the Layer 1 test (15mm disk).  This will use roughly 11mm of filament per print.  Slice it with one layer, one loop, skirt.
  - Peel the skirt from the build plate and measure with a caliper.  The thickness should be whatever you sliced.
  - Adjust the Z offset using [Sliced layer height - measured layer height]

That should get you pretty close.  Once you are laying down a nice first layer, it's down to standard tuning.  There is a ton of Klipper tuning resource on the net.


Notes:

- The Sovol bed sensor is temperature sensitive and there is also significant thermal bed movement.  Because of this, these macros heat soak for a significant period of time (minimum 2, max 12 minutes, depending on toolhead temperature).  When the printer is being used, it will do minimal heat soak.  Feel free to adjust to taste.
- I have two SV08 received roughly two months apart.  The second one has a toolhead that runs 8*C cooler than the first.  Perhaps they used a different fan or slightly different duct.  Because of this, I set the two printers differently:  variable_heat_soak_temp = 42 (on printer 1), 36 (on printer 2).
- If you change your bed sensor, you will want to completely rejigger this heat soak.  If you use a stock sensor, you will lay down an accurate first layer every time but it does a lot of heat soak on a cold printer before printing.
- My printers are both 100% stock hardware, including the inductive bed sensor.  I have completely taken over the software, however.
- After 3 months with the first printer, I am extremely pleased with the SV08.  I've squeezed about 20Kg of plastic through the two printers in that time.  Early on, there were quite a few failures.  Once the config was at a decent point and the Orca Profile was reasonably well tuned, I don't recall having a failure.  The stock Sovol build plate is brilliant.  I print 99% PLA.


Happy printing.
