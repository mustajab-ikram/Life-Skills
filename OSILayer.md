# The OSI model compendium

Table of contents:

- [The OSI model compendium](#the-osi-model-compendium)
  - [Reviewing the OSI Model](#reviewing-the-osi-model)
    - [What is the OSI model?](#what-is-the-osi-model)
    - [Pros and cons of OSI model](#pros-and-cons-of-osi-model)
      - [Pros:](#pros)
      - [Cons:](#cons)
  - [OSI model layers](#osi-model-layers)
    - [Brief looks of layers](#brief-looks-of-layers)
    - [Each layer in details](#each-layer-in-details)
      - [L7 The Application Layer](#l7-the-application-layer)
      - [L6 The Presentation layer](#l6-the-presentation-layer)
      - [L5 The Session Layer](#l5-the-session-layer)
      - [L4 The Transport Layer](#l4-the-transport-layer)
      - [L3 The Network Layer](#l3-the-network-layer)
      - [L2 The Data Link Layer](#l2-the-data-link-layer)
      - [L1 The Physical Layer](#l1-the-physical-layer)
    - [Transport layer ports](#transport-layer-ports)
    - [Important ports on transport layer](#important-ports-on-transport-layer)
    - [Acronyms](#acronyms)
  - [References](#references)
___

## Reviewing the OSI Model

### What is the OSI model?
- **The Open Systems Interconnection (OSI) Reference Model.**
    - *A conceptual framework that describes how data moves throughout a network.*
- Why was it developed?
    - *The OSI model describes how a network functions and standardizes the way that systems send information to one another.*
- Have unique protocols at each layer.
- It is only a reference model. It is not implemented in real world (TCP/IP is).
- The OSI Model breaks down the complex task of computer to computer communication into 7 layers.
    - **UPPER LAYERS (HOST LAYERS)**
        - Handled by host computer and performs application specific functions, such as data formatting, encryption, and connection management.
    - **LOWER LAYERS (MEDIA LAYERS)**
        - Provide network specific functions, such as routing, addressing, and flow control.
___

### Pros and cons of OSI model

#### Pros:

- It assists you with normalizing switch, switch, motherboard, and other equipment
- Lessens intricacy and normalizes interfaces
- Works with measured designing
- Assists you with guaranteeing interoperable innovation
- Assists you with speeding up the development
- Conventions can be supplanted by new conventions when innovation changes
- Offer help for association situated administrations just as connectionless assistance
- It's anything but a standard model in PC networking
- Supports connectionless and association situated administrations
- Offers adaptability to adjust to different kinds of conventions

#### Cons:

- Fitting of conventions is a dreary assignment
- You can just utilize it's anything but a reference model
- Doesn't characterize a particular convention
- In the OSI network layer model, a few administrations are copied in numerous layers, for example, the vehicle and information interface layers
- Layers can't work in equal as each layer need to hold on to acquire information from the past layer
___

## OSI model layers

### Brief looks of layers

<div align="center">
<img src="media/osi-model-7-layers.svg">
<p><strong>Figure:</strong> the OSI layers and their usage.</p>
</div>

___

### Each layer in details

#### L7 The Application Layer 
- **Network process to application.**

<div align="center">
<img src="media/7-application-layer.svg">
<p><strong>Figure:</strong> L7 the application layer</p>
</div>

- Where users communicate to the computer.
- Acts as an interface b/w the application program & the network.
- Provides an interface for Chrome or Outlook to communicate with the network.
- Applications doesn't reside in the application layer protocol, but instead interfaces with the application layer protocols.
- e.g., Chrome browser interfacing with HTTP protocol. 

#### L6 The Presentation layer
- **Data Representation and encryption.**
<div align="center">
<img src="media/6-presentation-layer.svg">
<p><strong>Figure:</strong> L6 the presentation layer.</p>
</div>

- Ensure that data transferred from one system's application layer can be read by other system's Application Layer.
- Character Encoding; Acts as the translater & formatter.
    - English Characters, Chinese Characters, etc
- Application Encryption.
- Example: HTML converted to ASCII format.

#### L5 The Session Layer
- **Interhost communcation.**

<div align="center">
<img src="media/5-session-layer.svg">
<p><strong>Figure:</strong> L5 the session layer.</p>
</div>

- Responsible for setting up, managing, and then tearing down sessions between Presentation-Layer entities.
- Coordinates communication between systems.
    - Start, Stop, Restart.

#### L4 The Transport Layer
- **End-to-End connections and reliability.**

<div align="center">
<img src="media/4-transport-layer.svg">
<p><strong>Figure:</strong> L4 the transport layer.</p>
</div>

- The "Post Office" Layer.
    - TCP (Transmission Control Protocol)
    - UDP (User Datagram Protocol)
- Ensures that data arrives safely at its destination.
- Segments & reassembles data into data stream.

#### L3 The Network Layer
- **Path determination and Logical Addressing(IP).**
<div align="center">
<img src="media/3-network-layer.svg">
<p><strong>Figure:</strong> L3 the network layer.</p>
</div>

- The "Routing" Layer.
- Provides addressing & routing services.
- Places two addresses in the packet:
    - Source addresss & destination address.
- Internet Protocol (IP)
    - The primary network protocol used on the Internet, IPv4, IPv6 Logical Addressing.

#### L2 The Data Link Layer
- **Physical Addressing (MAC & LLC).**
<div align="center">
<img src="media/2-data-link-layer.svg">
<p><strong>Figure:</strong> L2 the data link layer.</p>
</div>

- Provides physical transmission of thr data.
- Ensures that messages are delivered to the proper device on a LAN using hardware addresses.
    - MAC (Media Access Control) address.
    - The basic fundamental addressing on network to be able to send traffic from one device to another.
- Translates messages from the Network Layer into bits for the Physical Layer.
- **The "Switching" Layer.**

#### L1 The Physical Layer
- **Media, Signal, and Binary Transmission.**

<div align="center">
<img src="media/1-physical-layer.svg">
<p><strong>Figure:</strong> L1 the physical layer.</p>
</div>

- The Physics of the Network
    - Sends bits & receive bits
    - Signaling, cabling, connectors
    - This layer isn't about protocols
- *"If you have a physical layer problem."*
    - Fix your cabling, punch-downs, etc.
    - Testing & replacing cables.
    - Swapping adapter cards.
___

### Transport layer ports

| Category         | Range       | Comments                                                     |
| ---------------- | ----------- | ------------------------------------------------------------ |
| Well Known Ports | 0 - 1023    | Used by system processes e.g. SSH(22), DNS(53), FTP(21), etc. |
| Registered Ports | 1024-49151  | For specific services e.g. PostgreSQL(5432), Redis(6379), etc. |
| Private Ports    | 49152-65535 | For private purposes e.g. to run an application              |

### Important ports on transport layer

| Port Number | Protocol | Application                     |
| ----------- | -------- | ------------------------------- |
| 20          | TCP      | FTP data                        |
| 21          | TCP      | FTP control                     |
| 22          | TCP      | SSH                             |
| 23          | TCP      | Telnet                          |
| 25          | TCP      | SMTP                            |
| 53          | UDP, TCP | DNS                             |
| 67, 68      | UDP      | DHCP                            |
| 69          | UDP      | TFTP                            |
| 80          | TCP      | HTTP                            |
| 110         | TCP      | POP3                            |
| 161         | UDP      | SNMP                            |
| 443         | TCP      | SSL                             |
| 16384-32767 | UDP      | TRP-base Voice (VoIP) and Video |
___

### Acronyms

These acronyms are useful to remember the OSI model.
- All People Seem To Need Data Processing (**L7**-**L1**).  
- Please Do Not Throw Sausage Pizza Away (**L1**-**L7**).

___

## References

- [Introduction to Computer Networks for Non-Techies](https://www.udemy.com/course/introduction-to-computer-networks/)
- [What is the OSI Model? 7 layers explained in detail](https://www.educative.io/blog/osi-model-layers)
- [OSI Model Explained](https://youtu.be/vv4y_uOneC0)
- [What is the OSI model?](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)