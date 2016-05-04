# wifidog_mwan
Make wifidog work with multi-wan on openwrt

WiFidog is a captive portal solution for openwrt. 
https://wiki.openwrt.org/doc/howto/wireless.hotspot.wifidog

Multi-Wan package on openwrt provides a way to use multiple internet connections for failover or loadbalancing on the same router.
https://wiki.openwrt.org/doc/howto/mwan3

Both packages manipulate firewall/iptables rules for their own purpose.

This project aims to do neccesary changes to wifidog/mwan3 packages to make them work together.
