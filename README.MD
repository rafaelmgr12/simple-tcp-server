<h1 align="center">TCP Server/Client</h1>
<p align = "center"> An simple TCP server and client</p>


<p align="center">
   <a href="#-technology">Introduction</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-technology">Technology</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <a href="#-project">Project</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-how-to-run">How to Run</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-license">License</a>
</p>

<p align="center">
  <img alt="License" src="https://img.shields.io/static/v1?label=license&message=MIT&color=8257E5&labelColor=000000">
</p>

## Introduction

The purpose of creating this repository is for educational purposes. The goal is to develop a server and client that can communicate using the TCP protocol. However, before diving into the code, it is important to explain the key concepts of how TCP works. 

### What is?
TCP (Transmission Control Protocol) is a standard that defines how data is transmitted over a network. It is one of the core protocols of the internet protocol (IP) suite and is responsible for establishing, maintaining, and terminating connections between devices on a network. TCP works by breaking down data into small packets, which are then sent to the destination device over the network. The receiving device reassembles the packets in the correct order to reconstruct the original data. TCP also includes error-checking mechanisms to ensure that all packets are received correctly and in the correct order. This process is known as flow control and enables reliable data transfer across a network.

### How it works
TCP connections work through a process called the three-way handshake. The three-way handshake is a process that establishes a connection between two devices on a network before any data is exchanged. The process consists of three steps:

1. The initiating device, known as the client, sends a packet with the SYN (synchronize) flag set to the destination device, known as the server. This packet is called the SYN packet and serves as a request to initiate a connection.
2. The server receives the SYN packet and responds with a packet with both the SYN and ACK (acknowledge) flags set. This packet is called the SYN-ACK packet and serves as an acknowledgement of the client's request to initiate a connection.
3. The client receives the SYN-ACK packet and sends a packet with only the ACK flag set. This packet is called the ACK packet and serves as a final acknowledgement of the connection establishment.

At this point, the connection is established and data can be exchanged between the client and the server. Once the data transfer is complete, either side can initiate the termination of the connection, which is done through a similar process of sending packets with the FIN (finish) flag set. This process is called the four-way handshake and is used to close the connection.

### Pratical Example

An example of how TCP works would be a user sending an email using a web-based email client. The user writes and sends the email, and the web-based email client breaks the email down into small packets of data. These packets are then sent over the internet, using the IP protocol to route the packets to the destination email server.

The destination email server receives the packets and uses TCP to reassemble them in the correct order. The server then checks for any errors and, if none are found, delivers the email to the intended recipient's inbox.

This process happens in the background and is transparent to the user, who is only aware of sending and receiving the email. However, the process of breaking down the data into packets, sending them over the network, and reassembling them at the destination is managed by the TCP protocol, which ensures that the email is delivered reliably and in the correct order.

## ✨ Technology

The Project was develop as using the following techs:
- [Go](https://go.dev/)

## 💻 Project
> The server can accept multiple clients

The code works as follows:

The client code is a TCP client that connects to a server running on IP address 0.0.0.0 and port 9999. It creates two buffered readers, one for reading input from the client's terminal (os.Stdin) and the other for reading input from the server (con). It enters an infinite loop, where it first waits for input from the client, sends it to the server, waits for a response from the server, and logs the response. If there is an error, the connection is closed.

The server code is a TCP server that listens for incoming connections on IP address 0.0.0.0 and port 9999. It enters an infinite loop, where it waits for incoming connections, creates a new goroutine to handle the client request when a client connects, and logs the client request. If the input is ":QUIT", it logs that the client requested the server to close the connection and returns. If there is an error, the connection is closed.

## 🚀 How to Run

To run the this project :

**Run server**:

```
go run -race .\server\server.go
```

**Run client**
```
go run -race .\client\client.go
```

Once you are in a client session, just type something to see what happens. You might as well test exit operations too.

## 📄 License
The projects is under the MIT license. See the file [LICENSE](LICENSE) fore more details

---
## Author

Made with ♥ by Rafael 👋🏻


[![Linkedin Badge](https://img.shields.io/badge/-Rafael-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/tgmarinho/)](https://www.linkedin.com/in/rafael-mgr/)
[![Gmail Badge](https://img.shields.io/badge/-Gmail-red?style=flat-square&link=mailto:nelsonsantosaraujo@hotmail.com)](mailto:ribeirorafaelmatehus@gmail.com)
