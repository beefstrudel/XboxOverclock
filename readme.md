XboxOverclock with saving and reloading ability
============

XboxOverclock will allow you to overclock the FSB and NVCLK via software. It uses infromation gained from [XBOverclock](https://github.com/WulfyStylez/XBOverclock) by WulfyStylez.

Note: Text formatting on this fork needs work. 
If text on screen is overwritten all the controls are here.

Use the left and right DPAD to change the FSB.

Use the up and down DPAD to change the NVCLK.

Use X and A to change the memory divider.

Use Y to save overclock settings.

Press Start to apply (which will auto reboot).

Building
---------

See the requirements for [nxdk](https://github.com/XboxDev/nxdk/wiki/Install-the-Prerequisites).


```sh
git clone https://github.com/beefstrudel/XboxOverclock
cd XboxOverclock
eval $(../nxdk/bin/activate -s) make -f Makefile.nxdk
```

Then you'll have the xbe in the `bin` folder.

Running
---------

Once you boot into the xbe you'll see a prompt. Use the left and right D-Pad to change the wanted FSB frequency, use the up and down D-Pad to change NVCLK frequency.
This fork adds the ability to save the current settings with the Y button. Settings will auto load when the program starts. 

Hints
---------
Both over, and underclocking mess with the RAM frequency; the RAM on the Xbox is already overclocked out of the box thus the max it'll run is around ~235MHz, so to get higher CPU clocks you'll need to raise the memory divider. On a stock, recapped, 1.0 system I am able to run ~1077MHz (not exactly stable but running). Perhaps with some VCORE mods you'd be able to push this slightly higher, but I imagine a 40% OC is already pushing what this chip can do.
