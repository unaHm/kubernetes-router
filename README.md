# kubernetes-router
Lacing together some tools to make a router/firewall of sorts

The goal of this repo is to create a simple router and firewall with some extra tools that might be useful, such as:

* PiHole
* DHCP
* TFTP/PXE
* HomeAssistant

The firewall/QoS is intended to be managed by `firehol` and `fireqos`, as documented here:

https://kubesail.com/blog/k3s-firehol-router

# Notes

* Make sure that your LAN interface is NOT configured with a gateway, because it IS the gateway! I forgot this and was stuck for a while :)
* I intend to eventually wrap this into a script so that it can be used to deploy on a fresh OS installation
* There are certain directories missing for some of the applications, particularly TFTP. Be sure to create these and install the required files so PXE booting can take place
