# <h1 align="center"> Xiaomi Router 4AC 100M supported firmware </h1> 
<p align="center"> Padavan | OpenWRT | Keenetic | Stock </p>

## Requirements
- Access Point Mode (Wired Repeater)
- Termux

# Transition from Stock to other firmwares
• Using Termux app

• Dependencies:
 - `apt update; apt upgrade -y ; apt install git wget python3 python-pip inetutils -y`

• Using my Modified version of openwrt-invasion
  - `termux-setup-storage && pkg update && pkg upgrade && pkg install curl && curl https://raw.githubusercontent.com/xiv3r/termux-openwrt-invasion/refs/heads/main/openwrt-invasion.sh | sh && cd openwrt-invasion`

• `Reset` the Xiaomi 4C Router and setup with a password of `12345678`
  - `python3 remote_command_execution_vulnerability.py`

• Getting root access via Telnet
  - `telnet 192.168.31.1`
  - login:`root`
  - password:`root`
 
