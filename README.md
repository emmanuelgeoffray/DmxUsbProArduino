Hello,

This is a firmware for arduino + dmx shield.

It makes the arduino compatible with programs that use the Enttec Dmx Usb Pro protocol.

It uses the [SimpleDmx library](http://code.google.com/p/tinkerit/wiki/DmxSimple).

This has been successfully tested with [SK Pang's Arduino DMX Shield](http://www.skpang.co.uk/catalog/arduino-dmx-shield-p-663.html), and should work with all mentioned by SimpleDmx. Make sure to change the TX pin according to your shield.

This has been sucessfully tested with the following software: [ofxDmx](https://github.com/kylemcdonald/ofxDmx), [pySimpleDmx](https://github.com/c0z3n/pySimpleDMX). And should work with others.

The implementation lacks some checking for bad packets for now. You're welcome to help!


# Installation

```
sudo apt-get install arduino-mk
sudo usermod -aG dialout $(whoami)
```

Restart your session for the changes on groups to take effect.
Or `su - $USER`

```
git clone https://github.com/TinkerKit/DmxMaster
sudo cp -r DmxMaster /usr/share/arduino/libraries/
git clone git@github.com:emmanuelgeoffray/DmxUsbProArduino.git
cd DmxUsbProArduino
make
make upload
```

