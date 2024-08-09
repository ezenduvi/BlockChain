#Blockchain

This project involves building a simple blockchain peer-to-peer network using concepts like UDP communication, synchronization, consensus mechanisms, messaging strategies, and state handling. 
The goal is to create a blockchain where each block contains messages, a nonce, a hash with a specified difficulty level, and other relevant metadata.

## Features

- **Blockchain Peer:** Stores messages in blocks, each with a miner's name, nonce, hash, height, and messages.
- **Proof-of-Work Consensus:** Mining involves finding a nonce that satisfies the hash difficulty requirement.
- **Gossip Protocol:** Nodes join the network via gossiping and keep alive by re-gossiping every 30 seconds.
- **Consensus Mechanism:** Ensures all peers agree on the longest valid chain through regular consensus checks.
- **Peer Management:** Tracks and updates the list of peers, handles peer communication and block requests.

## Protocols Implemented

- **GOSSIP:** Announce peer to the network and reply to gossip messages.
- **GET_BLOCK:** Request and receive specific blocks from peers.
- **CONSENSUS:** Trigger a network-wide consensus to verify the longest valid chain.
- **STATS:** Obtain and share the blockchain's height and hash information.

