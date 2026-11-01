<div align="center">

# 🔐 Kali Linux Lab Setup

### NETWORKWALKS · CYBERSECURITY INTERNSHIP · WEEK 01

**Building my cybersecurity foundation, one lab at a time.**

A documented setup of my Kali Linux virtual machine using VMware Workstation Pro on Windows.

<br>

![Kali Linux](https://img.shields.io/badge/OS-Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Virtualization](https://img.shields.io/badge/Virtualization-VMware-607078?style=for-the-badge&logo=vmware&logoColor=white)
![Host OS](https://img.shields.io/badge/Host-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-2EA44F?style=for-the-badge)

</div>

---

## 📌 Table of Contents

- [🎯 Project Overview](#-project-overview)
- [🛠️ Lab Environment](#️-lab-environment)
- [⚙️ Network Configuration](#️-network-configuration)
- [🚀 Setup Process](#-setup-process)
- [🌐 Internet Connectivity Test](#-internet-connectivity-test)
- [📸 Screenshots](#-screenshots)
- [✅ Week 1 Checklist](#-week-1-checklist)
- [📚 Key Learnings](#-key-learnings)
- [👩‍💻 Author](#-author)

---

## 🎯 Project Overview

The objective of this task was to set up and run a functional **Kali Linux virtual machine** as the foundation for hands-on cybersecurity learning.

I downloaded the prebuilt Kali Linux VMware image from the official Kali Linux website, imported it into VMware Workstation Pro, and verified that the virtual machine boots successfully and has internet connectivity.

### Objectives

- Set up Kali Linux in a virtualized environment.
- Configure the virtual machine's network adapter.
- Verify the assigned IP address and network configuration.
- Test internet connectivity from inside Kali Linux.
- Document the setup with screenshots.

---

## 🛠️ Lab Environment

| Component | Configuration |
|:--|:--|
| **Name** | Ayesha Kazi |
| **Program** | Networkwalks Cybersecurity Internship |
| **Task** | Week 1 — Kali Linux Lab Setup |
| **Host Operating System** | Windows |
| **Virtualization Software** | VMware Workstation Pro |
| **Guest Operating System** | Kali Linux |
| **Installation Method** | Prebuilt VMware image |
| **Desktop Environment** | GNOME |
| **Network Adapter Mode** | Bridged |
| **Kali Linux IPv4 Address** | `192.168.29.204/24` |
| **Internet Connectivity** | Working |

> **Note:** The IP address shown above is the address assigned to my Kali Linux virtual machine during this setup. It may change depending on the network and DHCP configuration.

---

## ⚙️ Network Configuration

The Kali Linux virtual machine uses **Bridged networking** in VMware Workstation Pro.

In this mode, the virtual machine connects to the network through the host computer's network adapter and typically receives its own IP address from the network's DHCP server.

### Configuration Details

| Setting | Value |
|:--|:--|
| Network Adapter | Bridged |
| IPv4 Address | `192.168.29.204/24` |
| Connectivity | Verified |

### Check the IP Address

Open the Kali Linux terminal and execute:

```bash
ip addr
```

Locate the active network interface and check its IPv4 address.

To inspect the routing configuration, use:

```bash
ip route
```

---

## 🚀 Setup Process

### Step 1 — Download Kali Linux

Downloaded the prebuilt VMware image from the official Kali Linux website.

🔗 **Official download page:** https://www.kali.org/get-kali/#kali-virtual-machines

### Step 2 — Extract the Image

Extracted the downloaded `.7z` archive to access the virtual machine files.

### Step 3 — Open VMware Workstation Pro

Opened the extracted virtual machine in VMware Workstation Pro.

### Step 4 — Boot Kali Linux

Started the virtual machine and confirmed that Kali Linux booted successfully into the GNOME desktop environment.

### Step 5 — Configure Networking

Selected **Bridged** mode for the virtual machine's network adapter.

### Step 6 — Verify Network Connectivity

Checked the assigned IPv4 address and tested connectivity using the `ping` command.

---

## 🌐 Internet Connectivity Test

To verify connectivity from Kali Linux, open the terminal and run:

```bash
ping -c 4 8.8.8.8
```

This sends four ICMP echo requests to Google's public DNS server at `8.8.8.8`.

### Expected Result

Successful connectivity typically produces replies similar to:

```text
64 bytes from 8.8.8.8: icmp_seq=1 ttl=... time=... ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=... time=... ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=... time=... ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=... time=... ms
```

The exact TTL and response times may vary.

**Interpretation:** Replies indicate that the machine can reach the target using ICMP. If no replies are received, ICMP traffic may be blocked by the network or another configuration issue.

> **Additional note:** Pinging an IP address tests IP connectivity, not DNS resolution. To test both connectivity and DNS, you can additionally run:
>
> ```bash
> ping -c 4 google.com
> ```

---

## 📸 Screenshots

Screenshots documenting the actual setup should be added to the repository's `screenshots/` folder.

| Screenshot | Description |
|:--|:--|
| `01-kali-desktop.png` | Kali Linux running in VMware Workstation Pro |
| `02-vm-settings.png` | Virtual machine hardware settings |
| `03-network-adapter.png` | Network adapter configured to Bridged |
| `04-ip-address.png` | Terminal output showing the assigned IPv4 address |
| `05-connectivity-test.png` | Terminal output from `ping -c 4 8.8.8.8` |
| `06-internet-browser.png` | A website opened inside Kali Linux |

### 🖼️ Lab Preview

Once the screenshots have been uploaded to your repository, you can display them here.

**Kali Linux Desktop**

![Kali Linux Desktop](screenshots/01-kali-desktop.png)

**Network Configuration**

![VMware Network Adapter](screenshots/03-network-adapter.png)

**IP Address Verification**

![Kali Linux IP Address](screenshots/04-ip-address.png)

**Internet Connectivity**

![Ping Connectivity Test](screenshots/05-connectivity-test.png)

> **Important:** These image paths will display correctly only after you upload the corresponding screenshots to the `screenshots/` folder. Use screenshots captured from your own setup; do not represent placeholder images as completed evidence.

---

## ✅ Week 1 Checklist

- [x] Downloaded the prebuilt Kali Linux VMware image.
- [x] Extracted the virtual machine files.
- [x] Opened the virtual machine in VMware Workstation Pro.
- [x] Booted Kali Linux successfully.
- [x] Accessed the GNOME desktop environment.
- [x] Configured the network adapter in Bridged mode.
- [x] Verified the assigned IPv4 address.
- [x] Checked the network routing configuration.
- [x] Tested IP connectivity using `ping`.
- [x] Documented the lab setup for the internship.

---

## 📚 Key Learnings

Through this setup, I gained practical familiarity with:

- **Virtualization:** Running a Linux operating system inside a virtual machine.
- **Kali Linux:** Accessing a Linux environment for cybersecurity learning.
- **Network adapters:** Understanding Bridged networking in VMware.
- **IP addressing:** Identifying the virtual machine's assigned IPv4 address.
- **Network diagnostics:** Using `ip addr`, `ip route`, and `ping` to inspect and troubleshoot connectivity.
- **Technical documentation:** Recording the lab configuration and verification process in GitHub.

---

## 👩‍💻 Author

**Ayesha Kazi**

Cybersecurity Intern · Networkwalks

*Week 1 — Kali Linux Lab Setup*

---

<div align="center">

**🔐 Learn · Practice · Document · Improve**

*Building a strong foundation in cybersecurity.*

</div>