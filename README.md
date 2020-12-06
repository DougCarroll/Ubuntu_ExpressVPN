# Ubuntu_ExpressVPN
Desktop Icons for Ubuntu

Full instructions can be found on the ExpressVPN website

If you need to install on Raspberry PI, you'll need to use openvpn and make
your .desktop file look something like this, after downloading files from
ExpressVPN to use.  You need certificates in ovpn file, and username/password 
in vpn_connect file.

	#!/usr/bin/env xdg-open
	[Desktop Entry]
	Version=1.0
	Type=Application
	Terminal=false
	Exec=gnome-terminal --title ExpressVPN -- pkexec openvpn --config /home/<USERNAME>/VPN/my_expressvpn_usa_-_dallas_udp.ovpn  --auth-user-pass /home/<USERNAME>/VPN/vpn_connect
	Name=ExpressVPN
	Comment=ExpressV_Dallas
	Icon=/home/<USERNAME>/.icons/ExpressVPN.png


To install on regular PC:
	
	$sudo dpkg -i expressvpn_3.2.1.2-1_amd64.deb
	$expressvpn activate

Then pull down these file from Github, change <USERNAME>, and you should be good to go.

