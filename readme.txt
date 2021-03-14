
A KiCAD respin of the 040-060-Adapter_mk2a Eagle project from a few years ago. Size of bottom PCB minimized for 
better fit, top/bottom PCBs combined into single multi-design, voltage regulator moved to top PCB and a couple of
other features.

I built the NO-DIODES PCB version only to later realize that the 68060 User's Manual recommends three diodes in series
(section 11.2.1.2) after people mentioned the diodes in different forum. I hacked/soldered three regular sized diodes
in series directly to the VCC and 3V3 pins on the voltage regulator but amended the KiCAD design and added the three
diodes in series. I never built this newer version, but if I was to attempt this again, it would be with the newer PCB
version with the diodes.

I ordered a thinner 1mm (vs standard 1.6mm) PCB for more access to thicker part of socket pins. The top PCB marks
the pins with circles that need to be cut. Care has to be taken to prevent the marked 040 pins on the bottom PCB from
contacting the 060 pins on the top PCB. Worst case 5V goes to 060 3.3V pins. It was not enough to just cut the circled
pins, I also popped out the corresponding pins from the 040 socket, cut them right above the ferrule and put them back
in. Because the cut pins on the 040 socket are now technically damaged, it's mainly the solder on the underside of these
pins that are keeping them from pushing up onto the 060 pins when inserted into CPU socket, so I measured resistance
from VCC to 3V3 after install to make sure there were no short circuits.

I used real 040 and 060 sockets. There is not much room between the pins for the soldering iron. I had to use a thicker
chisel soldering tip at higher temperature to allow enough heat for the solder to wick to the thin pin solder pads. A
lot of the pads are connected to the ground or power planes that act as big heatsinks sucking away the heat, causing
solder to only stick to the pins instead of also to the solder pads. Both top and bottom PCBs should be carefully
inspected to make sure the solder has actually wicked to the solder pads, and that there are no shorts and no excessive
solder on pins. Might be easier to just use cheap socket strips instead of real sockets. The strips could be soldered
row by row (with CPU or other strips inserted to keep them straight) which would allow much better access for the
soldering iron tip.

