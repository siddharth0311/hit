BoneScript SocketIO Example
===========================

This is an example of how to use Socket.IO and BoneScript to control a BeagleBone Black from a remote device. You'll be able to control the brightness of LED's from a mobile device (cell phone, tablet) and use motion to control the LED's. The code uses Node.js as the web server, Socket.IO for communication between the web page and the BeagleBone Black, and Mobile JQuery for the web page lay-out.


Getting Started
---------------
What you'll need:
- 3 LED's (Red, Green, Yellow)
- 3 330 Ohm resistors
- Breadboard
- Jumper wires

Put these parts together following the diagram in the .png file. This example uses PWM pins P9_14 ,P9_16 and P8_19 so we can dim the LED's. 


Installation
------------
Make sure you have an Internet connection through a network cable or Wifi. Connect to the BeagleBone Black by SSH. Set the current time just to be sure:

````sh
/usr/bin/ntpdate -b -s -u pool.ntp.org
````

Install Socket.IO:

````sh
cd /var/lib/cloud9
npm install socket.io
````

Download files from GitHub to the BeagleBone Black:

````sh
cd ~
git clone git://github.com/lgxlogic/BoneScript-SocketIO
cp bonescript-socketio/*  /var/lib/cloud9
````

Go to the Cloud9 IDE on the BeagleBone Black, open HtmlLedDemo.js and click the RUN button. In the console you'll see the IP address of the BeagleBone Black on your network. Enter this IP address in a web browser on your cell phone or other device. Motion control only works on cell phones and tablets with modern browsers such as Google Chrome on Android. To see if your device is supported, go here: http://www.html5rocks.com/en/tutorials/device/orientation/deviceorientationsample.html


More info
---------
Visit Logic Supply to buy the BeagleBone Black and accessories at http://www.logicsupply.com/categories/beaglebone

Please follow Logic Supply on Google+ at https://plus.google.com/u/0/b/103613886667848850929/

Written by Roland Groeneveld for LGX / Logic Supply.

MIT License. All text above must be included in any redistribution.
