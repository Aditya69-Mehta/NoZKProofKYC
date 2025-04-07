# No ZK Proof KYC

A simple decentralized KYC (Know Your Customer) system built on Ethereum using Solidity. This version does **not** implement Zero-Knowledge Proofs, focusing instead on basic hashed identity storage and verification mechanisms. It serves as a foundational prototype for understanding how KYC data can be securely stored and accessed on-chain in a permissioned manner.

---

## 🛠 Tech Stack

- **Smart Contract:** Solidity, Hardhat  
- **Frontend:** HTML, CSS, JavaScript (vanilla)  
- **Blockchain Network:** Ethereum (via Alchemy RPC)  
- **Security:** Hashing using `keccak256` for identity obfuscation  
- **Tools:** MetaMask, Hardhat, Ethers.js

---

## 🚀 Features

- Users can register themselves for KYC by submitting their name, age, and a hashed ID.
- Verifiers can approve or reject KYC requests.
- Only authorized verifiers can access or approve user KYC.
- Simple, minimal frontend for interaction with smart contract.
- No off-chain storage — everything is handled on-chain (except for user-facing UI).

---

## 📁 Project Structure

