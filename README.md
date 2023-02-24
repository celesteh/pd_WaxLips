# pd_WaxLips
Based on Wax Lips by Tim Perkis.

See https://artifactrecordings.bandcamp.com/track/waxlips

## Setup
* Set the number box on the upper center to the number of people in your group.
* Find the IP addresses of your group mates and create a new message box for each person, which contains their address. Do not include yourself.
* Change the select box so the list of numbers starts at 0 and gets at least as high as your group size.
* Connect the outlets of the select box to the inlets of the IP address. Each address should have exactly one connection.
* Edit wax-player.pd

### wax-player.pd

The left inlet is a MIDI note, the right inlet is a MIDI velocity.  You must use the note input. You can control velocity however you want.

Possible uses of this file include making a MIDI patch to conect to a different piece of software or hardware. Or you may make a playable patch.  You may wish to have a few players that you can switch between.

### wax-plyer-polysyn-example.pd

wax-player-example.pd has some example players including the polysyn player.  This should open correctl in PD Vanilla, but may drop some connections in Purr Data.
The [poly 8 1] object should be connected to the [pack f f f] object beneath it, which should, in turn be connected to the [route] object.


## Play

One player must send out the first note. The patches will play themselves until collisions or other issues cause the programs to run out of steam. At that point, players may wish to regenerate their lookup tables, change their player and start again.  Or it may be an opportunity to end the performance.
