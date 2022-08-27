# HNG

The Home Network Guardian Tools Installer.

Although not fully optimised like on the Final Image that can be dowloaded [here](https://nurisi-my.sharepoint.com/:f:/g/personal/b_nurisi_onmicrosoft_com/EhBmyiICp7BMt1WtO7_jvTwBI65f2S7nWnSgIp6aIMZKvA?e=ldenDv) (Password: homeguardian )

this script should essentially seamlessly install all the prequiistes and let you configure everyhting yourself.

***

## Initial Deployment Deployment
Use an ethernet cable to connect the HNG to your Router

Find out the router Admin Page of your Home Router usually hosted at 192.168.0.1 or 192.168.1.1 

It looks something like this

![image-1.png](.//Screenshots/image-1.png)

Find which IP has your Router given to HNG Hostname by moving to the DHCP page of your router

![image-2.png](.//Screenshots/image-2.png)

Use your Router DHCP Settings to reserve the said IP for HNG to avoid conflicts.

![image-4.png](.//Screenshots/image-4.png)

If your Router Doesnt support DHCP Reservation HNG would work but the moment router DHCP expires additional configuration might be required.


## Installation
Run the master installer. This is a modified script from PiHole PiVPN and the IDS to minimise installer promts and ease the installtion.

sudo bash ./masterscript.sh


## Post Installation

## DNS 
Go back to your Router Page open DHCP Settings 

Change the DNS Server to the HNG IP do not give an alternate DNS Server

![image-5.png](.//Screenshots/image-5.png)

If your ISP(like SFR, Orange, Free) doesnt support DNS Change then turn off DHCP 

![image-6.png](.//Screenshots/image-6.png)

Now access your PiHole admin page by going to HNG IP/Pihole and Enable DHCP in Pihole and set the default gateway as your HNG IP

![image-7.png](.//Screenshots/image-7.png)

## Port Forwarding

Go to your router NAT Page and add the following PortForward to ensure VPN Connection.

![image-8.png](.//Screenshots/image-8.png)


## Start Using
All Necessary configurations are done you must be able to seamlessly use HNG now
