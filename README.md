I've included my SV08 configs for anyone who wants a starting place.  The configs supplied with the SV08 are essentially unusable.  These configs have printed a ton of stuff.  I have two SV08 and they are working about 50% of the time.

Many in the Sovol community prefer mainline klipper.  It can be installed using the excellent resource at: https://github.com/Rappetor/Sovol-SV08-Mainline


Here is how I bring up an SV08, once it has new firmware.

- PROBE_CALIBRATE
- Print the Layer 1 test (15mm disk).  This will use roughly 11mm of filament per print.  Slice it with one layer, one loop, skirt.
  - Peel the skirt from the build plate and measure with a caliper.  The thickness should be whatever you sliced.
  - Adjust the Z offset using [<sliced layer height> - <measured layer height>]

That should get you pretty close.

Happy printing.
