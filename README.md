# Welcome to my Hyperion Ambient TV Light Project instructions.

You can view my YouTube installation video here: COMING SOON (Aug 2020)

# For this project, we'll be using the following hardware:
1. Raspberry Pi (any Pi will work) I'll be using a Raspberry Pi Zero W ( https://amzn.to/3i3TfcM ). This project will require the Pi to talk to your home network (WiFi), so we need a Pi that has network capabilities.
2. Micro USB card for the Raspberry to install our OS ( https://amzn.to/2DFaUIT ) You'll need a SD card that is 4GB or larger
3. An Arduino that will control an LED Light Strip. I picked up these Arduino Nano clones: https://amzn.to/3a0Pbr1
4. WS2912B LED light Strip. My LED strip ( https://amzn.to/3gpbbON ) has 150 LEDs and is 16.4ft. There are LED sets that have more LEDs per foot...while that'll give you a brighter ambient light, it'll use more electricity, so you might need a larger power supply.
5. HDMI capture card ( https://amzn.to/33qUoav or https://www.aliexpress.com/item/4001032102280.html ) I bought mine on Aliexpress, but Amazon has an easier return policy.
6. Micro USB Hub ( https://amzn.to/2DENYJK ) This hub will give the Raspberry Pi Zero W four stand USB ports...The Raspberry Pi Zero only has one usable micro USB port, and we'll need 2 ports, 1 USB port for the HDMI Capture Card, and 1 for the Arduino Nano. If you already have a USB Hub, but you need a USB to Micro USB cable, I have a couple of these ( https://amzn.to/33qHadF )
7. Power Supply. You'll need 1 power supply to power the Raspberry Pi ( https://amzn.to/3k9HaEW ), and a 2nd (Much Larger) power supply to power the LED Light Strip. My 110 LEDs require 5V and use about 7.5Amps...using the Formula VOLTS x AMPS = WATTS, (5V x 7.5A = 37.5Amps), I would need a Power Supply that is larger that 37.5 Amps, so a power supply like this (50Watts) would work for me ( https://amzn.to/30ruOA4 ). REMEMBER...the more LEDs you have, a larger power supply would be needed.

NOTE: if you use multiple Power Supplies, ie 1 Power Supply for the Pi & 1 Power Supply for the LEDs, you will need to connect a GROUND wire from Raspberry Pi (or Arduino) to the LED Light strip. Not doing so will cause a Floating Ground issue that might cause your LEDs to not fuction correctly.

# Raspberry Pi Software
Software for the Raspberry Pi can be Downloaded here: ( https://github.com/hyperion-project/HyperBian ) Is a ready to use image for your Raspberry Pi. Based on the original Raspberry Pi Foundation image "Raspberry Pi OS Lite". Hyperion is already pre installed.

To burn the HyperBian image to your SD card you can use Win32 Disk Imager for Windows ( https://sourceforge.net/projects/win32diskimager/ ) or Belena Etcher for Mac ( https://www.balena.io/etcher/ )

Once you burn the HyperBian image to your SD card, you need to setup SSH and WiFi on the Pi. Create a file on the SD card called "wpa_supplicant.conf" (without the quotation marks) and inside enter to code found at this link: https://raw.githubusercontent.com/shrocky2/Hyperion/master/wpa_supplicant.conf replacing the SSID and Password with your Home WiFi name and Password. For SSH, create an empty file called "SSH" (without the quotation marks & without a file extention) and place that on the same SD Card.

# Arduino Software
Go to Arduino.com and setup a free account so you can use there FREE web editor. You'll need to install a Device Driver in order for the Web Application to install our software onto the Arduino. If you use an Arduino clone like I am in my video, You'll need to follow the Arduino Nano clone installion instructions to install a separate Device Drive for that specific Arduino. (The Arduino clones use a different driver than the Authentic Arduino)

Once inside the Arduino Web Editor, Create a NEW SKETCH and Copy/Paste the Code found here: https://raw.githubusercontent.com/shrocky2/Hyperion/master/ArduinoCode

Inside this code, you need to edit Line 3 to the number of LEDs you have around the boarder of your TV. In my setup, I have 110 LEDs.

On the left side of the Web Editor, Select Libraries, then Library Manager at the top...then Search for and install FASTLED.

More Info to Come...
