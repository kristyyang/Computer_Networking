# Computer Networks and the Internet

## 1.1 What is the internet ?

-  First, we can describe the nuts and bolts of the internet, the basic hardware and software components that make up the internet.

- Second, we can describe the Internet in terms of a network-ing infrastructure that provides services to distributed applications

### 1.1.1 A Nuts-and Bolts Description

- End system are connected together by a network of communication links and packet switches(分组交换).


```text
- communication links made up of different types of physical media (eg. coaxial cable,copper wire, optical fiber, and radio spectrum, radio spectrum)
```

- Transmission rate of a link measured in bits/second
(when one side of data being send it will adds header butes to each segment)

- Resulting packages of information, known as packets in the jargon of computer networks, are then sent through the network to the destination end system

分组是由一块用户数据和必要的地址和管理信息组成，保证网络能够将数据传递到目标。类似于从邮局发送的包裹上注明的地址一样,只有提供给网络这些信息，网络（邮局）才能把分组（包裹）往正确的地址传送。
分组通过最佳路径(取决于 路由算法)路由到目标。但并不是所有在相同两个主机之间传送的分组（即使是来自同一消息的那些分组）一定要沿着相同的路径传送。

-  A packet switch takes a paket arriving on one of its incoming communication links and forwards that packet on one of its outgoing communication links.

- Most prominent types in today Internet are **routers** and **link-leyer switches**.
     - **both** types of switches forward packets toward their *ultimate destinations.*
     - **Link-layer switches** are typically used in *access networks*.
     - **Router** are typically used in the *network core.*

-  The sequence(顺序) of communication links and packet switches
     -  sending end system to receiving end system is known as **ROUTE** or **PATH**

- End systems access the Internet through **Internet  service Providers (ISPs)**

- Each ISPs is in **itself** a network of packet switches and communication links.

- **ISPs** provide a variety of types of **network access** to the end system

- **ISPs** provide Internet access to **content providers**, containing Web sites and video servers directly to the Internet.

- **ISPs** provide access to end systems must also be **interconnected.**

- End systems, packet switches and other pieces of the Internet run **protocols** that control the **sending and receiving of informaiton within the Internet**.

- **The transimission Control protocal (TCP)** and  **Internet Protocal(IP)** are two of the most important protocols in the internet.

**IP protocol**

```text
specifies the format of the packets that are sent and received among routers and end systems.
```

### 1.1.2 A services Description

### 1.1.3 What is Protocol?

#### Network protocols

- All activity in the Internet that involves two or more communicating remote entities is governed by a protocal.

- Different protocols are used to accomplish different communication tasks.

```text
A Protocol defines the format and the order of messages exchanged between two or more communicating entities, as well as the actions taken on the transimission and/or receipt of a message or other event.
```

## 1.2 The Network Edge

Hosts and end systems interchangeably; *host = end system*.

- Hosts are sometimes further divided into two categories: **clients** and **servers**
   - clients eg: mobile PCs, smartphones, and so on.
   - servers eg: email, web pages, and video in large data centers.

### 1.2.1 Access Networks

Two type of broadband residential access are **digital subscriber line(DSL) and cable.**

## 1.3 Network core

### 1.3.1 Packet Switching

- End systems exchange messages with each other.
- To send a message from a source end system to destination end system. Long message need to into smaller chunks of data as **Packets**

- Between source and destinaion, each **packet** travels through **communication links and packet switches.**

#### Store-and-Forward Transmission

Most packet switches use **store-and-forward transmission** at the inputs to the links.

```text
Store-and-forword transmission

packet switch must receive the entire packet before it can begin to transmit the first bit of packet onto outbound link.
```

#### Queuing delays and packet loss

- Each packet switch has multiple links attached to it.

1. For each attached link, the packet switch has an output buffer, which stores packets that the router is about send into that link.

2. Packets suffer output buffer  **queuing delays**
3. Buffer space is finite, an arriving packet need to wait and  **packet loss** will occur.

#### Forwarding Tables and Routing Protocols

- Each internet has IP
- Each router has forwarding table that maps destination addresses, routers directs the packet to this outbound link.
- Internet has a number of special routing protocols that are used to automatically set the forwarding tables.

### 1.3.2 Circuit Switching

Two fundamental approaches to moving data through newwork of linkand switches.
**Circuit switching** and **packet switching**

- The resources needed **along a path** to provide for **communication bewteen the end systems.** that are reserved for duration of the communication session between the end systems.

- Hosts wanna communication, the network establishes a **dedicated end-to-end connection between the two hosts.**

#### Multiplexing in Circuit-Switched Networks

A circuit in a link is either **frequency-division multiplexing(FDM)** or **time-division multiplexing(TDM)**

- With FDM, the frequency spectrum of a link is divided up among the connections established across the link.

- With TDM link, time is divided into frames of fixed duration, and each freame is divided into a fixed number of time slots.
   * when network establishes a connection across a link, the network dedicates one time slot inevery frame to this connection.

- Proponents of **packet switching** have always argued that **circuit switching** is **wasteful** because the dedicated circuits are idle during  **silent periods**

#### Packet Switching Versus Circuit Switching

**Packet switching** more efficient

### 1.3.3 A network of networks

- we saw earlier that end systems connect into the Internet via an access ISP. The access

- ISP can provide either wired or wireless connectivity, using an array of access technologies including DSL cable, FTTH,Wi-Fi

- Our first network structure, *Network Structure 1*, interconnects all of the access ISPs with a single global transit ISP.

- Our second network Structure 2, two-tier hierarchy with global transit providers residing at the top tier and access ISPs at the bottom tier.
