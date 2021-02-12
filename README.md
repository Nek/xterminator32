A stupid as fuck MIDI controller hack for Behringer X32 Rack. Should work with the whole family of the devices. Should work with any MIDI controller but the implementation expects Launch Control XL to be used.

How to use:

1. get a raspberry pi

2. install purr data on it

3. put provided patch in your home folder

3. append 
```
sleep 5 
purr-data -nogui -open x32.pd
```
to .bashrc

4. switch raspberri into terminal auto login mode

5. configure your Launch Control XL. CC 1-8 correspond to the appropriate mixer board channel number. MIDI channel 01 is for levels, channel 02 is for pans, 03 for Send B (sends 9,10 on my board internally), 04 for Send A (13, 14 on my board internally).

6. edit the patch and put correct mixer board IP into the OSC message node

7. plug the board and the controller into raspberry and reboot

8. PROFIT!!! 
