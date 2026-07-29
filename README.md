# My X200 ThinkPad, A journey for privacy

This repository documents my journey with the classic X200 ThinkPad, which I have made fully libre and optimised for privacy and security. I was able to Libreboot my X200 using a CH341A programmer. Guides online and especially the libreboot website for the X200 made the process pretty easy. I initially chose Ubuntu Desktop for this project, but quickly switched to PureOS for its focus on privacy and a completely free software ecosystem with no proprietary software, which better suited the project.


## Hardware Modifications
I found hardware modifications on the X200 surprisingly straightforward. After removing a few screws and lifting the keyboard, I had full access to the internals and could start upgrading components. The first change that I made was replacing the stock Wi-Fi card with one that supports monitor mode and packet injection. While I had the X200 open, I also removed the internal speakers and the small USB/audio daughterboard to free up space inside. I then installed a WWAN card along with antennas putting them into the space freed up earlier. With a valid SIM card inserted my X200 can now connect directly to the cellular network, allowing it to use 4G LTE for sms. Additional upgrades include replacing the original 4GB of RAM with 8GB, and also installing a new 512GB SSD.

<img  src="https://github.com/user-attachments/assets/14c2b767-f985-4459-aeef-5654e7c684ef"  alt="Hardware"  width="50%">

### Upgrading from 4GB of RAM to 8GB of RAM:
<img  src="https://github.com/user-attachments/assets/8d42977b-47cc-4263-8d8e-ec93451d2fe6"  alt="RAM Upgrade"  width="50%">


### Hardened-Version-of-99-sysctl.conf
This is a Hardened Version of the 99-sysctl.conf in PureOS i made to lock down my X200 thinkpad to ensure it's got secure kernel-level networking behavior. 
