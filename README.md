# wifidog_mwan
Problem statement:
Make wifidog and multi-wan packages work together on openwrt

WiFidog is a captive portal/hotspot solution for openwrt based WiFi routers. 
https://wiki.openwrt.org/doc/howto/wireless.hotspot.wifidog

Multi-Wan package on openwrt provides a way to use multiple internet connections for failover or loadbalancing on the same router.
https://wiki.openwrt.org/doc/howto/mwan3

Both packages manipulate firewall/iptables rules for their own purpose.

WiFidog uses iptables rules to mark users(their IPs) as new(authenticating) or authenticated.
It also report data usage statistics to the authentication server. 
We are using this package for a 'wifi sharing ecosystem' wherein we authenticate and monitor data usage of WiFi users

mulit-wan package uses iptables rules to load balance the traffic on multiple WAN interfaces.
Some places where internet is critical requirement need multi-wan feature wherein premise owners take 2 or 3 internect connections to ensure always on internet connectivity.

We need to make multi-wan work with wifidog, such that authentication and data usage can be tracked over multiple wan interfaces.

This project aims to do neccesary changes to wifidog and mwan3 packages to make them work together.
