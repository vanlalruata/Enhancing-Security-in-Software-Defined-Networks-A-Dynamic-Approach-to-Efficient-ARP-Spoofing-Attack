
The ARP Spoofing mitigation module is integrated into the POX SDN controller, aiming to enhance network security by preventing LAN attackers from poisoning cache table entries of nodes. This module operates with minimal overhead and efficiently blocks malicious packets from infiltrating the network.

## Key Features
* Prevention of Cache Table Poisoning: The module effectively prevents LAN attackers from corrupting cache table entries of nodes within the network. It achieves this goal with minimal computational overhead, ensuring optimal performance.
* Blocking Malicious Packets: The module acts as a robust barrier, intercepting and blocking malicious packets from entering the network infrastructure. By identifying and isolating these packets, it maintains the integrity of the network and protects against potential security breaches.

## Setup Components
* ARPspoofperf.py: This script creates the test setup, incorporating the detection module for ARP spoofing mitigation.
* ARPspoofperfwithoutsol.py: This script establishes the test setup without the detection module, serving as a comparative scenario.
* l2_learning_arp_mitigation.py: This script contains the ARP mitigation module integrated into the POX controller. It forms the core component of the solution, enabling real-time detection and prevention of ARP spoofing attacks.

## How to Execute
### To run the system, follow these steps:

* Initiate the POX controller with the ARP mitigation module using the following command:

./pox.py log.level --DEBUG proto.dhcpd --network=10.1.1.0/24 --ip=10.1.1.1 forwarding.l2_learning_arp_mitigation

* This command initializes the controller, configuring it to operate with the specified network parameters and activating the ARP mitigation capabilities.

* Launch the network topology simulation with the following command:

sudo mn --mac --controller remote --topo=single,3

* This command sets up the network topology, incorporating the specified MAC addresses and controller configuration. The network will consist of a single topology with three nodes, allowing for comprehensive testing and evaluation of the ARP Spoofing mitigation module's effectiveness.

* By adhering to these instructions, users can assess the performance and reliability of the ARP Spoofing mitigation module within the specified network environment.
