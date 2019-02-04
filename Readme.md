# LFD271: HYPERLEDGER FABRIC FUNDAMENTALS:

# Blockchain and Distributed Ledger Technology
Following the terminology that a node represents an end-point and a network is a collection of interlnked nodes that exchange information, we can charaterize networks based on their topology:
* **Centralized networks**
* **Distributed networks**
* **Decentralized networks**


![](https://i.imgur.com/s0wZAMQ.png)

**Centralized Network** architecture has a central server to which all nodes are conected. 
* All Nodes(clients) send their data to one central node, the server, which then process and/or sends the data back or relays the data to other nodes in the network.

**Advantage**
* Can be easily upgraded and maintained.

**Disadvantage**
* If the server fails, the whole system fails. 
* Relies on a single point of trust; if that single point of trust is compromised, the entire system is compromised.
* There is less built-in validation regarding the fairness, correctness and integrity of the server and/or the service provided.
* The server is central point of trust.

**Distributed Network** (Mesh Network) has no central node or server. Each node, also denoted as peer, can be connected to other nodes, and data is transmitted or processed through various nodes, not just through a particular one.

**Advantage**
* Resilient and cheap.
* Lower quality links and nodes can create a highly reliable and resilient communication network. 
* Geographic spread - the network can grow quite large by just adding nodes.

**Disadvantage**
* Highly spread out system with low quality links, the speed of data propagation can be low. This affects the speedy replication of blocks to all nodes.

**Decentralized Network** is a distributed combination of some centralized systems/networks.
It is not centralized, as it definitely doesn't rely on one single server, but is also not necessarily fully distributed, as it can have a few sub-networks that are more "centralized".

**Advantage**
* Doesn't rely on one single and central node.
* Doesn't require as many links between all the other nodes.

**Disadvantage**
* Risky partitioning of networks into sub-networks if one or more of the semi-central hubs go down. The ordinary nodes of the network only have limited routes with other nodes that pass through the damaged or non-active semi-central hubs.


## Centralized vs Decentralized solutions
* **Maintenance, Consistency**
    * Centralized systems are considered easier to maintain.
    * For Decentralized systems, consistency and maintenance becomes an issue, as multiple copies of compatible software and associated rules have to be running on different semi-central nodes or on nodes where this consistency matters.
* **Upgradability** 
    * Centralized system, has less issue with version-inconsistency. (For Example: "We no longer support Microsoft Internet Explorer version 6.x" or "Please Upgrade your flash Version")
    * For Decentralized system, it is a lot harder to push an upgrade to all nodes. In Decentralized network getting a wide "consensus" arround such an upgrade is a much harder task.
* **Scalability and Performance**
    * Centralized systems have more "direct" communication between nodes, and the number of hops required for nodes to communicate is less.
    * Decentralized systems have better throughput, as having more nodes scale better.
* **Fault Tolerance/Points of Failure**
    * Centralized systems pose a much higher risk when anything goes wrong on the sever-side - as it may bring the whole network/service down, when all is centered around it. There is no redundancy.
    * Decentralized and distributed systems are much more preferable when redundancy is needed, which is also how the internet was designed.
* **Determinism and Predictability**
    * Other than software upgrades and version updates, distributed and decentralized systems are unusually vulnerable to non-determinism. On the physical side, different nodes/machines in the system have different hardware, performance and locks. In addition, such nodes and their owners/operators may also have different incentives. Unlike with centralized system, when one can own the machine, make sure it operates well, is performant and well-maintained, one does not usually have the same level of control over all the nodes in a distributed and decentralized system. Therefore, one cannot "blindly" rely on nodes relaying data on time, that transmissions are not being blocked or that data is not tampered with. 


## Blockchain

* A blockchain is a continuously growing list of records, which are ordered and combined/grouped into blocks. 
* Blocks are **linked (or "chained") using cryptography**. The first block in a blockchain is called the **genesis** block, and each following block is appended after the last block in the chain. 
* Each block typically contains a cryptographic hash of the previous block. Since each new block contains a hash of the previous block, a blockchain is inherently resistant to modification of historical data. 
* In typical blockchain implementations, the records that are grouped into a block are referred to as **transactions that take place between parties and are added to the about-to-be-written block after they have been verified.**

* For use as a distributed ledger, a blockchain is typically **managed by a peer-to-peer network** collectively adhering to a protocol for validating new blocks. **Once recorded, the data in any given block cannot be altered retroactively** without the alteration of all subsequent blocks, which requires collusion of the network majority. 

### Permissioned vs Permissionless Blockchain

**Permissionless blockchains** (think Bitcoin, Ethereum, etc.) 
* Offer access to anyone who wants to participate, including participation in the rules that govern how the blockchain functions at a fundamental level (like transaction validation). 
* Permissionless blockchains are, by design, open to everyone, and therefore, are more resistant to internal (bad actors from within the community) and external threats (forces outside of the community who want to control or thwart it). 
* Many participants verify transactions and the blocks that they are in, and help relay what they consider valid blocks. "Good" blocks that contain transactions, that the majority verify as correct, are propagated and lengthen the valid blockchain. Additionally, any node can opt-in to protect the network by participating in consensus algorithms and are incentivized by being rewarded with transaction fees.


**Permissioned blockchains** 
* Limit this governance participation to a selected group of actors, and often restrict access to the blockchain network to new participants who have cleared some level of identity authentication.
* Permissioned blockchains can offer the advantage of being less prone to the costs and overhead of transaction verification and validation processes that slow the network or make executing transactions very expensive. 

The main difference between Permissioned and Permissionless networks is **who is allowed to participate in the network.** This includes the initial access to the network and the distributed ledger, as well as **participating in the consensus protocol**. Bitcoin and Ethereum are examples of public and permissionless blockchains. These networks have mechanisms to incentivize and encourage people to join the network. **Permissioned blockchains are not visible and require permission to join the network.**



### Why Enterprises are choosing Permissioned Blockchains?

Many industries, and nearly all businesses, want to protect certain pieces of information from the details of any transaction - or even the record of the transaction itself! Certainly, this is the case in any regulated industry, like healthcare or financial services. Even when a business is not within a regulated framework, there are competitive advantages to protecting detailed information about the business's infrastructure, distribution points, or even customer data. 

Blockchain and decentralized technologies enable data robustness and integrity, and allow for the disintermediation of mediators and third parties from databases and processes. 

**Disintermediation**  is defined as reduction in the use of intermediaries between suppliers (e.g. producers) and consumers, for example by allowing one to buy directly from the farmer, rather through the middleman or by allowing others to purchase stocks directly using an exchange's mobile application directly and not through my retail banker. Historically, in the case of the financial industry, every transaction has required a counterparty in order to process the transaction. By definition, disintermediation goes hand in hand with disruption; after all, we are removing the middlemen and changing (in some cases, radically) the business model and incentive economies pegged to mediation. We can already see several prominent business models that are based on disintermediation (and are extremely disruptive): 

* **Uber**
	The largest taxi company with no vehicles. Algorithms drive their business model, and they connect market makers and market seekers. With an amazingly rich and contextually relevant user experience, they are one of the world’s most disruptive companies. 

* **Alibaba, Amazon**
	The world’s largest retailers and marketplaces, with no real inventory or retail space. Their success is attributable to directly connecting the vendors to consumers, along with harvesting insights derived from transactions. Those insights have led to intelligent marketing and selling. 
* **Airbnb**
	A couch surfing alternative that has no real inventory but yet exceeds any hospitality chain in numbers of transactions. It has created an internet-based marketplace while disintermediating the likes of tour operators and travel agents. 
    
    
Blockchain has the promise to help disintermediate and distrupt more industries, and in many cases adding permissioning to the system actually helps the members of the network to control who can access some of the shared data - in a way which allows them to share even sensitive data securely while preserving privacy, and keeping confidential data protected from unauthorized eyes. 

Industries that rely on intermediaries include (but are not limited to) the following:
* **Insurance**
	Property and casualty, auto, life 
* **Healthcare**
	Electronic healthcare records, healthcare information systems 
* **Financial services**
	Consumer/retail banks, investment banks, brokerage, etc. 
* **Transportation and logistics**
	Services associated with supply chains, including exports, imports, logistics, and related services such as finance, fund transfers, contracts, and Forex. 
* **Retail and real estate**
	Trade of durable and non-durable goods, which relies on huge margins and delays consumed by a system of intermediaries established centuries ago.
    

Blockchain technologies can address the risk of malicious nodes tampering with the data on transmission, address the risks of inconsistent system behaviors that are stemming from working with different nodes, hardware, timezone, and incentives, while being able to remove the reliance on a single point of trust and not be susceptible to having a single point of failure through a centralized topology that does not scale. 

The data on transmission is unalterable due to the securing of the transaction hash tree, along with the difficulty of obtaining the proof of work; alteration cannot be done without recomputing the proof of work hash which takes enormous computing power. In terms of the consistency, all the nodes just need to follow the same rules for validity and the layout of the blocks as well as compatibility in the transmission protocols. This allows for a heterogeneous group of nodes to collaborate on propagating valid blocks. The rules on following the longest chain also work in creating agreement across geographies, since if a longer chain becomes available slowed by network distance and link quality, then all nodes that follow the rules will build on the longest chain and discard any shorter chains that they may have.


Fundamentally, enterprises can leverage blockchain to lower uncertainty and increase trust. This can lead to faster, more secure transactional applications, as well as to removing a lot of frictions by digitizing, automating and decentralizing a lot of their day-to-day activities. For all of these reasons and many more, companies and industry consortiums will continue to focus on permissioned blockchains when evaluating the technology's potential. As mentioned, such blockchain solutions offer participants secure ways to define the rules of membership and governance in ways that provide: 

* **Immutability**
	To prevent data tampering of records, using blockchain to represent a single source of truth (e.g. for the official "books and records").
* **Privacy and Confidentiality**
	So that sensitive data (such as personal client information or sensitive commercial information) can be exchanged securely and not shared with unauthorized parties.
* **Scalability, Reliablity and Availability**
	For supporting mission-critical systems.
* **Auditability**
	Being able to monitor, manage, track, verify and retain data and records, as required and mandated by certain regulations and jurisdictions.

___

# Hyperledger Fundamentals
## Introduction

In December 2015, Hyperledger was founded as a collaborative effort created to advance blockchain technology by identifying and addressing important features for a cross-industry open standard for distributed ledgers that can transform the way business transactions are conducted globally. Hyperledger is hosted by **The Linux Foundation**

**Type of Hyperledger Frameworks**
* **Hyperldger Burrow** is a permissionable smart contract machine. Hyperledger Burrow provides a modular blockchain client with a permissioned smart contract interpreter built in part to the specification of the Ethereum Virtual Machine (EVM).
* **Hyperledger Fabric** is intended to serve as a foundation for developing applications or solutions with a modular architecture, whereas several key components of Hyperledger Fabric are plug-and-play.
* **Hyperledger Indy** contains tools, libraries, and reusable components for providing digital identities rooted on blockchains or other distributed ledgers so that they are interoperable across administrative domains, applications, and any other silos
* **Hyperledger Iroha** is a business blockchain framework designed to be simple and easy to incorporate into infrastructural projects requiring distributed ledger technology.
* **Hyperledger Sawtooth** is a modular platform for building, deploying, and running distributed ledgers. Hyperledger Sawtooth includes a novel consensus algorithm, Proof of Elapsed Time (PoET), which targets large distributed validator populations with minimal resource consumption.

**Fabric Tools**
* **Hyperledger Calliper** is a blockchain benchmark tool, which allows users to measure the performance of a specific blockchain implementation with a set of predefined use cases.
*  **Hyperledger Cello** aims to bring the on-demand “as-a-service” deployment model to the blockchain ecosystem to reduce the effort required for creating, managing and terminating blockchains
*  **Hyperledger Composer** is a collaboration tool for building blockchain business networks, accelerating the development of smart contracts and their deployment across a distributed ledger
*  **Hyperledger Quilt** offers interoperability between ledger systems by implementing ILP, which is primarily a payments protocol and is designed to transfer value across distributed ledgers and non-distributed ledgers. 

## Architecture
**Distributed Ledger Technologies**
* DLTs(Distributed Ledger Technologies) **work with a peer-to-peer network of nodes, where a ledger is distributed such that each node has an identical copy of the ledger.** 
* Ledger is an append only system of records or **log of transactions**. 
* A distributed ledger is a multi-party database with no central trusted authority. The differentiating nuance is that when **transactions are processed in blocks according to the ordering of a blockchain, the result is a distributed ledger.** Such transactions are ordered and grouped into blocks (hence the term "blockchain")

**Identity** establish a root of trust during the setup of a blockchain instance 
* The enrollment and registration of identities or system entities during network operation, and the management of changes like drops, adds, and revocations. Membership Services, under Identity, also include authentication and authorization (think about a member of a group, or a role). 

**Ledger** is the sequenced record of all state transitions in a network. 
* It is easy to think about it as the bookkeeper's table, having keys or attributes (such as "*account1balance*") and their respective values (keeps a record that "*account1balance*" is currently 17).
     
**Transactions** are state transitions that are stored in the ledger 
* They are a result of smart contract invocations ("transactions") submitted by participating parties. 

**Consensus** is the mechanism for reaching or **generating an agreement from network participants** (e.g. regarding the validity of a claim or proposed transaction). 
* This layer is using the peer-to-peer network as the underlying communication layer, **the distributed ledger that is shared between the peers, as well as an ordering service which orders the transactions and groups them into blocks**. 

**Smart Contract Layer** has the ability to run and execute some agreed-upon business logic. 
* "logic" is built into units of code that are denoted as "Smart Contracts". 
* Smart Contracts are a way to submit/propose scripts and programs that encapsulate some logic and have them live on the shared peer-to-peer network, in a way that peers can execute that exact same piece of logic. 

**Security and Crypto Services** allow different crypto algorithms or modules to be swapped out without affecting other modules. 

## Hyperledger Fabric Components

The most simplified view of a typical Hyperledger Fabric deployment is comprised of nodes that are connected as a peer-to-peer network, with a distributed ledger which is shared amongst the nodes. 

However, the nodes in Hyperledger Fabric have different roles. First, such connected nodes in Hyperledger Fabric can be of two categories: **peers** and **orderers**


* **Peers** are nodes that maintain a local copy of the ledger. 
    * They **can also propose a new transaction** that will be shared around, and potentially be saved/applied/committed to the ledger.

* **Orderers** are nodes running an "ordering service". 
    * In Hyperledger Fabric network there needs to be at least one node which is running the "ordering service", but it does not have to be the only one. ***There may be several nodes running the ordering service, and these are denoted as the "orderers".*** 
    * When a peer proposes a transaction and the transaction is committed, the **orderer helps ensure that transactions are, as the name implies, ordered correctly, and such ordered transactions are being shared with the rest of the peers.** 

There are two types of peers in Hyperledger Fabric: 

* **Endorsing Peer/Endorser** "votes" for, or "endorses" transactions ***that are proposed by the client or application layer***. The peer **does not add the transaction onto the ledger.**
       
     ***The role of endorser***
       
    *  After ***checking the client signature, it runs chaincode to get the read and write sets of the World State affected by the transaction.***
    *  These are **then sent to the orderer by the clients who collect the endorsements.** Read and write sets are the inputs and outputs to the chaincode running on the endorser. This is called **simulating the transaction**, as the results are not written back into the ledger.

***Note:*** In Hyperledger Fabric, every endorser (or endorsing node) is also a committer (committing node). So, while the endorsers are the ones whose endorsement for the transaction the client seeks, later on, both endorsers and committers ultimately commit the transaction to the ledger.

* **Committing Peer/Committer** is a peer which validates transactions after endorsement and ordering to apply the results of the transaction onto the local ledger. At this point, the valid transactions are immutably written to the ledger.

***Note:*** Every endorsing peer is also a committer, but not the other way around. There are committers that are not endorsers. 

## Identity and Membership Services

Hyperledger Fabric is a permissioned blockchain, in the sense that all participants have known identities. Especially in regulated markets, many use cases require complying with some strict KYC (Know Your Customer) requirements. These KYC requirements mandate a set of minimum checks that an organization has to conduct against a customer, before that customer is "onboarded onto the system". 

To enable permissioned networks, Hyperledger Fabric provides an identity and membership service that manages user IDs and authenticates all participants on the network. Access control lists can be used to provide additional layers of permission through authorization of specific network operations. For example, a specific user ID could be permitted to invoke a chaincode function, but blocked from deploying new chaincode. 

Because different industries and different organizations have different requirements, Hyperledger Fabric's modularity comes into play here with a pretty flexible membership service mechanism. The Hyperledger Fabric module that is in charge of participant registration, enrollment and its authentication is the **Membership Services** component.

## Fabric Certificate Authority

**Certificate Authority (CA)** that is provided both in code or via a pre-built Docker image with every Hyperledger Fabric release. 
* It is released under the Hyperledger Fabric CA component. This component is used for registering and enrolling nodes that are part of the blockchain. 
* It is responsible for creating **Enrollment Certificates (ECerts)** in the form of **standard X.509 v3** to participants that are granted the permission to join and participate in the (permissioned) blockchain network. 
* Certificate Authority, is a service **needed for issuing the (Enrollment) certificates to authenticated participants.** 

***It is important to know that, as part of Hyperledger Fabric's modular design, Fabric CA is just a reference implementation for a CA, and anyone can extend, develop his/her own, and replace it if needed.***

## Membership Services and the Membership Service Provider

Hyperledger Fabric supports **a pluggable interface which is called the Membership Service Provider (MSP)**. 
* The Membership Service Provider **manages the authentication of identity and permission management,** which are key for knowing when or whether the CA should actually issue a certificate. 
* Membership Service Provider (MSP) is a component that **aims to offer an abstraction of a membership operation architecture.** 


***There are various Membership Services implementations. Hyperledger Fabric comes with a default one, but others can write their own or integrate with other implementations that adhere to the Membership Services Provider interface.***

## The Distributed Ledger in Hyperledger Fabric

The distributed ledger in Hyperledger Fabric is comprised of two parts. We have the **World State** and the **Transaction Log**.
* **World State**
    Effectively, when we look at the "World State", or put differently, the current "state of the world", we are looking at a versioned list of key/value pairs. The value can be almost anything (it is actually a Binary Large OBject - BLOB or JSON), while the key is a unique identifier. It is typical to represent an asset or a parameter using the "key", and then to assign it an initial value, update it when needed, and even discard it in cases where it is not needed anymore.

* **Transaction Log**
    The Transaction Log **is a collection of blocks containing a sequence of transactions**. 
    * Transactions include a set of *before* and *after* key/value pairs - typically, this is referred to as an RW set (Read-Write set). 
    * Each block (other than the first one) includes a hash of the previous block. 
    * This implies that each block contains a reference to all previous blocks through the hash of the previous block. 
    * The Transaction Log is an immutable, append-only, ordered list of all transactions, which is stored on each peer. 
    * Each peer maintains a copy of the distributed ledger, which includes a log of transactions and the world state results stored in a database as key/values pairs.

As you can see below, a ledger state with **key**=CAR1 and **value**=Audi. There is a ledger state with **key**=CAR2 and a more complex value {model:BMW, color=red, owner=Jane}. 

The ledger state is used to record application information to be shared via the blockchain. This example shows ledger states for two cars, CAR1 and CAR2. As You can see that states have a key and a value. Your application programs invoke chaincode which access states via simple APIs - they **get**, **put**, and **delete** states using the key (e.g. "CAR1", set value to be "Mazda"). **Consensus algorithms ensure consistency between all copies of the ledger, so that members will agree to the upcoming changes to the state**

![](https://i.imgur.com/865vcYF.png)

## Understanding the World State
 
The World State component is the aggregate state of the ledger at a given point in time. It is the result of applying the whole Transaction Log, one transaction at a time, to the initial state of the ledger at its birth, when no state existed. 
* However, the World State **is used by chaincode and queries to get at the current state of the ledger** This is done instead of applying all the transactions serially to get at the current state, for efficiency. 
* The Transaction Log **contains a record of all state transitions to the World State.** 
* The World State is stored in a database of key value pairs. The key itself is composed of a unique value, and associated version shows the effect of transactions. With each transaction that affects the key, the version associated with the key is advanced.

***In Hyperledger Fabric, the Transaction Log contains and append only record of transactions. This record is immutable: once written, the Transaction Log cannot be changed. Together, the Transaction Log and the World State make up the distributed ledger.***


## Smart Contract Layer in Hyperledger
Hyperledger Fabric uses the term chaincode to refer to what most blockchains call a "smart contract". 
* Chaincode is simply a computer program (written in a programming language such as Golang, Node.js, etc.) which implements a predefined interface. 
* Such programs are compiled, **deployed across the network, and executed inside a Docker container, which is completely isolated from the ordering service or the Peer processes.**
* Participants can use chaincodes to implement the logic part of the decentralized application, which allows nodes and participants to run and work with the ledger. This provides the ability to run business logic in a decentralized system (and update the distributed ledger) in a consistent and replicable way
* **Chaincode is used to initialize and manage the ledger state through transactions submitted by participants or their applications.** This is done through the SDKs
* As the name suggests, deploy transactions are requests to deploy a certain chaincode across the distributed network. If the request to deploy the chaincode is approved, and the chaincode is deployed globally, chaincode invocations can be achieved using invoke transactions which, as the name indicates, are requests to invoke a call to an already deployed chaincode. Client applications invoke already deployed chaincode on behalf of the participants through transactions.

## Putting Everything Together 
**Certificate Authority**
>* Registration of Identities.
>* Enrollment Certificates (ECerts) issuance
>* Certificate Renewal/Revocation (using Certificate Revocation Lists - CRLs)

**Peer**
>* Can update and query the ledger.
>* Peers that are endorsers can endorse proposed transactions. These endorsements are being evaluated against the Endorsement Policy (you will play with this in the lab exercises).
>* Manage the ledger (both the Transaction Log and the World State).

**Ordering Service**
>* Can be run by one or several nodes
>* Creates the actual blocks of the blockchain (by ordering and grouping transactions)
>* Peers will commit changes to the ledger only after the transaction has been ordered.



### Hyperledger Fabric Work Flow:

![](https://i.imgur.com/J64uYIR.png)


In the Hyperledger Fabric workflow diagram, other than having an application using the Hyperledger Fabric SDK to interact with the Fabric CA or the ledger, 
* There are three Endorsing Peers and three non-Endorsing Peers (which is just a Committing Peer, or Committer, marked in orange).
* There may be cases where three Endorsing Peers validate and endorse a proposed transaction (the Endorsers are marked in blue), while some other Endorsers do not endorse the proposed transaction.

Hyperledger Fabric's endorsement model is very flexible in the sense that there is an agreed-upon Endorsement Policy, which basically states under what conditions a transaction is considered "endorsed" or "widely accepted". In other words, we can look at the endorsement policy in terms of "what needs to happen" to get a proposed transaction to be "approved" or marked as "valid" by the endorsers. 

Transactions must be written to the ledger in the order in which they appear in a block, even though they might be between different sets of participants within the network. For this to happen, the order of transactions must be established, and a method for rejecting bad transactions that have been inserted into the ledger in error (or maliciously) must be put into place. This happens through the setting of a bitmask for bad transactions during validations and is stored locally on every validator's Transaction Log.

# Hyperledger Fabric Transactions

## The Ledger
The distributed ledger component, which is comprised of a **World State** (the versioned list of key-value pairs) and the **Transaction Log** (the collection of transactions that actually affect the World State).

* A digital ledger has a very similar structure. In Hyperledger Fabric, the Transaction Log in particular is logically very similar to the ledger we just described (which **"logs" activity == transactions). The World State part of the ledger has a similar "key" (column) and a "value" column,** 
* which are versioned. Using the Transaction Log, we keep track of the transactions that are changing the ledger's World State in each "iteration" of change, or put differently, in each version.
* **The changes to the World State are carried through transactions that create the "next version" of the World State. Such changes are added to the ledger's log, in an append-only way. That is, we always append and not erase or change transactions that are already written to the ledger. This is why you hear so often the term "immutable ledger**
* The written transactions are immutable. This is a similar concept to the permanent summary of the results of all the amounts/transactions entered (or "logged") so far.
* Typical blockchain deployments, and Hyperledger Fabric in particular, **the ledger is distributed among the participants of the blockchain network. The technology and mechanism that are used - such underlying technology is commonly referred to as the DLT (Distributed Ledger Technology).** 
* So in a line, we have a versioned set of **key/value pairs that are distributed among peers.**

## Chanicode:
* **Decentralized and distributed systems has one of the key challenges that in such systems is to keep things "in sync".** For example, we would like all the nodes to run the same version of some "logic", or to know that each node in the network is looking at the same version of data.

* **"a smart contract is a computerized transaction protocol that executes the terms of a contract"**
* A smart contract can be a user-defined(A user-defined program that can self-execute some logic) portion of code that will transfer a digital asset (or update some values that reflect some balance or ownership) between blockchain participants.(which is also able to disintermediate third parties.)

* **An important thing is that the chaincode (or smart contract) just "moved" tokens (or assets) between two parties (Alice and Bob) without an intermediary - that is, without a third party (or a man-in-the-middle).**
* Blockchain technology in general, and Hyperledger Fabric in particular, are regarded as upcoming and promising technology with the potential to disrupt and disintermediate many such digital asset transfers, or updates to the World State using valid transactions.
* User-defined programs, called **chaincodes, are used to change the ledger's state. Chaincode is used to initialize and manage the ledger state through transactions submitted by participants or their applications.**

## Transaction Deploy:

Users (running client applications) that would like to add some logic to the blockchain they are part of can write their business logic or chaincode, and then request the blockchain network to deploy it. 
Users write their code (in Golang, Node.js, etc.) against the Hyperledger Fabric chaincode interface.
Once the code is written (the coding, debugging can be done separately), the client application can use the SDK to deploy a chaincode through a Hyperledger Fabric transaction. Effectively, a **deploy transaction** is a request to deploy a certain chaincode across the distributed network.
**This requires rights to deploy the chaincode as proven by the signatures attached to the certificates of deployment.** The chaincode must be then installed and instantiated to be properly deployed.
Upon success, the requested chaincode has been deployed to the blockchain network.

## Transaction Invoke:

Invoke transactions are requests to call (or yes, "invoke") an already deployed chaincode. **That is, when a user or a client application would like to make a change to the ledger's state, they use the SDK to propose that all the peers will make the change that will be made by the requested chaincode invocation.**
This part of the design resembles a database stored procedure, where such calls to the database stored procedure are done through Hyperledger Fabric (invoke) transactions.
Invoke function from the chaincode while passing the operation name (generally referred to as "function name") and parameters for the transaction. Of course, the chaincode has to be properly deployed, installed and instantiated before  Invokecan be executed on it.

## Transaction Query
The third type of Hyperledger Fabric Transaction is the query transaction. A query transaction can be done through the CLI(Command LIne Interface) and/or programmaticallythrough the Hyperledger Fabric SDKs.

The main difference is that queries don't modify the ledger in any way. instead just returning data from it.

## Reading from the ledger, Writing of the ledger

An invoked chaincode can read the state of the ledger or it can update (or write to) the ledger. Updating the ledger includes either adding a new key (that was not seen before) to the key/value pairs, or updating a value associated with an existing value of the key which is already in the set of the key/value pairs.
Client applications invoke already deployed chaincode on behalf of the participants through transactions.
This how really looks in practice here is a [snippet of the code](https://github.com/hyperledger/fabric-samples/blob/6b2799e6208c421347b07ac19bc9783018693540/fabcar/invoke.js#L61) that is used transaction from the Hyperledger Fabric sample applications:
```js
	var request = {
		chaincodeId: 'fabcar',
		fcn: '',
		args: [''],
		chainId: 'mychannel',
		txId: tx_id

```
the invoke.js sample code constructs a request that is used by the Hyperledger Fabric SDK to invoke a chaincode called **fabcar**.
The request object of the client application can use the SDK to create a request which specifies the chaincode (ID) to invoke, and a function with arguments. For example, one could invoke:
A createCar chaincode function call with the following arguments: **['CAR12', 'Honda', 'Accord', 'Black', 'Tom']**
A changeCarOwner chaincode function call with the following arguments: **['CAR12', 'Jerry']**
This is why we believe that it may be somewhat more intuitive to think about a chaincode function invocation (through an invoke transaction) in a Hyperledger Fabric blockchain deployment as the decentralized version of the stored procedure paradigm. The difference is that here, instead of a call to a stored procedure which is executed and operates inside or on top of a centralized database Hyperledger Fabric invoke transactions are executed by peers, and the changes are committed by each committing peer that is updating their local World State.

## Anatomy of Chaincode:
**One**
A typical implementation of chaincode in Go contains the following sections:
Import statement with libraries that we need functions and structures from. The import statement may also contain any other utilities if you are going to be using them in implementing your chaincode. These could include byte and string manipulation or JSON handling, but here is the absolute minimum required for writing a chaincode:

```go
import (
    "fmt"
    "github.com/hyperledger/fabric/core/chaincode/shim"
    "github.com/hyperledger/fabric/protos/peer"
)
```
* **fmt** is used for formatted I/O functions similar to  and scanf that will be used for reading from or writing to files or the terminal.
* **shim** provides APIs for the chaincode to access its state variables, transaction context and call other chaincodes.
* **protobuf** (which stands for protocol buffers) is taken from the third import. It was created to provide a platform and language neutral standard for data interchange it's used by Hyperledger Fabric for this purpose.

**Two**
The structure of what you are modeling:
```go
//A Hyperledger Fabric Asset 
type HLFAsset struct { 


}
```
**Three**
* An implementation of the **ChaincodeStubInterface** (normally these are methods attached to the model structure, in our case the HLFAsset refer to Init and examples below). 
* This interface defines the functions used by Hyperledger Fabric to interact with the chaincode, and used in the chaincode to interact with the ledger. 
* To read from the ledger in the chaincode, use the  GetState() call. The signatures of the functions in the interface that we will discuss are provided here (note that a lot more are omitted):

```go
type ChaincodeStubInterface interface {
//...
GetArgs() [][]byte
GetFunctionAndParameters() (string, []string)
PutState(key string, value []byte) error
Delstate(key string) error
GetStateByRange(startKey, endKey string )(StateQueryIteratorInterface, error)

//...

}
```

First goes a family of functions to get the arguments intended for chaincode Init() and Invoke() functions:
* **GetArgs()** is the main one; ***It returns the arguments as a byte array.*** There are numerous other variants with different function signatures that return the arguments as strings, function names, slices, etc., but in our example we will use the byte variant.
* **GetFunctionAndParameters()** is the other function of this type called frequently, especially inside your Invoke implementation **to get both the function name and the arguments.** This other function is used so that you can direct the call to your own implementations of what needs to be done during a particular Invoke call; i.e. makes the Invoke call trigger a specific function that you have implemented.

* **GetState()** function reads the World State from the ledger. This returns the value from the ledger (or rather, the World State) identified by the specific key passed into it.

***Note:*** that GetState() returns the value of the key currently committed to the ledger not data that has been modified by a PutState()  call, which has not been committed to the ledger. There are also some variants that return specific attributes like Transaction Ids.

* **PutState()** function proposes to write a value for a specific key into the ledger. This modifies the write set of the World State.

***Note: that until the transaction is validated and committed, the transaction is not in the ledger. Some rules have to be followed for the keys; for example, the keys must not be empty and should not start with 0x00.***

* **DelState()** is a special variant of PutState() that deletes the key from the ledger; as with all other functions, this becomes effective only on commitment to the ledger.

* **GetStateByRange()** returns a range iterator over a set of keys in the ledger. The iterator can be used to iterate over all keys. This can be used to implement a query.

An implementation of the Chaincode interface. Any chaincode has to implement the Chaincode interface: 
```go
type Chaincode interface {

Init(stub ChaincodeStubInterface) pb.Response
Invoke(stub ChaincodeStubInterface) pb.Response

}
```
This consists of two functions, **Init() and Invoke(). These are the functions used to interact with any particular instance of the chaincode.**

**Init()** allows the chaincode to initialize its internal data during the instantiate or upgrade system operations.A simple call given below with just two parameters propse to put a simple key and a value on our ledger.

```go
// Init is called during chaincode instantiation to initialize data.
// During chaincode upgrade this function needs to implement migration of data 
// be very careful to not trample existing data during migration (not implemented).
func (t *HLFAsset) Init(csi shim.ChaincodeStubInterface) peer.Response {

// Get the arguments in the form of strings
    args := csi.GetStringArgs()
    if len(args) !=2 {

        return shim.error("Expecting a key and a value, not %d arguments",len(args))

    }

// We store the key and the value passed into this function on the ledger
    err := ci.PutState(args[0], []byte(args[1]))

    if err!= nil {
        return shim.error(err.Error())
    }

    return shim.Success(nil)
}

```
**CSI** Container Storage Interface. This package doesn't contain any functional code and this file exists only to make it possible to import this repository with GO.
**Invoke()** is called to invoke a transaction. All substantial interaction from the Application or ClientAPI with the chaincode is done through this function. The chaincode normally uses the functions of the **ChaincodeStubInterface** described above to service the Invoke call.
First **GetFunctionAndParameters()** is called to get the function names and the corresponding parameters that Invoke is called with. These are then used to call the appropriate function which reads, writes or queries the ledger. This specific approach is not required, but is the most commonly seen, as this makes the code maintaining easier. The chaincode that we write references the Write(), read(), qry() function. 

```go
// Each transaction is a 'read' or 'write' or a 'qry' on the asset created by Init function.
// The write method may cretae a new asset by specifying a new key-value pair.

func (t *HLFAsset) Invoke (csi shim.ChaincodeStubInterface) peer.Response {

// get the function and args from the transaction proposal
    fn, args := stub.GetFunctionAndParameters()

var result string
var err error 
    if fn =='write' {
        result, err = write(stub,args)
    }else if fn=="read" {
        result,err = read(stub,args)
    }else if fn ="qry" {
        result, err = qry(stub,args)
    }
    else {
        return shim.Error("Invalid smart contract function name.")
    }

    if err != nil {
        return shim.Error(err.Error())
    }
// Return the result as success paylooad return shinm.success([] byte(result))

}
```
**Five**

**A main function:** The main entry point of the chaincode. This starts up chaincode in the container during the instanitate operation. 
```go
func main() {
    if err := shim.Start(new (HLFAsset)); err!= nil {
    fmt.Printf("Error starting HLFAsset chaincode: %s", err.Error())
    }
}
```

## Consensus

Consensus service support "the process by which a network of nodes provides a guaranteed ordering of transaction and validates the block of transaction. Consensus must provide the following core functionality"

* Confirms the correctness of all transactions in a proposed block, according to endorsement and consensus policies.
* Agrees on order and correctness and hence on results of execution (implies agreement on global state).
* Interfaces and depends on smart-contract layer (specifically, chaincode and transaction validation) to verify correctness of an ordered set of transactions in a block".

## Ordering Service

Because **determinism** and **consistency** are so important the role of the Ordering Service is vital.

* An **ordering service** can be run by one or several nodes. * It creates the actual blocks of the blockchain (by ordering and grouping transactions), while making sure that issues (inconsistencies) like the ones we mentioned will not happen.
***Note:*** Ordering service plays a big role-without the ordering service we may end up with inconsistencies or non-deterministic behavior.
## Endorsement Validation

This is where the peers that are the endorsers play an important role. Effectively, we do not want a system where any proposed transaction, or put differently, any request to update the ledger would"blindly get accepted". This is where the endorsing peers (also referred to as **validators** can validate and either endorse (vote in favor) or vote against a proposed transaction.

In Hyperledger Fabric, there is an agreed-upon **endorsement policy** which basically states under what conditions a transaction is considered "endorsed" or "widely accepted". In other words, we can look at the endorsement policy in terms of "what needs to happen" to get a proposed transaction to be "approved" or marked as "valid" by the endorsers.

### How It Works
* Think about a very simple endorsement policy which states that for a transaction to be considered endorsed, we require a majority of endorsers to endorse it. So, if we have 3 endorsers, a simple endorsement policy may require that we need to obtain at least 2 endorsers saying "yes".
* The last step here, having reached consensus, is to apply the changes to the ledger: adding the transaction to a block, distributing the block, and having all the peers commit the changes to their local copy of the ledger (updating the Transaction Log and the World State).

## Lifecycle of a Transaction
***Step 1: Propose Transaction***
The client propose a transaction to the endorsing peers for endorsement.![](https://i.imgur.com/qDeUnOg.png)

***Step 2: Endorsers Simulate the Proposed Transaction***
* Each of the three endorsing peers (or endorsers) will execute the proposed transaction. 
    * ***Note*** at this point, these executions are not updating each peer's local ledger.
* The client application is using the SDK because it needs to obtain or collect cryptographically signed endorsements from the endorsers.
* While simulating the execution of a chaincode, the endorser is constructing a list of the data (keys and values) that are read from the ledger (by the chaincode) and the data that will be written if the chaincode was executed in a non-simulation mode. These are two sets: read set and a write set.

![](https://i.imgur.com/ceyGLMO.png)


***Step 3: Proposal Response***

Each Endorser Returns its signed endorsement back to the client(through the SDK), with the read set and the write set which the endorser obtained through simulating the proposed transaction's chaincode.

![](https://i.imgur.com/A1XSG2r.png)

***Step 4: Broadcast Request***
* Through the Hyperledger Fabric SDK the client/application submits to the ordering service the signed endorsements (with the read sets and the write sets) that were received from the endorsers.
* This step can be described as a request for the proposed and endorsed transaction to get into a block and get broadcasted.

***Note*** other SDKs/clients/applications may submit some other transactions to the ordering service. We cannot assume that we have only one single transaction in the system.

![](https://i.imgur.com/jplXtvK.png)

***Step 5: Validate Endorsement and Other Transaction***

The orderer gathers transactions into a block in the same order it received them. It imposes a deterministic order of the transactions in a block. Additionally, it creates an order of blocks, also guaranteeing that it never creates any transactions by itself.

**Delivery guarantees:** the orderer has to deliver the blocks in the order that it created them, with total-order guarantees to the committing peers as well as the other peers. In fact, the orderer channel has both inbound guarantees (for transactions from the application peers) using **broadcast()** and outbound guarantees for delivering blocks of transactions, using **deliver()** to the client and committing peers.

![](https://i.imgur.com/YyEA3vC.png)

***Step 6: Deliver Transaction***

The block is being delivered/distributed from the ordering service to the committing peers using the peer-to-peer network and the gossip protocol.

![](https://i.imgur.com/YVOT9VZ.png)

***Step 7: Validate and Update the Ledger***

Peers will commit changes to the ledger only after the transaction has successfully gone through the full cycle. So, a block is added (see the green block added in the diagram by each committing peer).
* Every committing peer validates against the endorsement policy. 
* Also, committing peers check to ensure the read-sets are still valid for the current state. 

***Note:*** Peers do not "blindly trust" the ordering service. From the first step when the client/application makes a transaction proposal all the way through the endorsers, when enough endorsements are received, the proposed transaction and its endorsement go through an ordering service, which checks the signed endorsements, verifies that the endorsement policy is satisfied, adds it to a block (possibly groups it with other transactions) and broadcasts it/delivers that block to all the peers.

![](https://i.imgur.com/pc215fb.png)

***Step 8: Notify Client/Application***

Application can register to be notified when transaction succeed or fail, and when blocks are added to the ledger. Application will be notified by each peer to which they are connected.

# Membership, Services, MSPs and Channels

## Public Key Infrastructure:

Hyperledger Fabric is a permissioned network, and the identities of participants are tightly controlled. 
* **Public Key Infrastructure (PKI)** refers to the infrastructure which supports public key cryptography, also known as asymmetric cryptography. **Public key cryptography is a cryptographic system that uses pairs of keys.** The holder generates this pair of keys using a cryptographic function: 
    * **The public keys are sent to everyone interested in interacting with the holder, while the private keys are kept secret by the owner.** This accomplishes two functions:
        * **Authentication**, where the public key verifies that a holder of the paired private key sent the message and 
        * **Encryption**, where only the paired private key holder can decrypt the message encrypted with the public key.

* **PKI** infrastructure is responsible for securing electronic interactions in enterprises and across enterprises. 
    * **PKI binds the public keys of entities to their identities, who possess a secret (a private key) that corresponds to their public key.** 
    * These bindings are done through digital certificates signed by a Certificate Authority (CA), which can be verified by using the CA's public key. Hyperledger Fabric PKI is governed by the X.509 family of standards. 
    * The structure and semantics of the digital certificates and Certificate Revocation Lists (CRLs) in X.509 standards are governed by RFC 5280. This also allows the Hyperledger Fabric Identity Framework to interoperate with existing legacy systems, since almost all enterprises implement X.509-compatible systems.

* Digital certificates are detailed and rich structures following the X.509 standard.
* They have to be signed by a Certificate Authority to be authenticated. 
* They can describe identity attributes in detail, as well as provide trust through a certificate. The way in which the certificate data is altered or removed in X.509 is through the use of Certificate Revocation Lists, also to be signed through the chain of trust by certificate authorities.

## PKI: Chain of Trust
The way PKI works in practice is through a root CA, which is often one of the well-known CAs (such as Symantec, Verisign, etc.) that are distributed with every browser.   

In the case of many Hyperledger Fabric channel configurations, this is often a properly configured Fabric CA. This is known as the trust anchor; the trust anchor is self-certified and well-known.

The root CA can sign leaf digital certificates (meaning certificates for entities that are not CAs), and also certificates for what are known as intermediate CAs. 

**The difference between root CAs and intermediate CAs is**
* The fact that the root CA self certifies its digital certificate and any intermediate CA certificate has to be signed by the root CA or an already established intermediate CA.

**Intermediate CAs can sign certificates for other intermediate CAs as well as leaf digital certificates.** The trust for any leaf digital certificate can be traced back to the root CA through a chain of unforgeable certificates, which is what is called the chain of trust. 

**In Hyperledger Fabric developers created Fabric CA to function as a root CA as well as intermediate CA to be able to test as well as run business networks.**

Hyperledger Fabric Membership Services employ a similar chain of trust. The Root CA of the Hyperledger Fabric channel ecosystem can create intermediate CAs. The root CA can bridge into the legacy systems of the enterprise through a series of CAs, back to the public, well-accepted external root CA as well. This is how the Hyperledger Fabric Identity system functions in the context of large enterprises, and even cross-enterprise. The larger world of Identity Management systems in general is explained next.

## PKI: Authorization

Authorization is the ability to restrict an entity's access to certain read or write transactions. Deploying  or invoking chaincode is also implemented using the information available in the digital certificates.  **Hyperledger Fabric uses Role Based Access Control (RBAC).**

To summarize PKI, we have the following concepts: 
* Public and private key pairs.
* Digital certificates and revocation lists; the Hyperledger Fabric Identity system follows the X.509  standard.
* Certificate authorities and the chain of trust.
* Verification of the certificates and authorization.

## Membership Services

Membership Services authenticates, authorizes, and manages identities on a Hyperledger Fabric permissioned blockchain network. The membership services code that runs in peers and orderers both authenticates and authorizes blockchain operations.

* Hyperledger Fabric creates a transactional network where all participants have known  identities; these include organizations, network components, and end users or client applications.
* Public Key Infrastructure is used to generate cryptographic certificates which are  tied to these participants. As a result, user access control can be implemented on the network level, as well as on the channel level. 
* Channel in Hyperledger Fabric is a segregated sub-network consisting of two or more participant organizational units created for the purpose of conducting private and confidential transactions. 
* The concept of channels coupled with this access control helps address confidentiality and hence privacy of the data and chaincode deployment, execution and update.

## Membership Services 
### Identity
In permissioned blockchain systems, **Identity is essential, rich, decentralized, and reliable.**
* **Essential** 
All activity on permissioned systems requires Identity; it is foundational and needed before any activity can happen. Setting up channels, deploying chaincode, proposing transactions, ordering  transactions and participating in consensus, validating and endorsing transactions, querying the ledger,  administering nodes - all of these require Identity. 
* **Rich** 
Authentication, authorization and other identity management functions require access to many Identity attributes. **Hyperledger Fabric uses certificate-based identities (X.509 certificates) in the form of Enrollment Certificates (ECerts) for users, and Root Certificates (rootCerts) for members organizations.** 
We usually refer to the (member) organizations as the ones who form the consortium, and the users as the end nodes that belong to the consortium though one of the (member) organizations. 
    * Think about a hierarchy of companies and employees, where the companies form a consortium, and as part of the agreement, the companies add their employees (as users, belonging to these organizations).   The X.509 family of standards allows for a flexible set of attributes for Identity to be defined securely. 
* **Decentralized**
Can be consumed and validated locally, without relying on a central server.  All certificates  can be verified locally using public information cached locally, including revocations done using a CRL. This is due to the chain of trust created using the PKI. 

***Note: CRL contains the certificates that are no longer valid. So CRL is used to check that a certificate is still valid. If an impersonator tries to pass a compromised digital certificate to a CA, it can be first checked against the issuing CA’s CRL to make sure it’s listed as no longer valid***

* **Reliable**
Each participant in the network has an associated digital certificate issued by a CA, which in the  Fabric world, is implemented using Fabric-CA. **The issuing authority for the X.509 certificate can be tracked  back to a Certificate Authority that is reliable.**

### Authentication and Authorization
**Authentication** is the process of verifying Identity. 
* Hyperledger Fabric uses a PKI-based authentication scheme. The proof of possession of a secret (a private key) corresponding to the public key in the X.509 certificate authenticates the user's (or device's) Identity.

**Authorization** is the process of determining access rights and privileges to a resource or permission to perform specific actions. 
* Hyperledger Fabric uses the Role Based Authorization Control (RBAC) scheme, where each Identity is assigned a role. 
* The authorization policies are defined per resource or action, and relate to roles rather than specific identities. This provides better flexibility and agility, as roles can be reassigned if, for example, a specific employee leaves the enterprise or is on vacation.

## Fabric CA
Hyperledger Fabric CA is an out-of-the-box implementation of a Certificate Authority (CA) for use with Hyperledger Fabric. Fabric CA either registers Identities or connects to an existing LDAP to use as the user registry. Fabric CA issues, renews and revokes Enrollment Certificates and Root Certificates to network member organizations, their system components and their users, including administrators. All these certificates are in the X.509 format. Also, support for PKI means that Fabric-CA supports Certificate Revocation Lists (CRL). 

* **Fabric CA is using the client/server architecture** here, the server can be implemented as a cluster to support High Availability. As with any CA, the Fabric-CA can generate self-signed X.509 certificates.  

Multiple Fabric CAs can be started. Normally, this would follow the PKI chain of trust philosophy, where one of them is a root CA and the rest are intermediate CAs authenticated by the root CA.

Fabric CA is only provided as a default reference implementation of a CA. It can be replaced with another CA to generate appropriate certificates and support Revocation Lists.

***Note: LDAP is lightweight directory access protocol. It configured with Fabric CA to store the identity information of any particular user. It performs two major task i) Authenticate an identity prior to enrollment. ii) Retrieve an identity’s attributes values which are used for authorization.***

## Membership Service Provider(MSP)

The **Membership Service Provider(MSP) in Hyperledger Fabric is responsible for Identity Management functions in  the context of the Fabric blockchain network.**
* An implementation of MSP identifies which root CAs and intermediate CAs are trusted to define the members of a trust domain (e.g. an organization), either by listing the identities of their members, or by identifying which CAs are authorized to issue valid identities for their members or a combination of both. 
* **An MSP also enforces role-based authorization control within the scope of the organization which the MSP represents (e.g. administrators, or members of a sub-organization group), and sets the basis for controlling  access privileges in the context of the network and a channel (e.g. channel admins, readers, writers).** In this context, the  organization is a managed group of members.

* An organization is divided into multiple organizational units(OUs), each with a certain set of responsibilities.**When a CA issues X.509 certificates, the OU field in the certificate specifies the line of business to which the identity belongs.**

**The configuration of an MSP is broadcasted to all the channels where members of the corresponding organization participate this is called the  channel MSP** . 
* In addition to the channel MSP, peers, orderers, and  clients also maintain a local MSP  instance to authenticate member messages outside the context of a channel, and to  define the permissions over a particular component (who has the ability to install chaincode, for example).  The MSP also has to handle Certification Revocation Lists (CRLs), which we discussed in the PKI section.  Every node and user must have a local MSP which defines the permissions of that node and allows the user  to authenticate its transactions or as an administrator. Due to the hierarchical nature of the subgroups  during channel setup, this configuration requirement can be fulfilled quite easily. This results in local MSPs  for every type of peer.
The scope of channel MSPs is at the channel level; they define the administration and participation rights  on a channel level, which helps to create a chain of trust to expose identities of entities' members to other  participating entities at that level. Channel MSPs are named in the  configtxgen of the channel. Multiple  organizations participating in the channel have their own MSPs. 

**For example,** If organization A and  organization B participate in a channel, msp.A and msp.B will be defined in the channel genesis block. The names of MSPs have to be  unique in a channel. **The configuration elements and participants at the channel level, even though maintained at the organization level, are logically copied or accessible to every organization node on the channel and kept synchronized via consensus.** In the the above example, msp.A configuration elements are  available to nodes in organization B and vice versa. This enables employees at organization A to participate in  transactions in the same channel with organization B, helping to transcend the organization boundaries.  There is another level above this called a  Network Level. MSPs at the Network Level define the  members of the network and are authorized to perform network level administrative tasks, like creating of  channels.

### MSP Structure:
The scopes of these MSPs are different, but the most important function of an MSP at any level is the identification and interaction with root or intermediate CAs used to establish a chain of trust.
**Local MSP configuration is stored in a local folder with a specific structure. Usually, the structure is in the form of a file folder with subfolders for each type of element.** It is helpful to think of a channel MSP configuration this way, as well. Local MSPs are defined for every type of local node, like peer or orderer. Their configurations only apply locally. In addition to the elements we just talked about, local MSPs have the following attributes: 
**Node Identity**
The identity of the node; i.e. cryptographic material that, in combination with the  private key (held separately), would allow the node to authenticate itself in the messages that it sends  to other participants of its channels and network. This is mandatory for a local MSP.
**KeyStore for Private Key**
This contains the node’s private key. This key cryptographically matches the node’s public key present in the Node Identity X.509 certificate. This is used, for example, to sign a transaction proposal response, as part of the endorsement phase. The access to this key is restricted to identities of users who have administrative access. This item is mandatory for local MSPs, and must contain exactly one private key. Channel MSPs do not include this element, as they aim to offer identity validation functionality,and not signing ability.

## Channels
A Hyperledger Fabric channel is a segregated way of communication between two or more specific network members, for the purpose of conducting transactions. The channel structure is the only way in which Hyperledger Fabric business networks can be set up. A channel is defined by the following components: 
**1. Members (organization units)**
**2. The shared ledger**
**3. Chaincode**
**4. The ordering service.**

* Each transaction on the network is executed on a channel, where each party must be authenticated and authorized to transact on that channel. 
* Each peer that joins a channel has its own identity given by a Membership Services Provider (MSP), which authenticates each peer to its channel peers and services. **Channels have the advantage of providing confidentially.** 

Each and every concept described in all the preceding sections and chapters is valid only in the context of a Fabric channel. By default, a channel can include all participants in a network. **If private communications are needed, just the organizational units that need to participate in such private communication can create a separate channel where they are the only authorized members.**

No ledger data can pass from one channel to another. This separation of ledgers, by channel, is defined and implemented by configuration chaincode, the identity membership service and the gossip protocol. 
The dissemination of data, which includes information on transactions, ledger state and channel membership, is restricted to peers with verifiable membership on the channel. This isolation of peers and ledger data by channel, allows network members that require private and confidential transactions to coexist with business competitors on the same blockchain network.

### Channel Setup
To create a new channel, the client SDK calls the configuration system chaincode with parameters like policies, the MSP IDs and members (organizations). This creates a genesis block for the channel ledger, which stores configuration information about the channel policies and members. The genesis block is the first block in the channel's ledger. It contains only configuration information. When a new member is added to an existing channel, the member gets access to the appropriate information in the genesis block. The MSP ID has to be unique within channels.

The channel configuration is done using a collection of configuration transactions. Each collection consists of one or more versioned configuration transactions (configtx) in a grouped hierarchy. Configuration modification policies control the permissioning of changes to that configuration. The hierarchical structure permits the inheritance of policies for configurations deeper in the hierarchy from higher levels.

As we mentioned above, the configuration contains information about the Membership Services Provider attached to the channel. 

### Operating a Channel
Once a channel is set up, participants in the channel can deploy and invoke chaincode, engaging in all  activities that we have seen before - to propose, endorse, order and validate transactions, of course  limited by the rights granted them by their MSPs inherited from the channel configuration and interaction  with the CA.

Channel configuration can also be modified dynamically to add more participants and their own MSPs. T  his can only be done if one has the proper administration rights by being in a role that is permitted  to make these changes.

A very important result of the channel setup is increased privacy. Unlike public-permissionless blockchains  (as well as some of the other permissioned chains), Hyperledger Fabric segregates the activity of a channel  from participants who are not members of the channel; these outsiders cannot even see the frequency, nor  the size of the messages that pass between the participants of the channel. This increases the  privacy of the business transactions, also by shielding the chaincode from prying eyes.

## Hyperledger Composer 
**Hyperledger Composer is an open development tool set and framework to make developing blockchain applications easier.** 
* The goal is to accelerate time to value, and make it easier to integrate blockchain applications with the existing business systems. 


### Creating Application Using Hyperledger Composer 

Steps to creating an application using Hyperledger Composer include:

**1. Modeling assets participants and transactions to create a .cto file.**
**2. Writing transaction  functions  in Javascript as a  .js file.**
**3. Creating access control rules  as an  .acl file.**
**4. Creating a query definition  as a  .qry file.**

Together, these four types of files make up a  **Business Definition Network (BDN)**. 
**Business network cards** are a combination of an identity, a connection profile, and metadata, the metadata optionally containing the name of the business network to connect to. Business network cards simplify the process of connecting to a business network, and extend the concept of an identity outside the business network to a 'wallet' of identities, each associated with a specific business network and connection  profile.
**Connection profiles** are used across Hyperledger Composer to specify how to connect to an execution runtime. There are different configuration options for each type of execution runtime. For example, the connection profile for a Hyperledger Fabric v1.1 runtime will contain the TCP/IP addresses and ports for the Fabric peers, as well as cryptographic certificates, etc.



# Recap:
1. Peer can be part of one or more channel
2. Every channel has a separate ledger
3. Every Channel has one or more chain codes getting & setting values in the ledger
4. Every Chain code has a different endorsement policy
5. Chaincode must be installed in each peer that is part of the channel and instantiated.
6. When a Chaincode gets instantiated a policy (endorsing) has to be defined. [consensus: before a transaction can be recorded in the ledger only if a rule is met]