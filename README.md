# Chat and VoIP Communication System

This repository implements a simple **Chat and VoIP** communication system. It allows users to send text messages, make voice calls, and test the microphone through a custom-built application. The system utilizes UDP-based messaging for communication.

## Overview

The system consists of a Java application where users can:
- Send and receive text messages.
- Make and answer voice calls.
- Test microphone functionality for audio calls.
- Handle different states for the communication process, such as active calls, outgoing calls, incoming calls, and microphone testing.

The application is designed to work over a network using UDP for messaging and voice transmission. It includes classes to send and receive messages, handle call setup and termination, and manage audio input/output.

## How to Run

### Prerequisites:
1. **Java Development Kit (JDK)**: The application is built using Java, so ensure you have the JDK installed on your system.
2. **Wireshark (Optional)**: Use Wireshark to inspect the UDP packets for better understanding of the communication process.

### Configuration
**You need to update the receiverAddress and ownAddress with correct IP addresses and ports. These are used for setting up the connections for both sending and receiving data.**
```java
// Change with correct address and ports
static String receiverAddressString = "ipAddress";  // Change with actual address
static String ownAddressString = "ipAddress";      // Change with actual address
static int receiverPort = 12346;                    // Change with correct port
static int ownPort = 12345;                         // Change with correct port
```

### Running the Application:
**Windows:**
```bash
cd C:\your-local-path\src\main\java && javac
com\cn2\communication\*.java && java com.cn2.communication.App
```

**Linux/MacOS:**
```bash
cd your-local-path/src/main/java && javac com/cn2/communication/*.java
&& java com.cn2.communication.App
```

### System Architecture:
The application architecture consists of the following components:
- **Chat Client**: Responsible for sending and receiving text messages using UDP.
- **Voice Client**: Handles the sending and receiving of voice data via UDP.
- **Microphone Testing**: Provides functionality to test microphone input.
- **State Management**: The system manages various states, including call initiation, call active, call termination, and microphone testing.

### Running Multiple Instances:
To test the application with multiple users, you can run the program on different machines or different terminals by specifying different port numbers. Ensure that each instance has a unique port number for the UDP communication.

### Features
- **Message Sending**: The system can send messages over a UDP connection.
- **Message Receiving**: Messages can be received asynchronously using UDP packets.
- **Audio Transmission**: Voice calls are made by capturing audio from the microphone and sending it over the network.

---

## Acknowledgments

- **Java**: Official documentation for [Java](https://docs.oracle.com/en/java/).
- **Wireshark**: [Wireshark](https://www.wireshark.org/) for network protocol analysis.
- **JDK (Java Development Kit)**: [JDK Documentation](https://www.oracle.com/java/technologies/javase-downloads.html). 

---
