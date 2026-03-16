# CCNA-TWO-NETWORK-ROUTING
## Overview

This project demonstrates how a router connects two different networks so devices in each network can communicate.

## Topology

Devices used:

* 1 Router
* 2 Switches
* 2 PCs

Network Layout:

PC1 — Switch1 — Router — Switch2 — PC2

## IP Addressing

| Device      | IP Address   | Subnet Mask   | Gateway     |
| ----------- | ------------ | ------------- | ----------- |
| Router G0/0 | 192.168.1.1  | 255.255.255.0 | -           |
| Router G0/1 | 192.168.2.1  | 255.255.255.0 | -           |
| PC1         | 192.168.1.10 | 255.255.255.0 | 192.168.1.1 |
| PC2         | 192.168.2.10 | 255.255.255.0 | 192.168.2.1 |

## Router Configuration

enable
configure terminal

interface g0/0
ip address 192.168.1.1 255.255.255.0
no shutdown

interface g0/1
ip address 192.168.2.1 255.255.255.0
no shutdown

end
write memory

## Verification

Test connectivity from PC1:

ping 192.168.2.10

If configuration is correct, PC1 should successfully reach PC2.

## Skills Demonstrated

* Router interface configuration
* Connecting multiple networks
* IPv4 addressing
* Basic connectivity testing

## Files Included

* project2.pkt
* topology.png
* router-config.txt
* README.md

<img width="649" height="517" alt="Topology" src="https://github.com/user-attachments/assets/5021baa5-8b47-4c76-8da2-698861aaf8ea" />
<img width="803" height="684" alt="CMD ip route" src="https://github.com/user-attachments/assets/67c4adf6-3744-4137-9b14-910791c0c1a6" />
<img width="861" height="685" alt="running config" src="https://github.com/user-attachments/assets/23a611c8-e70e-484e-b29d-3da1c3c05229" />
