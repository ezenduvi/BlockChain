## Blockchain

This project involves developing a decentralized peer-to-peer network that implements a basic blockchain. The blockchain consists of blocks containing messages, a nonce, and a hash that satisfies a proof-of-work requirement. The main focus is on understanding and implementing core blockchain principles such as UDP communication, consensus algorithms, message synchronization, and peer management.

## Project Summary

The blockchain is structured to simulate a network where each node (peer) can communicate with others, mine new blocks, and reach consensus on the blockchain's state. Key components include message handling, proof-of-work mining, gossip protocol for peer communication, and a robust consensus mechanism to ensure network integrity.

## Key Features

### 1. **Blockchain Peer**
   - Each peer in the network maintains its own copy of the blockchain.
   - Blocks store data such as messages, miner's name, nonce, hash, and block height.
   - Peers can request blocks from others to synchronize their chains.

### 2. **Proof-of-Work (PoW) Consensus**
   - The blockchain uses a PoW mechanism where mining involves solving a cryptographic puzzle.
   - Miners find a nonce that, when hashed with the block's contents, produces a hash with a specified number of leading zeroes.

### 3. **Gossip Protocol**
   - Nodes join the network using the gossip protocol, announcing their presence to others.
   - Nodes re-gossip every 30 seconds to maintain connectivity and update the peer list.

### 4. **Consensus Mechanism**
   - The network uses a longest-chain rule to achieve consensus.
   - Regular consensus checks ensure that all peers agree on the most valid chain.

### 5. **Peer Management**
   - Each peer keeps track of other active peers in the network.
   - The peer list is regularly updated, and inactive peers are removed to keep the network healthy.

## Protocols Implemented

### **GOSSIP**
   - Peers announce themselves to the network and respond to gossip messages to learn about other peers.

### **GET_BLOCK**
   - Allows peers to request specific blocks from others to synchronize their blockchain.

### **CONSENSUS**
   - Initiates a consensus process across the network to verify and adopt the longest valid blockchain.

### **STATS**
   - Peers can request and share blockchain statistics, including the current height and latest block hash.

## Running the Blockchain Peer

To start a peer, execute the following command:

```bash
python blockchain_peer.py --host [HOST] --port [PORT] --name [NAME]
