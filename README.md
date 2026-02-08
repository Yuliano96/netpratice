*This project has been created as part of the 42 curriculum by ypacileo.*

## Description
This project is a networking training exercise focused on understanding and applying core TCP/IP concepts.
The goal is to correctly configure IP addresses, subnet masks, gateways, and routing rules so that all devices in a given network topology can communicate properly.

Through multiple levels, the project reinforces fundamental networking knowledge such as subnetting, routing logic, and the role of different network devices.

## Instructions

To solve this project, the student must:

* Download the file attached to the project's page.
* Extract the files in any folder they choose.
* In this folder, run the run.sh file (a shell script that will launch a webserver and open the dedicated page in their preferred web browser).
* Once the interface is open, the student should input their login to begin practicing with their personal configuration.
* The student will have to complete 10 levels and, for each level, export their configuration using the 'Get my config' button. Those files will later be turned in at the root of the repository, as mentioned in the submission part.

## Submission Details

- A total of 10 exported configuration files (one per level) must be placed at the root of the Git repository.

- An English-written README.md file must also be present at the repository root.

- The repository must contain only the required files for evaluation.

## Resources

### TCP/IP Model

The TCP/IP model defines how devices transmit data between each other and enables communication across networks and long distances. It describes how data is exchanged and organized within networks and is divided into four layers:

1. **Network Access Layer**
Defines how data is physically transmitted over the network. It includes hardware signaling and media such as network interface cards (NICs), Ethernet cables, and wireless networks. This layer corresponds to the Physical and Data Link layers of the OSI model.

2. **Internet Layer**
Responsible for packet routing and logical addressing. It ensures that data packets are sent across networks and reach their correct destination, primarily using IP addressing.

3. **Transport Layer**
Provides reliable data transfer between source and destination devices. It handles packet segmentation, sequencing, error detection, and flow control, ensuring data integrity and correct order.

4. **Application Layer**
Represents the programs and services that use TCP/IP to communicate, such as email systems and messaging platforms. It combines the Application, Presentation, and Session layers of the OSI model.

### OSI Model

The Open Systems Interconnection (OSI) model is a conceptual framework that standardizes network communication into seven layers, allowing interoperability between different systems and technologies.

The seven layers are:

1. **Layer 7 – Application:** User-facing applications and network services.

2. **Layer 6 – Presentation:** Data translation, encryption, and compression.

3. **Layer 5 – Session:** Session establishment, management, and termination.

4. **Layer 4– Transport:** End-to-end data delivery and reliability.

5. **Layer 3 – Network:** Logical addressing, routing, and packet forwarding.

6. **Layer 2 – Data Link:** Local network data transfer and MAC addressing.

7. **Layer 1 – Physical:** Physical transmission media and hardware components.

## Subnet Mask

A subnet mask is a critical component of TCP/IP networking. It is used to determine whether a destination host is located on the local network or on a remote network.

IP addresses do not inherently define which part represents the network and which part represents the host. The subnet mask provides this information.
For example, the subnet mask 255.255.255.0 corresponds to:

	11111111.11111111.11111111.00000000

By aligning the IP address and the subnet mask, the network and host portions can be identified, allowing proper routing and communication.

# Default Gateway

When a TCP/IP host needs to communicate with a device on a different network, it sends the packet to a router known as the default gateway.

- The host compares the destination IP address with its own subnet mask:

- If the destination is local, the packet is sent directly within the subnet.

- If the destination is remote, the packet is forwarded to the default gateway, which is responsible for routing it to the correct network.

## Router

A router is a device that forwards data packets between different networks. It typically connects a local area network (LAN) to external networks such as the internet via a WAN interface.

Routers use routing protocols to determine the most efficient path for data transmission, allowing devices within a local network to communicate with external networks.
## Switch

A switch is a network device used to connect multiple devices within a local area network (LAN). Unlike hubs, switches forward data only to the intended destination device using MAC addresses.

This targeted forwarding reduces network traffic, improves performance, and ensures efficient and secure communication between connected devices.

## Use of AI Tools

AI tools were used for the following purposes:

- Clarifying networking theory (TCP/IP addressing, subnetting, routing, default gateways).

- Validating logical reasoning while solving network configurations.

- Improving the clarity and quality of documentation and explanations.

AI tools were not used to automatically generate final solutions without understanding.



## References

- https://www.fortinet.com/lat/resources/cyberglossary/tcp-ip
- https://learn.microsoft.com/en-us/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting
- https://www.geyma.com/blog/diferencia-router-switch/

## Tutorials

- https://www.youtube.com/watch?v=9k7TteZaXms&list=PLg9145ptuAijivEI4t0cb31FA41zqclwO
- https://www.youtube.com/watch?v=wksPyiU1BvE&list=PLbcS-eIZbbxWSCANJXiXj_5zBriR81m54



