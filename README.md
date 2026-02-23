# Crypto Blockchain Simulation

A C++ implementation of a cryptocurrency blockchain system that simulates real-world blockchain behavior including mining, transaction handling, and proof-of-work.

## Overview

This project models how cryptocurrencies like Bitcoin operate at a fundamental level. The simulation implements a complete blockchain with SHA-256 hashing, proof-of-work mining that requires finding hashes with a specific number of leading zeros, and dynamic difficulty adjustment based on block generation time. It also includes a full transaction system with inputs, outputs, digital signatures, and UTXO (Unspent Transaction Output) tracking to manage wallet balances which is the same model Bitcoin uses.

## Features

- **Proof-of-Work Mining** – Mines blocks by finding nonces (32-bit numbers) that produce hashes with the required leading zeros (difficulty of 4 by default)
- **Dynamic Difficulty Adjustment** – Automatically adjusts mining difficulty every 10 blocks based on how fast blocks are being generated
- **Transaction System** – Full TxIn/TxOut model with coinbase transactions (mining rewards of 50 coins) and peer-to-peer transfers
- **UTXO Management** – Tracks unspent transaction outputs to validate balances and prevent double-spending
- **Digital Signatures** – Signs and verifies transactions to ensure only the owner can spend their coins
- **Chain Validation** – Validates block structure, timestamps, hashes, and genesis block consistency
- **Chain Replacement** – Implements the "longest chain wins" rule for resolving conflicts between peers

## Technologies Used

- C++
- SHA-256 hashing algorithm
- Vector-based blockchain structure

## How It Works

1. Genesis block is created and mined on startup
2. New blocks are mined by incrementing a nonce until the hash has enough leading zeros
3. Coinbase transactions reward miners with 50 coins
4. Users can send coins by creating signed transactions that consume UTXOs and create new ones
5. All transactions are validated to ensure inputs equal outputs and signatures are valid

## What I Learned

Building this project gave me a deep understanding of cryptographic hashing, proof-of-work mechanisms, and how the UTXO model prevents double-spending in decentralized systems.
