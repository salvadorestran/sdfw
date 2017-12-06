# sdfw
A Distributed and Software-Defined Firewall based on OpenFlow

As you will surely know, many of the last ransomware attacks, such as Wannacry and others, spread leveraging a vulnerability in SMB protocol, which can let an intruder inject shellcode into vulnerable Windows systems using the EternalBlue exploit.

The malware code is capable of searchig vulnerable machines by their IP address in the LAN and attempting exploitation via SMB port 445.

This way, the traditional approach to protect the machines in a corporate LAN consists of installing the proper operating system patches and updating the antivirus sofware in order to close any vulnerable TCP or UDP port.

In this Proof of Concept (PoC) I will demonstrate how easy and efficient is to employ another approach based on a distributed Firewall on every and each of the switches in the corporate LAN.

The PoC is based on the following key components:
1.- a set of OpenFLow compliant switches, which will be simulated with Open vSwitch
2.- an OpenFlow controller with the firewall application running on it, which will be the Ryu controller and its available Firewall app
3.- a web Frontend application, which will be developed in order to let an administrator manage the distributed firewall by means the REST API provided by Ryu

(to be continued...)
