# <h1 align="center"> Xiaomi Router 4AC 100M supported firmware </h1> 
<p align="center"> Padavan | OpenWRT | Keenetic | Stock </p>

<h1 align="center"> Termux </h1>

## Requirements
- Access Point Mode Router (Wired Repeater)
- [Termux_v118.apk](https://apkcombo.com/termux/com.termux/download/phone-0.118.1-apk)

# Auto Install
- Open termux and paste the command below 👇 
```sh
termux-setup-storage && pkg update && pkg upgrade -y && pkg install curl && curl https://raw.githubusercontent.com/xiv3r/termux-openwrt-invasion/refs/heads/main/openwrt-invasion.sh | sh && cd openwrt-invasion
```

# Setup
- Reset the Xiaomi-4AC router and configure it with a password of `12345678`.
- Connect the lan cable to Xiaomi 4AC Router WAN for internet.
- Connect to the Xiaomi_***** wifi and execute the command below 👇. 

```sh
python3 remote_command_execution_vulnerability.py
```
<img src="https://github.com/xiv3r/Xiaomi-Mi-Router-4A-Gigabit-KeeneticOS-4.1.7/blob/main/Screenshot_2024_1029_143545.png">

- Gateway:`192.168.31.1`
- Password:`12345678`
- leave default settings and hit enter

# <h1 align="center"> Transition From Stock to Keenetic or Padavan</h1>
  
- ## Getting the root access via `telnet`
```sh
telnet 192.168.31.1
```
- login:`root`
- passwd:`root`

- ## Method 1: Download from Repo
```sh
cd /tmp && wget -O KeeneticOS_v3.7.4-Full-16M.bin https://raw.githubusercontent.com/xiv3r/Xiaomi-4AC-100M-Custom-Firmware/refs/heads/main/KeeneticOS_v3.7.4-Full-16M.bin
```

- ## Method 2: Import the firmware using termux Fileserver (stable)
- Download here the [KeeneticOS_v3.7.4-Full-16M.bin](https://raw.githubusercontent.com/xiv3r/Xiaomi-4AC-100M-Custom-Firmware/refs/heads/main/KeeneticOS_v3.7.4-Full-16M.bin) 16MB keenetic firmware, Paste the commands bellow 👇
```sh
cd storage/downloads && wget -O KeeneticOS_v3.7.4-Full-16M.bin https://raw.githubusercontent.com/xiv3r/Xiaomi-4AC-100M-Custom-Firmware/refs/heads/main/KeeneticOS_v3.7.4-Full-16M.bin
```
- Add new termux terminal (swipe left) and paste the commands below 👇 
```sh
cd storage/downloads && python3 -m http.server -b localhost
```
- Goto 👉 [http://localhost:8000](http://localhost:8000)
- Copy the link of KeeneticOS_v3.7.4-Full-16M.bin file
```sh
cd /tmp && wget -O http://localhost:8000/KeeneticOS_v3.7.4-Full-16M.bin
```
- ## Flash the Keenetic Firmware
```sh
mtd -e ALL -r write /tmp/KeeneticOS_v3.7.4-Full-16M.bin ALL
```
- after rebooting
# 👉 Goto [192.168.1.1](http://192.168.1.1)
