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
