 🧠 Packet Tracer - Configure a Wireless Router and Clients

 📘 Project Overview

This project simulates a real-world **home network setup** using **Cisco Packet Tracer**.
The goal is to help a homeowner (Natsumi) connect her home devices — PCs, a laptop, and a television — to the internet through a cable modem and a wireless router.

The lab demonstrates essential networking skills including:

* Connecting devices with correct cabling.
* Configuring a home wireless router.
* Setting up DHCP and IP addressing.
* Enabling secure Wi-Fi.
* Testing end-to-end connectivity.

---

## 🎯 Objectives

1. **Part 1:** Connect all physical and logical devices.
2. **Part 2:** Configure the home wireless router.
3. **Part 3:** Configure IP addressing for all hosts and test network connectivity.

---

## 🏠 Network Topology

**Devices Used:**

* Cable Splitter
* Cable Modem
* Home Wireless Router (with built-in switch and access point)
* Office PC (wired)
* Bedroom PC (wired)
* Laptop (wireless)
* Television (coaxial connection)

**Connections:**

* Coaxial: Cable Splitter → Modem & TV
* Ethernet (Straight-Through):

  * Modem → Router Internet Port
  * Router GigabitEthernet1 → Office PC
  * Router GigabitEthernet2 → Bedroom PC
* Wireless (2.4 GHz): Laptop → Router (SSID: **MyHome**)

---

## ⚙️ Configuration Steps

### 🧩 Part 1: Connect the Devices

1. **Connect Coaxial Cables**

   * Coaxial1 → Cable Modem (Port 0)
   * Coaxial2 → Television (Port 0)
   * Verify TV connection by turning it ON (TV program appears).

2. **Connect Ethernet Cables**

   * Cable Modem (Port 1) → Router (Internet Port)
   * Office PC (FastEthernet0) → Router (GigabitEthernet1)
   * Bedroom PC (FastEthernet0) → Router (GigabitEthernet2)

---

### 🖥️ Part 2: Configure the Wireless Router

1. **Access Router GUI**

   * On Office PC → `Desktop > IP Configuration > DHCP`
   * Open Web Browser → Enter **Default Gateway IP (Router IP)**
   * Login credentials: `admin / admin`

2. **Set Basic Configuration**

   * Change **Maximum Number of Users** (DHCP) to `10`.
   * Save Settings.
   * Change **Admin Password**: `MyPassword1!`

3. **Configure Wireless Network**

   * Enable **2.4 GHz Network**.
   * Set **SSID:** `MyHome`
   * Security: **WPA2 Personal**
   * Passphrase: `MyPassPhrase1!`
   * Save and apply settings.

---

### 💻 Part 3: Configure Clients and Test Connectivity

1. **Laptop (Wireless Connection)**

   * Go to `Desktop > PC Wireless > Connect`
   * Select SSID: `MyHome`
   * Enter Passphrase: `MyPassPhrase1!`
   * Obtain IP via DHCP (should start with 192.168.x.x)
   * Verify connectivity: Open Web Browser → `skillsforall.srv`

2. **Office PC (Wired Connection)**

   * Already connected to router.
   * Test connectivity: Web Browser → `skillsforall.srv`

3. **Bedroom PC (Wired Connection)**

   * Configure DHCP in IP Configuration.
   * Test connectivity: Web Browser → `skillsforall.srv`

---

## 🚧 Problems Encountered & Solutions

| **Problem**                                | **Cause**                                     | **Solution**                                                                                      |
| ------------------------------------------ | --------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **TV not displaying any program**          | Incorrect coaxial connection                  | Reconnected Coaxial1 to Cable Modem and Coaxial2 to TV. Turned ON TV to verify.                   |
| **Office PC not getting IP address**       | DHCP delay in Packet Tracer simulation        | Used **Fast Forward Time** to speed up DHCP process.                                              |
| **Router GUI inaccessible**                | Office PC not receiving gateway address       | Toggled between **DHCP** and **Static** to refresh configuration.                                 |
| **Wireless network not visible on Laptop** | Wireless interface disabled or SSID not saved | Enabled 2.4 GHz network and re-saved **SSID: MyHome** in router settings.                         |
| **Laptop connected but no internet**       | DHCP lease delay                              | Used **Fast Forward Time** multiple times to obtain valid IP and establish internet connectivity. |
| **Login lost after saving settings**       | Router reboots after admin password change    | Re-authenticated using new credentials: `admin / MyPassword1!`.                                   |

---

## ✅ Verification

All devices successfully connected to the internet and communicated with each other:

* **Office PC:** Internet access ✅
* **Bedroom PC:** Internet access ✅
* **Laptop (Wireless):** Internet access ✅
* **Television:** Video service functional ✅

---

## 🔒 Security Configuration Summary

| Setting           | Value            |
| ----------------- | ---------------- |
| SSID              | `MyHome`         |
| Wireless Security | WPA2 Personal    |
| Passphrase        | `MyPassPhrase1!` |
| Admin Password    | `MyPassword1!`   |
| DHCP Max Users    | 10               |

---

## 📁 Repository Structure

```
PacketTracer_WirelessRouter_Configuration/
├── PacketTracer_WirelessRouter_Configuration.pkt   # Cisco Packet Tracer file
├── README.md                                       # Project documentation (this file)
└── screenshots/                                    # (Optional) screenshots of setup
```

---

## 🧩 Skills Demonstrated

* Network topology design in Cisco Packet Tracer
* DHCP configuration and IP addressing
* Router GUI management and password hardening
* Wireless LAN setup with WPA2 security
* Troubleshooting network connectivity

---

## 💡 Lessons Learned

* Importance of **correct cabling** and **interface selection** in physical topology.
* How **DHCP automation** simplifies client configuration.
* The role of default gateway in enabling external communication.
* How to secure wireless networks using WPA2 encryption.
* Importance of saving settings after each configuration step.

---

👩‍💻 Author

Name: Abdulmalik Hamza
Course: Networking Fundamentals / Cisco Packet Tracer Lab
Date: October 2025

---

📜 License

This project is open-source and available under the [MIT License](LICENSE).
Feel free to fork, modify, and experiment for educational purposes.

---


