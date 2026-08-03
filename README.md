# Linux Enumeration & Privilege Escalation Cheatsheet

![Linux](https://img.shields.io/badge/Linux-Enumeration-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Status](https://img.shields.io/badge/Status-In%20Progress-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

---

## 📖 Overview

This repository is my personal Linux Enumeration and Privilege Escalation Cheatsheet built while studying Penetration Testing.

The goal is to document useful commands, tools, methodologies, and privilege escalation techniques that can be used during Linux security assessments and Capture The Flag (CTF) challenges.

This cheatsheet will continue to grow as I complete more TryHackMe rooms, home labs, and penetration testing exercises.

---

## 🎯 Objectives

- Learn Linux Enumeration
- Learn Privilege Escalation
- Document useful commands
- Build a professional reference guide
- Improve penetration testing workflow

---

## 📂 Repository Structure

```
linux-enumeration-cheatsheet/

├── README.md
├── screenshots/
├── scripts/
├── wordlists/
└── resources/
```

---

## 📚 Topics Covered

- System Enumeration
- User Enumeration
- Network Enumeration
- Process Enumeration
- Service Enumeration
- File Enumeration
- SUID & SGID
- Capabilities
- Cron Jobs
- PATH Hijacking
- Writable Files
- Docker Enumeration
- NFS Enumeration
- Kernel Exploits
- Useful Tools

---

# 🖥 System Enumeration

## Kernel Version

```bash
uname -a
```

Displays the Linux kernel version and system architecture.

---

## Hostname

```bash
hostname
```

Displays the hostname of the target machine.

---

## Distribution Information

```bash
cat /etc/os-release
```

Displays operating system information.

---

## CPU Information

```bash
lscpu
```

Displays CPU details.

---

## Mounted Drives

```bash
mount
```

Displays mounted file systems.

---

## Disk Usage

```bash
df -h
```

Displays available disk space.

---

## Environment Variables

```bash
env
```

Displays current environment variables.

---

## 🛠 Tools

- linPEAS
- pspy
- Linux Exploit Suggester
- GTFOBins
- Nmap
- Netcat

---

# 🖥️ Linux Enumeration

Enumeration is the most important phase of a penetration test. Before attempting exploitation or privilege escalation, gather as much information about the target system as possible.

---

# 📍 System Information

## Kernel Version

```bash
uname -a
```

Displays kernel version, architecture, hostname, and build information.

---

## Operating System

```bash
cat /etc/os-release
```

Shows Linux distribution information.

Alternative:

```bash
cat /etc/issue
```

---

## Hostname

```bash
hostname
```

Displays the machine hostname.

---

## Current User

```bash
whoami
```

Displays the current logged-in user.

---

## User ID

```bash
id
```

Shows:

- UID
- GID
- Groups

Example:

```bash
uid=1000(karen) gid=1000(karen) groups=1000(karen),27(sudo)
```

If the user belongs to the **sudo** group, privilege escalation may be possible.

---

## Logged In Users

```bash
who
```

Displays currently logged-in users.

---

## Last Login

```bash
last
```

Shows login history.

---

# 💾 Hardware Information

## CPU

```bash
lscpu
```

Displays CPU architecture and details.

---

## Memory

```bash
free -h
```

Shows RAM usage.

---

## Disk Usage

```bash
df -h
```

Shows mounted disks and available storage.

---

## Mounted Drives

```bash
mount
```

Lists mounted file systems.

---

# 🌐 Network Enumeration

## Interfaces

```bash
ip a
```

or

```bash
ifconfig
```

Displays network interfaces.

---

## Routing Table

```bash
ip route
```

Shows routing information.

---

## ARP Table

```bash
arp -a
```

Displays neighboring devices.

---

## Listening Ports

```bash
ss -tuln
```

or

```bash
netstat -tuln
```

Lists listening services.

---

## DNS Configuration

```bash
cat /etc/resolv.conf
```

Displays configured DNS servers.

---

## Hosts File

```bash
cat /etc/hosts
```

Shows local hostname mappings.

---

## 📌 Status

🚧 Currently being updated as I progress through TryHackMe and home lab exercises.

---

## 📜 License

MIT License
