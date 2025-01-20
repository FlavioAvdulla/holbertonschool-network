# Networking Basics

## Table of Contents
1. [OSI Model](#osi-model)
2. [Types of Network](#types-of-network)
3. [MAC and IP Address](#mac-and-ip-address)
    - [Questions](#questions)
4. [UDP and TCP](#udp-and-tcp)
    - [Questions](#questions-1)
5. [TCP and UDP Ports](#tcp-and-udp-ports)
6. [Is the Host on the Network](#is-the-host-on-the-network)

## OSI Model
OSI (Open Systems Interconnection) is an abstract model to describe layered communication and computer network design. The idea is to segregate the different parts of what make communication possible.
File: `0-OSI_model`

## Types of Network
LAN connect local devices together, WAN connects LANs together, and WANs are operating over the Internet.
File: `1-types_of_network`

## MAC and IP Address
### Questions:
1. **What is a MAC address?**
    - The name of a network interface
    - The unique identifier of a network interface
    - A network interface
2. **What is an IP address?**
    - Is to devices connected to a network what postal address is to houses
    - The unique identifier of a network interface
    - Is a number that network devices use to connect to networks
File: `2-MAC_and_IP_address`

## UDP and TCP
Let’s fill the empty parts in the drawing above.

### Questions:
1. **Which statement is correct for the TCP box:**
    - It is a protocol that is transferring data in a slow way but surely
    - It is a protocol that is transferring data in a fast way and might loss data along in the process
2. **Which statement is correct for the UDP box:**
    - It is a protocol that is transferring data in a slow way but surely
    - It is a protocol that is transferring data in a fast way and might loss data along in the process
3. **Which statement is correct for the TCP worker:**
    - Have you received boxes x, y, z?
    - May I increase the rate at which I am sending you boxes?
File: `3-UDP_and_TCP`

## TCP and UDP Ports
Once packets have been sent to the right network device using IP using either UDP or TCP as a mode of transportation, it needs to actually enter the network device.

If we continue the comparison of a network device to your house, where IP address is like your postal address, UDP and TCP ports are like the windows and doors of your place. A TCP/UDP network device has 65535 ports. Some of them are officially reserved for a specific usage, some of them are known to be used for a specific usage (but nothing is officially declared) and the rest are free of use.

While the full list of ports should not be memorized, it is important to know the most used ports, let’s start by remembering 3 of them:
- 22 for SSH
- 80 for HTTP
- 443 for HTTPS

Note that a specific IP + port = socket.

### Task:
Write a Bash script that displays listening ports:
- That only shows listening sockets
- That shows the PID and name of the program to which each socket belongs
File: `4-TCP_and_UDP_ports`

## Is the Host on the Network
The Internet Control Message Protocol (ICMP) is a protocol in the Internet protocol suite. It is used by network devices to check if other network devices are available on the network. The command ping uses ICMP to make sure that a network device remains online or to troubleshoot issues on the network.

### Task:
Write a Bash script that pings an IP address passed as an argument.

#### Requirements:
- Accepts a string as an argument
- Displays Usage: `5-is_the_host_on_the_network {IP_ADDRESS}` if no argument passed
- Ping the IP 5 times

It is interesting to look at the time value, which is the time that it took for the ICMP request to go to the 8.8.8.8 IP and come back to my host. The IP 8.8.8.8 is owned by Google, and the quickest roundtrip between my computer and Google was 7.57 ms which is pretty fast, which is a sign that the network path between my computer and Google’s datacenter is in good shape. A slow ping would indicate a slow network.

Next time you feel that your connection is slow, try the ping command to see what is going on!
File: `5-is_the_host_on_the_network`
