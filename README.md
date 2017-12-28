# achiwa-v3
Achiwa is an intrusion detection software for individuals and small businesses

Current product URL (in french): https://www.tibsys.com/cybersecurite/achiwa

- Product owner: Tristan Israël (tristan.israel@tibsys.com)
- Document file name: README.md
- Document owner: Tristan Israël (tristan.israel@tibsys.com)
- Document version: 1.0 2017-12-28

########

Achiwa is runnable on macOs, Windows and GNU/Linux (Debian like distributions).

It sniffes all network data (using libpcap) and identifies new devices. Identification process is done using multiple algorithms: MAC address, OS recognition, software recognition, intrusion tests, CIFS/SMB protocol, and others.

When a new device is identified, it is presented to the user (OS, device name, device type, user names, others). The user can set it as a friend device or in the black hole.

When put in the black hole, Achiwa sends multiple requests to make the device fail (fake router MAC address, exploits, others) and force the intruder to leave.

The main goal is to help the user monitor its network and make it more secure: when a new device is detected Achiwa is going to give him information on how its network's security could be improved.

There are tools included which aim at helping the user diagnose its own computer security.

#####

Current situation:
- Software is in version 2.4.x
- Developed using C++, Qt5, boost (2 .hpp files) and openssl (not for long)
- Not maintained by initial company (tibSys SARL)
- Around 6 000 users
- Packaged for macOS 10.9+, Windows XP+, GNU/Linux debian style distrib
- Bugs to be fixed but works quite well
- Improvements to be done
- Bug tracker available (MantisBT)

Target:
- Free the software (no more licence management)
- Redirect software update management to another location (initial service is down)
- The same for crash reporter
- Make improvements (see below)
- Make fixes (see BT)

Improvements:
- Software architecture
- Optimize classes
- Intrusion detection 
- Devices recognition (algorithms, databases)
- System integration (Deprecated APIs on macOS, Windows new APIs for networking and network filtering)
- Network traffic analysis (libpcap / new driver ?)
- Create a Windows 10 Metro GUI

Dependencies:
- boost (functions.hpp and tribool.hpp)
- openssl
- QAppUpdater (see github.com/tibsys/qappupdater)
- libpcap (http://www.tcpdump.org/)

Compilation environments:
- Qt 5.4+
- macOs: XCode and clang
- GNU/Linux: gcc and stdlib
- Windows: Visual C++ 2012+ with SDK 7.1+ (not mingw because of missing libraries for networking)

Steps:
- [TBD] Provide my full source code to improve this software and make it available freely for all people. I need to clean it a bit before.
- [TBD] Write a specifications book on the existing (v2)
- [TBD] Create a team
- [TBD] Write a new specifications book (v3)
- [TBD] Comment all source files
- [TBD] Identify problems in the current architecture
- [TBD] Start coding v3

