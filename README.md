## WAN MAC address randomizer for OpenWRT

### Purpose
This script generates a random MAC address for the WAN interface on an OpenWRT router. It is implemented as an [init script](https://wiki.openwrt.org/doc/techref/initscripts), so it is able to randomize the MAC address every time the router restarts.

### Dependencies
Nothing special. It should work on a base OpenWRT system.

### Usage
1. Copy `wan-mac` to `/etc/init.d/`
2. Make sure the file is executable (`chmod +x /etc/init.d/wan-mac`)
3. Modify the `START` line in the file if you'd like to customize the init order (optional)
4. Enable the service so it will randomize the MAC address on every boot (`/etc/init.d/wan-mac enable`)
5. Restart your router or start the service manually (`/etc/init.d/wan-mac start`)

### Notes
Tested on a TL-WR1043ND 1.0 running OpenWRT Chaos Calmer.

### License
WTFPL
