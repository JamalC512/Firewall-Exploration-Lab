# Firewall Exploration Lab

## Project Overview

The Firewall Exploration Lab was a hands-on network security project where I explored how Linux firewalls inspect, filter, and control network traffic. The lab gave me experience working with firewall rules at both the Linux kernel level using Netfilter and through the command line using iptables.

I completed the project in a controlled Linux and Docker environment where I could generate different types of network traffic, apply firewall rules, and observe how those rules affected communication between systems.

Instead of only learning what a firewall does, this project allowed me to see how packets are processed and how specific rules can allow, block, or limit network communication.

## Lab Environment

The lab used Linux systems and Docker containers to create an isolated network environment. The containers allowed me to generate and test different types of traffic without affecting an outside network.

Some of the main technologies and tools used during the lab included:

- Linux
- Docker
- Netfilter
- iptables
- Linux Kernel Modules
- dmesg
- conntrack
- TCP/IP
- DNS
- ICMP

The environment allowed me to create firewall rules and then test whether traffic was successfully accepted, dropped, or limited.

## Working with Netfilter

One of the main parts of the lab involved working with Netfilter, which is part of the Linux networking system and provides the framework used to inspect and manipulate network packets.

I worked with a Linux kernel module that interacted with Netfilter to intercept network traffic as packets moved through the system.

This gave me a better understanding of how firewall filtering can happen at a lower level of the operating system instead of only through a graphical firewall application.

I was able to examine different types of traffic, including:

- TCP
- UDP
- ICMP
- DNS

Working with these protocols helped me understand that firewall behavior can be different depending on the type of traffic being inspected.

## Packet Inspection and Protocol Logging

Another part of the project involved examining information contained inside network packets.

The firewall module was used to identify and log information about different protocols. This allowed me to observe the traffic being processed and better understand how a firewall determines what type of packet it is handling.

I worked with TCP, UDP, and ICMP traffic and also examined DNS communication.

This part of the project strengthened my understanding of how information contained in network and transport layer headers can be used when creating firewall policies.

## Working with iptables

I also used iptables to create and test firewall rules from the Linux command line.

I worked with the major iptables chains:

- INPUT
- OUTPUT
- FORWARD

The INPUT chain allowed me to work with traffic being sent to the system, while the OUTPUT chain dealt with traffic leaving the system. The FORWARD chain was used when traffic needed to pass through a system on its way to another destination.

Working with these different chains helped me understand that firewall rules have to be placed in the correct location depending on the direction that traffic is traveling.

## Testing Firewall Rules

After creating firewall rules, I generated network traffic to determine whether the rules were working correctly.

I tested different types of communication, including ping traffic, DNS requests, and TCP connections.

By changing firewall rules and repeating the tests, I could compare the results and determine whether specific traffic was being accepted or blocked.

This helped me understand the importance of testing firewall configurations instead of assuming that a rule is working correctly after it is created.

## DNS Traffic Filtering

The lab also included working with DNS traffic.

DNS is important because systems use it to translate domain names into IP addresses. I examined how firewall rules could affect DNS requests and how blocking the necessary DNS traffic could prevent a system from resolving domain names even when other network connectivity was still available.

This helped demonstrate how firewall configurations can affect individual network services without completely disconnecting a system from the network.

## Stateless Packet Filtering

I explored stateless packet filtering, where packets are evaluated mainly based on the information contained in each individual packet.

This can include information such as:

- Source IP address
- Destination IP address
- Protocol
- Source port
- Destination port

Working with stateless filtering helped me understand how basic firewall rules can make decisions without keeping track of the full connection between two systems.

## Stateful Packet Filtering

The lab also introduced stateful packet filtering.

Unlike stateless filtering, a stateful firewall keeps track of active network connections and can make filtering decisions based on the state of a connection.

I worked with connection tracking to better understand how Linux can identify whether traffic belongs to a new or already established connection.

This demonstrated why stateful filtering can provide more context when deciding whether network traffic should be allowed.

## Connection Tracking

I used connection tracking concepts during the lab to examine active network connections.

This helped me understand how a firewall can keep information about communication between systems instead of treating every packet as completely unrelated.

Connection tracking is useful because return traffic from a legitimate connection can be recognized as part of that existing communication.

This part of the lab helped connect my understanding of TCP sessions with firewall security.

## Rate Limiting

I also worked with rate limiting to control how frequently certain traffic was allowed through the firewall.

Instead of completely blocking a type of traffic, rate limiting can restrict how much of that traffic is accepted within a certain period.

This demonstrated another way firewall rules can be used to protect systems from excessive or unwanted network traffic while still allowing legitimate communication.

## Kernel Logging and Verification

To verify what the firewall was doing, I examined Linux kernel messages using `dmesg`.

The logs allowed me to confirm that packets were being detected by the kernel module and helped me compare the logged information with the network traffic I generated during testing.

Using logs was important because it provided another way to verify firewall behavior instead of relying only on whether a connection appeared to work.

I also tested communication between Docker containers to see the effects of different firewall configurations in real time.

## Security Concepts Demonstrated

This project covered several important networking and cybersecurity concepts, including:

- Network firewalls
- Packet filtering
- Netfilter
- iptables
- Linux kernel networking
- TCP traffic
- UDP traffic
- ICMP traffic
- DNS filtering
- INPUT, OUTPUT, and FORWARD chains
- Stateful packet filtering
- Stateless packet filtering
- Connection tracking
- Rate limiting
- Firewall logging
- Network traffic testing

## Skills and Technologies

**Operating Systems and Environments**
- Linux
- Docker

**Firewall Technologies**
- Netfilter
- iptables
- Linux Kernel Modules

**Networking**
- TCP/IP
- TCP
- UDP
- ICMP
- DNS
- Network Traffic Analysis

**Security Concepts**
- Packet Filtering
- Stateful Filtering
- Stateless Filtering
- Connection Tracking
- Rate Limiting
- Firewall Rule Testing

**Tools**
- iptables
- conntrack
- dmesg
- Docker

## What I Learned

The Firewall Exploration Lab helped me understand what happens behind the scenes when a firewall processes network traffic. Before completing the lab, I understood that firewalls could allow or block traffic, but this project gave me experience creating the rules and testing how those rules affected actual network communication.

Working with Netfilter and a Linux kernel module also helped me understand how packet filtering can take place inside the operating system. Using iptables gave me more experience controlling traffic based on its direction, protocol, and connection information.

I also gained a better understanding of the difference between stateful and stateless packet filtering. Connection tracking showed me how a firewall can use information about an existing connection when deciding whether traffic should be accepted.

Testing DNS, TCP, UDP, and ICMP traffic also showed me why firewall rules have to be configured carefully. A rule that is too restrictive can interfere with legitimate services, while a rule that is too open can create unnecessary security risks.

Overall, this project strengthened my Linux, networking, firewall configuration, packet filtering, troubleshooting, and network security skills.

## Disclaimer

This project was completed in an isolated and controlled lab environment for cybersecurity education and training. The firewall configurations and network testing performed during this project were used to understand defensive network security concepts and Linux firewall technologies.
