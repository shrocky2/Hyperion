# Welcome to my Hyperion Ambient TV Light Project instructions.

You can view my YouTube installation video here: COMING SOON (Aug 2020)

# For this project, we'll be using the following hardware:
1. Raspberry Pi (any Pi will work) I'll be using a Raspberry Pi Zero W. This project will require the Pi to talk to your home network (WiFi), so we need a Pi that has network capabilities.
2. Micro USB card for the Raspberry to install our OS ( https://amzn.to/2DFaUIT ) You'll need a SD card that is 4GB or larger
3. An Arduino that will control an LED Light Strip. I picked up these Arduino Nano clones: https://amzn.to/3a0Pbr1
4. WS2912B LED light Strip. My LED strip ( https://amzn.to/3gpbbON ) has 150 LEDs and is 16.4ft. There are LED sets that have more LEDs per foot...while that'll give you a brighter ambient light, it'll use more electricity, so you might need a larger power supply.
5. HDMI capture card ( https://amzn.to/33qUoav or https://www.aliexpress.com/item/4001032102280.html ) I bought mine on Aliexpress, but Amazon has an easier return policy.
6. Micro USB Hub ( https://amzn.to/2DENYJK ) This hub will give the Raspberry Pi Zero W four stand USB ports...The Raspberry Pi Zero only has one usable micro USB port, and we'll need 2 ports, 1 USB port for the HDMI Capture Card, and 1 for the Arduino Nano. If you already have a USB Hub, but you need a USB to Micro USB cable, I have a couple of these ( https://amzn.to/33qHadF )
7. Power Supply. You'll need 1 power supply to power the Raspberry Pi ( https://amzn.to/3k9HaEW ), and a 2nd (Much Larger) power supply to power the LED Light Strip. My 110 LEDs require 5V and use about 7.5Amps...using the Formula VOLTS x AMPS = WATTS, (5V x 7.5A = 37.5Amps), I would need a Power Supply that is larger that 37.5 Amps, so a power supply like this (50Watts) would work for me ( https://amzn.to/30ruOA4 ). REMEMBER...the more LEDs you have, a larger power supply would be needed.
NOTE: if you use multiple Power Supplies, ie 1 Power Supply for the Pi & 1 Power Supply for the LEDs, you will need to connect a GROUND wire from Raspberry Pi (or Arduino) to the LED Light strip. Not doing so will cause a Floating Ground issue that might cause your LEDs to not fuction correctly.

# Software
Software for the Raspberry Pi can be Downloaded here: ( https://github.com/hyperion-project/HyperBian ) Is a ready to use image for your Raspberry Pi. Based on the original Raspberry Pi Foundation image "Raspberry Pi OS Lite". Hyperion is already pre installed.

More Info to Come...
