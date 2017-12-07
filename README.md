# sdfw
## **A Distributed and Software-Defined Firewall based on *OpenFlow***

As you will surely know, many of the last ransomware attacks, such as *Wannacry* and others, spread leveraging a vulnerability in SMB protocol, which can let an intruder inject shellcode into vulnerable Windows systems using the *EternalBlue* exploit.

The malware code is capable of searching vulnerable machines by their IP address in the LAN and attempting exploitation via SMB port 445.

This way, the traditional approach to protect the machines in a corporate LAN consists of installing the proper operating system patches and updating the antivirus software in order to close any vulnerable TCP or UDP port.

In this Proof of Concept (PoC) I will demonstrate how easy and efficient is to employ another approach based on the installation of a Firewall on every and each of the switches in the corporate LAN.

The PoC is based on the following key components:

1. a set of OpenFlow compliant switches, which will be simulated with [*Open vSwitch*](http://openvswitch.org/)

2. an OpenFlow controller with the firewall application running on it, which will be the [*Ryu*](https://github.com/osrg/ryu) controller and its available Firewall app

3. a *Front-end* web application, which **will be developed** in order to let an administrator manage the distributed firewall easily by means the REST API provided by Ryu

(to be continued...)
