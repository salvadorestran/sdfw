# sdfw
## **A Distributed and Software-Defined Firewall based on *OpenFlow***

This repository aims to implement a Proof of Concept (PoC) that shows how to prevent the propagation of malware into corporate networks, by means of Software-Defined Networking based on *OpenFlow*.

### **Abstract**
As you will surely know, many of the last ransomware attacks, such as *Wannacry* and others, spread leveraging a vulnerability in SMB protocol, which can let an intruder inject shellcode into vulnerable Windows systems using the *EternalBlue* exploit.

The malware code is capable of searching vulnerable machines by their IP address in the LAN and attempting exploitation via SMB port 445.

This way, the traditional approach to protect the machines in a corporate LAN consists of installing the proper operating system patches and updating the antivirus software in order to close any vulnerable TCP or UDP port.

In this PoC it will be demonstrated how easy and efficient is to employ another approach based on the installation of a Firewall on every and each of the switches in the corporate LAN.

The PoC is based on the following key components:

1. OpenFlow 1.3 compliant switches, which will be supplied by [*Open vSwitch*](http://openvswitch.org/).

2. [*FAUCET*](https://github.com/salvadorestran), an OpenFlow controller for multi table OpenFlow 1.3 switches, that implements layer 2 switching, VLANs, ACLs, and layer 3 IPv4 and IPv6 routing.

3. [*Mininet*](http://mininet.org/), a tool that creates a virtual network over Linux, running real kernel, switch and application code, on a single machine (VM, cloud or native), in seconds.

#### Table of Contents:

- [Requirements](https://github.com/salvadorestran/sdfw#requirements)
- [Installation](https://github.com/salvadorestran/sdfw#installation)
- [Scenarios](https://github.com/salvadorestran/sdfw#scenarios)
- [Use cases](https://github.com/salvadorestran/sdfw#use-cases)

### **Requirements**

- Any machine with x86 type processor (Intel/AMD/etc.) and Virtualization Technology enabled
- At least 2GB RAM and 10GB of free Hard Disk space
- Any Debian Linux installed such as Ubuntu 16.04.3 LTS or similar
- VNX installed [(VNX Installation Guide)](http://web.dit.upm.es/vnxwiki/index.php/Vnx-install-ubuntu3)
- [Mininet](http://mininet.org/download/) installed into a VM (recommended)
- [*Ryu* SDN controller](https://github.com/osrg/ryu) installed
- [nodejs](https://nodejs.org/en/) and [npm](https://www.npmjs.com/) installed **in the same machine where *Ryu* will be ran**

### **Installation**
See [`INSTALL.md`](https://github.com/salvadorestran/sdfw/blob/master/INSTALL.md) for installation instructions and details.

### **Scenarios**
See [`SCENARIOS.md`](https://github.com/salvadorestran/sdfw/blob/master/SCENARIOS.md) for simulation options and running instructions.

### **Use cases**
See [`USE_CASES.md`](https://github.com/salvadorestran/sdfw/blob/master/USE_CASES.md) for firewall set-up and test instructions.
