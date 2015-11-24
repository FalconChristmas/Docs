# Network Setup

- [Interface Settings](#interface-settings)
- [DNS Settings](#dns-settings)

<a name="interface-settings"></a>
## Interface Settings

### Interface
On a standard RPI unit this will be eth0 only. Eth0 is the network jack on the RPI. If you added a WiFi dongle, you will also have wlan0. Select from the dropdown which interface you wish to configure.

### Interface Mode
**Static or DHCP**
- Static is a specific IP address you want the select interface to bind to. Please note this HAS to be a unique IP address on the network. Multi machines can not have the same IP and will just cause you problems. 
- DHCP is a auto assigned IP from your router. Once this IP has been assigned, as long as your router continues to see this device on your network it "SHOULD" keep that assinged IP unless you reset the DHCP settings of your router then this can change. In DHCP mode you can not assign any of the following 3 entries in the Interface section as these come from your router.

### IP Address
In static mode you can enter the desigered IP in the form of ###.###.###.### (Ex: 192.168.0.26). You do not need to put in leading 0's, but you do need all 4 sections seperated by a "."

### Netmask
In static mode normally this is 255.255.255.0 for most setups. If your setup is unique, you will know if a different netmask is required for your network.

### Gateway
In static mode normally this will be one of 2 different setups. Format again is in ###.###.###.### and could end in .1 or .254 for most home routers (Ex: 192.168.0.1 or 192.168.0.254). If you are not sure you can look at your network properties for your laptop or desktop to see what its gateway IP is set to.

### Update Interface
Will save your currently selected interface configuration to your flash drive. A Restart Network button will appear. You can attempt to restart the network - but it is recommended to finish up your Interface and DNS settings, and then reboot the unit from the main status screen. Sometimes the RPI will not update it's network without a reboot.

> NOTE: If you are configuring both eth0 and wlan0, they should not be on the same networks. A common setup is eth0 on a dedicated lan (Ex: 192.168.1.100) and wlan0 setup either Static or DHCP. Either way only ONE interface should have a Gateway IP. The interface that needs to get out to the Inet for remote access or updates should be the only interface with a Gateway IP setup.

<a name="dns-settings"></a>
## DNS Settings

### HostName
This must be a single word, 8 letters or less, alpa/numeric only (no symbols, punciation or spaces) and should be unique to your setup. This lets the Falcon Player software find other compatible player devices on your network and also allows you to access that unique player by its name in your web browser. Some common examples are FPP1, FPP2 or FPPM, FPPS1, FPPS2 etc.

### Save
Button will set the hostname and save it to your flash drive configuration.

### DNS Server Mode
Manual or DCHP Mode

### DNS Server 1 
In Static mode this is in the standard IP format of ###.###.###.### - most of the time this will be the IP address of your router. This can also be a public DNS IP as well (Ex: Google is 8.8.8.8).

### DNS Server 2
Optional, but same setup as DNS Server 1.

### Update DNS
This will update your DNS settings configuration on your flash drive. A Restart DNS button will show up allowing you to restart the DNS server program without rebooting.

