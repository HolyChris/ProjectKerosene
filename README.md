# What is Project Kerosene?

Every embedded hardware developer faces the same workflow every time they want to get started with a new device. Before they can evaluate a sensor, before they can deploy, and even before they can write a single line of code they must go through the following process:

1. Have the device in hand 
1. Download the proper drivers
1. Connect to the device
1. Set up their development environment with the proper deployment toolchain
1. Find a 'Hello World' code snippet to ensure the device is functional
1. Get the board to flash correctly, deploy your code, and start building your application. 

Project Kerosene offers the ability to skip to the last step: have a board with the correct toolchain available from anywhere on the planet. It is not a virtualized board, it is not a board with remote access, it is Hardware-As-A-Service where you can request a session on a physical device to get up and running with new hardware with no overhead. 

The following demonstration offers you the chance to become familiar with the ST Micro B-L072Z-LRWAN1 Discovery board which has a ST X-NUCLEO-IKS01A3 sensor board attached. Using this, you can build and test an entire end-to-end IoT Application on the Helium Network from anywhere on the planet with no need to have a single piece of hardware in your possession.


# Getting Started with Helium Tutorial

**NOTE: DUE TO A SUB-BAND CHANGE ON THE HELIUM NETWORK, THIS TUTORIAL IS NOT FUNCTIONAL. WE ARE WORKING TO RESOLVE THIS!**

In this tutorial, we'll provision a new device on the Helium network, request a remote session using Project Kerosene on an ST Micro B-L072Z-LRWAN1 Discovery board which has a ST X-NUCLEO-IKS01A3 sensor board attached, place our newly provisioned device keys into the provided sample code, flash our code onto the Discovery board, then see our data traverse the Helium network in real time, on real devices. At the end of the tutorial, we suggest what you can do with this system beyond an introduction. 

![Device Creation](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/ConnectingTo.JPG)

*IMPORTANT: We are looking for feedback on this service and would genuinely appreciate hearing about your experience. It would be immensly useful if you could answer the following questions and email them to c@m3r.co*

Desired Feedback:

1. Have you used LoRaWAN devices or the Helium Network Before?
1. What are you initial thoughts on the service?
1. Did this make it easier for you to get started with LoRaWAN and helium?
1. Is there anything you might think of using this service for?
<!-- 1. On a scale of 1-10, would you recommend this to a friend? (1= Would not recommend, 10= Would highly recommend) -->

Thank you and please let us know what you think!

**(NOTE: We currently do not support smartphones or tablets)**

## Overview Video

[![Project Kerosene Overview Video](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/Intro.png "Project Kerosene Overview Video")](https://youtu.be/n0ywquV5GpY)

## Getting Started

1. First you need to have a Helium Console account. Create one at https://console.helium.com/dashboard
1. Once you're logged in, you will want to create a new device, click on 'Devices' then on the right side, click 'new device'
   - ![Device Creation](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/DeviceCreation.png)
1. Give your device a name, and click okay. 
1. Next you'll want to get your APPEUI, DEVEUI, and APPKEY values in the correct format. Click on the device you just created 
   1. ![Key Location](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/KeyLocation.png)
1. Next, you'll want get your keys in the correct format, click on the arrows next to the keys to change the format to least significant bit (lsb) or most significant bit (msb). You'll want both the APPEUI and DEVEUI in lsb format, and the APP KEY in msb format
   1. ![Key Format](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/KeyFormat.png)
1. Now we're ready to request a remote session using Project Kerosene: 
   - **[Click THIS LINK to request a session.](https://rerobots.net/sandbox/helium/gy4Z4kRfgn4yAuavaWeGWQjjF1WJeQt6)** 
   -  If there are no boards available, please wait a few minutes and refresh the page. We are currently limited by the number of devices available.
   - _(If you are unable to get an instance, please reach out to c@m3r.co)_
1. When you have a remote session, you'll be presented with a screen  showing an editor on the left, a 'terminal' on the right, and 2 buttons of 'build' and 'flash'. Now you're ready to input your fresh device keys. 
   1. ![Environment](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/Environment.png)
1. In the Helium Console, copy the app eui  key in the LSB format
   1. ![Copy Keys](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/KeyFormat.png)
1. Paste that key in between the brackets where it says APPEUI
   1. ![Where to place keys](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/SampleCodeKeyLocation.png)
1. Next, copy the DEVEUI key in the LSB format from the Helium Console, and paste that value betwen the brackets marked DEVEUI in the sample code
1. Now, copy the APPKEY key in the MSB format from the Helium Console, and paste that value betwen the brackets marked APPKEY in the sample code
1. If you'd like to check  your code for compile errors, you can do so by clicking the 'build' button
   1. ![Build](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/BuildStep.png)
1. The results of the build will be displayed on the panel to the right of the editor. If your build says success you’re ready to flash your code onto the board. 
1. When you click the 'flash' button, your code will compile and then be deployed to the board. The results of the deployment  will show up on the panel to the right
   1. ![Flash Device](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/FlashStep.png)
1. If you use the sample code provided and you input your keys correctly, after a few moments you will begin to see data come from this within the Helium Console. 
   1. ![Console with real data](https://raw.githubusercontent.com/HolyChris/ProjectKerosene/master/images/DataComingThrough.png)
1. You can now set up your backend services like AWS IOT or Helium Cargo as a way to store the data that you were transmitting over the network. [Here is a great video on how to get started with AWS IOT](https://youtu.be/XLxUgwdbqG8)
1. You can also modify the code in the editor to make changes to the data that you want to transmit.
1. Initially these device sessions will be limited to 15 minutes. If you would like a longer duration of time, please reach out to c@m3r.co
1. ...
1. **PROFIT**

## What now?

First, thank you for taking the time to try this out! We'd LOVE to hear your thoughts, what made sense, what didn't, or anything about your experience you'd like to share. Here are the following questions we're most interested in:

1. Have you used LoRaWAN devices or the Helium Network Before?
1. What are you initial thoughts on the service?
1. Did this make it easier for you to get started with LoRaWAN and helium?
1. Is there anything you might think of using this service for?
<!-- 1. On a scale of 1-10, would you recommend this to a friend? (1= Would not recommend, 10= Would highly recommend) -->

**Please send your response to c@m3r.co and we'll be in touch**

### Here's how we envision utilizing this service

Now that you're gotten this far, I'd like to share how we think of this project, if any of these reasonate, let's talk. 

1. Give new users of hardware platforms real experience with the device without requiring it to be in their possession.
1. Effective, distributed, and remote training opportunities on real devices which are always in a known state (no more device setup during training!)
1. Application developers can quickly evaluate hardware platforms
1. Application developers can quickly evaluate sensors
1. Have the ability to take code that might have worked in a simulator and run it on a physical device
1. Co-operatively debug code running on an embedded device (disambiguate hardware, software, and firmware issues)
1. Integrate Continuous Integration processes with on demand physical devices

