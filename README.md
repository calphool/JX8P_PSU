# JX8P_PSU
Replacement power supply for Roland JX8P

![Alt text](JX8P_PSU.jpg)

The power supply for the Roland JX8P is nearly 40 years old at this point, and if you own a JX8P you should probably be a little concerned about its 
typical manner of failing, which is to spike the +5V rail (your logic rail) frying lots of logic chips on your synth.  It is also built 
around heat generating linear regulators, which makes its demise even more likely.

I decided to replace mine preventatively, and this project is the result of that effort.  It's basically three Recom power modules with a common ground, and 
various conditioning components on the output side to make sure we have perfectly smooth rails, despite the fact that these are switching rather than linear 
supplies.  It works fabulously.

The LEDs and resistors near them are optional, but they give you an easy way to identify that all 4 rails are operating properly.  

Be aware that this 
PCB is managing mains voltages, so don't take on this project if you don't know what you're doing, or if this is a first attempt at building a PCB.  
**Don't fool with mains voltages unless you know precisely how to protect yourself.**

Also be aware that this PCB needs insulation on the bottom of the board.  The JX8P uses a shielded metal foil that is grounded.  You'll get fireworks if you 
just plunk this PCB down and connect it.  I used a sheet of plexiglass, and attached the board and plexiglass to the wooden base of the synth using 6-32 
nylon screws and nuts.

I sourced all the components from Mouser, though you can probably find them anywhere.  

The board has some safety features.  Since what we care about is the synth, I strapped all the rails to some very sturdy zeners that should protect the 
sensitive components of the synth if somehow one of the power units went out of spec.

The total current draw across the fuse is just above 1.5 amps, so a 2 amp fuse should probably be what you use.

I've included a Gerber .zip file, so you can just send the .zip to your favorite PCB fab house.

On the mains side (labeled N / L), you'll take the output of the JX8P's filter board, and connect it here.  Remove the transformer and the old power supply 
board.  The leads that used to go to the transformer (the green and the white) will now connect to this board.  The white one should connect to the N screw terminal and 
the green one should connect to the L screw terminal.

Regarding the connectors that go to the synthesizer itself, they are no longer available, so I desoldered the old ones from my old power supply board.  If 
you don't have good desoldering tools, you have other options.  You could snip the connector off of the synth and simply solder the wires directly, making sure to label 
them before you cut anything.  You could also change the connector to something more standard and user header pins, again be sure to label each wire before 
you do this.  The old power supply actually has markings for the voltages for each wire, and the wires are color coded as well.

At the time this was originally built (May 2025), you could get 5 PCBs from PCBWay for around $40, and the total cost for all the components is around $90, 
so for $130 you should be able to replace your old power supply, which is considerably cheaper than some so-called "professional" replacement power supplies 
I've seen online.  I seriously doubt that these "professional" boards are any more professional that this one, as all the heavy lifting is done in three 
components -- the Recom modules.  I didn't try it, but you *might* literally be able to get away with doing nothing more than connecting your synth directly 
to the outputs of the three Recom modules (making sure that you combine their output grounds).  I chose to put components after the output to make sure it's 
smooth and without ripple, but those Recom modules might be sufficient without all that stuff.

Best of luck.  As always, this project is a personal project.  I am not liable for any damage you do to your synth, to yourself, your friends and family, or 
to your property, even if there is an error in this design.  Build at your own risk, and make sure to check the output voltages on everything before you connect it to your synth.
