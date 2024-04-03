# Relieve Router OpenWRT Configuration 

This is a repo for the specific functionality of the TP Link TL-WR902AC router.

Once you have configured the router with OpenWRT using TL-WR902AC-OpenWRT.mp4

You then need to go to System -> Flash Firmware then restore the firmware from the file on the repo. This will configure the router with a LAN and WAN network and firewall settings etc.

Once you have the standard configuration you need to update all packages using opkg update and install opkg install openssh-sftp-server (using Putty or similar).

You will then be able to download WinSCP and connect via FTP to the router.

The 99-my-action file needs to placed into /etc/hotplug.d/iface directory and ensure that it's executable by chmod +x /etc/hotplug.d/iface/99-my-action

Using logread and connecting and disconencting a ethernet cable to an upstream router you shoudl see log messages.


