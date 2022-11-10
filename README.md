##this code is unmaintained and untested with current QMK revisions!

# keyhive-sofle-trackball-integration

This guide is to add support for the pimoroni trackball to the keyhive sofle v2.
There is no current support for rgb, nor do i see any planned unless i get a pcb that has more than half the leds able to be lit up.

first clone the repo below. This was the first repo with support for the pimoroni trackball.

https://github.com/foureight84/sofle-keyboard-pimoroni/tree/a1ff268a4958e55b6503ea3f810bb59c537bf5da

rename the file qmk_firmware 

go to the keyboards > sofle folder and replace rev1 with the rev one in this repo. (i like to rename it to compare files)
compile with: compile -kb sofle/rev1 -km foureight84

flash like you would normally

for pro-micro: 
qmk flash -kb sofle/rev1 -km foureight84 -bl avrdude-split-left
or
qmk flash -kb sofle/rev1 -km foureight84 -bl avrdude-split-right

for elite-c:
qmk flash -kb sofle/rev1 -km foureight84 -bl dfu-split-left
or
qmk flash -kb sofle/rev1 -km foureight84 -bl dfu-split-right 

to solder the pimoroni trackball, use the same method as in the above repo.
for vcc either use p1, the pin on the oled, or solder directly to the underside of where the pro micro or elite c was soldered, matching the leads coming off the trackball.


changes that were made are in the config.h file and rev1.h
