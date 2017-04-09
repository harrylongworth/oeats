
# How to format Mark Down?

https://en.wikipedia.org/wiki/Markdown

# Auto Mount USB storage in the websever folder

http://www.techjawab.com/2013/06/how-to-setup-mount-auto-mount-usb-hard.html

sudo apt-get install ntfs-3g

ls -l /dev/disk/by-uuid/
to list devices (when have USB plugged in)

Nope - requires device specific configuration

http://askubuntu.com/questions/214646/how-to-configure-the-default-automount-location
 not really
 
 

# How turn RP into a hotspot?

https://www.maketecheasier.com/set-up-raspberry-pi-as-wireless-access-point/

# How route all traffic to local webserver

from 
https://www.raspberrypi.org/forums/viewtopic.php?t=33708&p=350253

sudo iptables -t nat -A PREROUTING -d 0/0 -p tcp --dport 80 -j DNAT --to-destination 192.168.42.1:80

where 192.168.42.1 is the PI address

# Download Youtube?
savemedia.com

# Safely shutdown PI
sudo shutdown -h now

# Use dnsmasq instead

http://www.andrewoberstar.com/blog/2012/12/30/raspberry-pi-as-server-dns-and-dhcp

stop current DHCP service
sudo service isc-dhcp-server stop


# Remove package

What is the correct way to completely remove an application
apt-get remove packagename
will remove the binaries, but not the configuration or data files of the package packagename. It will also leave dependencies installed with it on installation time untouched.
apt-get purge packagename or apt-get remove --purge packagename
will remove about everything regarding the package packagename, but not the dependencies installed with it on installation. Both commands are equivalent.








