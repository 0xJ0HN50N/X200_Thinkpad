# My X200 ThinkPad, A journey for privacy

This repository documents my journey with the classic X200 ThinkPad, which I have made fully libre and optimised for privacy and security. I was able to Libreboot my X200 using a CH341A programmer. Guides online and especially the libreboot website for the X200 made the process pretty easy. I initially chose Ubuntu Desktop for this project, but quickly switched to PureOS for its focus on privacy and a completely free software ecosystem with no proprietary software, which better suited the project.

<p align="center">
  <img src="https://github.com/user-attachments/assets/ac22a08c-cc0b-4680-a3bf-15e5c14601ea"
       alt="Thinkpad_with_new_screen"
       width="500">
</p>


## Hardware Modifications
I found hardware modifications on the X200 very straight forward. After removing a few screws and lifting the keyboard, I had access to the internals and started upgrading components. The first change that I made was replacing the stock Wi-Fi card with one that supports monitor mode and packet injection. While I had the X200 open, I also removed the internal speakers and the small USB/audio daughterboard to free up space inside. 

I then installed a WWAN card along with antennas putting them into the space freed up that I created earlier. With a valid SIM card inserted my X200 can now connect directly to the cellular network, and due to it being librebooted it has access to use 4G LTE for sms. Additional upgrades include replacing the original 4GB of RAM with 8GB, and also installing a new 512GB SSD, both of these upgrades had a huge performance boost on the laptop and allow it to perform daily tasks much smoother. I have also upgraded the original display in my ThinkPad X200 with an HV121WX4-120 AFFS wide-angle LCD panel, which offers significantly improved viewing angles and better image quality compared to the original display.


<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/14c2b767-f985-4459-aeef-5654e7c684ef" alt="Hardware" width="75%">
      <br>
      <b>Hardware Modifications</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/8d42977b-47cc-4263-8d8e-ec93451d2fe6" alt="RAM Upgrade" width="75%">
      <br>
      <b>RAM Upgrade</b>
    </td>
  </tr>
</table>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/c26422b1-722c-41f2-aac0-7eb5e7807376" alt="Install New Screen X200" width="50%">
      <br>
      <b>AFFS Display Upgrade</b>
    </td>
  </tr>
</table>



### Libre Laptop Hardening & Security Configuration
My Lenovo ThinkPad X200 has been hardened with a focus on privacy and minimising proprietary software dependence. I run PureOS on it meaning I benefit from the security foundation of Debian while also using a fully open source operating system. This combined with Libreboot, which replaced the proprietary BIOS and removed nearly all of Intel's proprietary firmware, brings the laptop close to being fully libre and a complete transparent environment.

I created a hardened version of PureOS's 99-sysctl.conf to improve kernel level network security, alongside a very strict UFW firewall rule set, MAC address randomisation, and a default deny network approach where communication is only allowed when I explicitly enable it after boot. I perform Lynis security scans and apply the recommended hardening suggestions when I can, while also auditing active network connections using tools such as ss and netstat to remove unnecessary services. In addition, I run both Whonix Gateway and Workstation through Virtual Machine Manager as an isolated environment for OSINT research, security tools, and testing. All these measures I have put in place reduce the attack surface of my X200 ThinkPad while maintaining a fun, usable, privacy focused workstation.
