# Google Summer of Code 2020 - OWASP (Final Submission)

## Table of Contents

- [Overview](#overview)
    - [About me](#about-me)
    - [Project details](#project-details)
    - [Proposed summary](#proposed-summary)
    - [Work done](#work-done)
    - [Over Timeline](#timeline)

- [Screenshots screenscasts and tutorial videos](#screenshots-screenscasts-and-tutorial-videos)

## Overview

### About Me

- **Name:** Kushal Majmundar
- **Major:** Computer Science & Engineering
- **University:** International Institute of Information technology, Hyderabad
- **GitHub:** [@kUSHAL0601](https://github.com/kUSHAL0601)
- **E-mail:** majmundarkushal9@gmail.com
- **Project URL:** https://www.github.com/OWASP/SecureTea-Project<br>

### Project details

The OWASP SecureTea Project focuses on providing a one-stop security solution for various devices (personal computers / servers / IoT devices).

Currently the following features are supported:

- [x] Intrusion Detection System
- [x] Firewall
- [x] AntiVirus
- [x] Server Log Monitor
- [x] System Log Monitor
- [x] Local Web Deface Detection & Prevention System
- [x] Auto Web Server Patcher
- [x] IoT Anonymity checker
- [x] Auto report generation using OSINT
- [x] Notifying suspicious activities using various mediums (Twitter, Telegram, Slack, Gmail, SMS, AWS & more)
- [x] Interactive GUI for ease of setting up
- [x] History Logger
- [x] GUI with authentication for Enterprise networks
- [x] Social Engineering
- [x] Eligibility traces based method for automatic blacklisting of ip addresses



**Organisation:** OWASP Foundation<br>
**Project URL:** https://www.github.com/OWASP/SecureTea-Project<br>
**IRC channel:** https://t.me/joinchat/Az5yZxQg7Djs-UZWKKCRVQ<br>
**Mentor:** Rejah Rehim [(@rejahrehim)](https://github.com/rejahrehim), Ade Yoseman Putra[@adeyosemanputra](https://github.com/adeyosemanputra)<br>
**Proposal Title:** SecureTea<br>
**Tag:** securetea tools<br>

### Proposed summary

**Proposed summary as per proposal**:

One of my primary goals is to make securetea an industrially usable product. The major topics I am targeting are:

1.  Updating GUI
2.  Improving IDS
3.  Login module --> Server side and Client side builds
4.  Deface detection using ML
5.  History Logger
6.  Fix issues and bugs throughout

### Work done

**Summary of the work done during the GSoC Phase (I - III):**

- [Installation script](https://github.com/OWASP/SecureTea-Project/pull/253):
    - Fixed installation issues over various operating systems
    - Encapsulated it into two scripts, one for apt based system and other for rpm based systems.
    - Tested on ubuntu-16.04, ubuntu-20.04, Fedora 32, CentOS7, ParrotSec-4.6, Kali-Linux 2016, Kali Linux 2018

- [History Logger](https://github.com/OWASP/SecureTea-Project/pull/254):
    - A system logger to log every command run on the terminal
    - Can help to recover at a later point
    - Logging using inbuilt rsyslog

- [GUI Updates](https://github.com/OWASP/SecureTea-Project/pull/256):
    - Get security applet work using gui. Initially it was not in a working state making the gui of no use.
    - Introduce login module to gui
    - Introduce real-time notifications of SecureTea app to gui by connecting socket of Flask to Angular
    - Save user's choice of configuration
    - Introduced history logger to gui
    - Added cli args to skip reading from config file as well as skip taking input
    - Fixed error with geocode

- [Web deface detection using set difference](https://github.com/OWASP/SecureTea-Project/pull/257):
    - Web deface detection was based on hash initially. Introduce set to know what content is actually being changed.

- [Eligibility Traces](https://github.com/OWASP/SecureTea-Project/pull/258):
    - Added options to use custom scanners from clamav, yara and virus_total
    - Added eligibility traces(Reinforcement Learning) in IDS to make it a semi-IPS i.e. blacklisting frequent offenders
    - You can read more about eligibility traces [here](http://www.incompleteideas.net/book/ebook/node72.html)

- [Bump dependencies, Bug fixes](https://github.com/OWASP/SecureTea-Project/pull/259):
    - Updated angular dependencies to avoid security risks in those modules
    - Added rsyslog to installation script, modifies history logger to work on all OS
    - Dependecies for server app resolved

- [Social Engineering](https://github.com/OWASP/SecureTea-Project/pull/260):
    - Introduced social engineering as a module
    - Gives the credability of an email address using [emailrep.io](https://emailrep.io/)

- [Fix pip install, test case](https://github.com/OWASP/SecureTea-Project/pull/262):
    - Updated requirements.txt for pip install
    - Fixed test case based on updated code

- [Fix build](https://github.com/OWASP/SecureTea-Project/pull/264):
    - Fixed failing build because of order of logging

- [Continious Integration](https://github.com/OWASP/SecureTea-Project/pull/265):
    - Introduced CI using github action
    - Makes a new tag called pre-release and updates it on every push
    - Travis-CI is configured to then roll these changes to pip

### Timeline
|Date            |Type        |Status|ID  |Name                                                                                                   |
|----------------|------------|------|----|-------------------------------------------------------------------------------------------------------|
|**Phase-1**        |            |      |    |                                                                                                       |
|25.06.2020      |PR       |Merged|[#253](https://github.com/OWASP/SecureTea-Project/pull/253) |Scripts to install dependencies                                                                                  |
|25.06.2020      |PR       |Merged|[#254](https://github.com/OWASP/SecureTea-Project/pull/254) |History Logger                                                                                  |
|**Phase-2**        |            |      |    |                                                                                                       |
|11.07.2020      |PR       |Merged|[#256](https://github.com/OWASP/SecureTea-Project/pull/256) |Gui Updates                                                                                  |
|11.07.2020      |PR       |Merged|[#257](https://github.com/OWASP/SecureTea-Project/pull/257) |Web deface set                                                                                  |
|24.07.2020      |PR       |Merged|[#258](https://github.com/OWASP/SecureTea-Project/pull/258) |Eligibility Traces                                                                                  |
|28.07.2020      |PR       |Merged|[#259](https://github.com/OWASP/SecureTea-Project/pull/259) |Bug Fixes                                                                                  |
|**Phase-3**        |            |      |    |                                                                                                       |
|20.08.2020      |PR       |Merged|[#260](https://github.com/OWASP/SecureTea-Project/pull/260) |Social Engineering, Bug Fixes, Documentation                                                                                  |
|24.08.2020      |PR       |Merged|[#262](https://github.com/OWASP/SecureTea-Project/pull/262) |Fixing failed test case, pip install                                                                                  |
|24.08.2020      |PR       |Merged|[#264](https://github.com/OWASP/SecureTea-Project/pull/264) |Fixing Build                                                                                  |
|24.08.2020      |PR       |Merged|[#265](https://github.com/OWASP/SecureTea-Project/pull/265) |Added github action                                                                                  |

### Commits
View list of commits [here](https://github.com/OWASP/SecureTea-Project/commits?author=kUSHAL0601).

### Contribution graph and status

**Commits:**

![graph](https://i.ibb.co/M6YjVPM/Contri-Comm.png)

**Contribution to OWASP:**

![graph](https://i.ibb.co/1v3HK7J/Contri-Graph.png)

## Screenshots screenscasts and tutorial videos

**Angular JS GUI dashboard**

![Notifications](https://user-images.githubusercontent.com/29600964/86742417-bc2c6280-c055-11ea-92a9-c14731cf86a8.png)


**Videos**

[SecureTea Installation over various OS](https://drive.google.com/drive/folders/1ll-53cm-LXHcLmBkjsGBERDSUaUrA2Qe?usp=sharing)
