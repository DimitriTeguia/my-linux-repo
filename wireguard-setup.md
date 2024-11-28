## Server Setup (PiVPN)
- install following: https://www.pivpn.io/
- choose cloudfare (easiest (1.1.1.1))
- use custom DNS query (for that you need to setup a dynamic DNS e.g. FreeDNS: follow https://notthebe.ee/blog/set-up-your-own-vpn-on-raspberry-pi/#template)
- forward port


## Client Setup

- sudo apt update && sudo apt upgrade -y
- sudo apt install wireguard
- sudo mkdir /etc/wireguard
- sudo nano /etc/wireguard/<config_name>.conf
- copy config from server in the file.
- sudo wg-quick up <config_name> (or sudo sudo nmcli connection import type wireguard file /etc/wireguard/<config_name>.conf)
- sudo systemctl enable wg-quick@<config_name>