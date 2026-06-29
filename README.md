# E-Auction Using Blockchain

A Blockchain-Based Blind Auction System that enables secure, transparent, and tamper-resistant auctions using smart contracts. This project implements blind bidding, a reveal phase, and on-chain auction settlement so bids remain private until revealed and winners are determined in a trustless way.

**🔗 [Project Report](https://github.com/SulavBaskota/E-Auction-Using-Blockchain/raw/main/Project%20Report.pdf)**

## Table of Contents

- [Project Structure](#️-project-structure)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Install & Setup](#install--setup)
  - [Compile & Test Contracts](#compile--test-contracts)
  - [Deploying Contracts](#deploying-contracts)
  - [Frontend](#frontend)
- [Available Scripts](#available-scripts)
- [Key Technologies](#key-technologies)

## 🗂️ Project Structure
- /client → Frontend app built with Next.js
- /web3 → Solidity smart contracts and deployment scripts

## Features

- 🔒 Blind bidding: Bidders submit hashed (sealed) bids keeping amounts private during the bidding phase.
- 🔓 Reveal phase: Bidders reveal their bids later to determine the winner.
- 🧾 On-chain settlement: Smart contract enforces auction rules and transfers funds / assets.
- 🧑‍⚖️ Owner controls: Auction creation and start/end times managed by the auction owner, and administrative tasks by admins.
- 🔁 Refunds: Losing bidders can reclaim funds as implemented in the contract logic.
- 📢 Events & logs: Contract emits events for important state changes to support UIs and off-chain listeners.
- ✅ Tests: Unit tests for smart contract logic to ensure correctness and security.

## 🧩 Tech Stack
- **Smart Contracts:** Solidity, Hardhat, Ethereum testnet
- **Frontend:** React.js, Next.js, Mantine UI, ethers.js
- **Wallet Integration:** MetaMask
- **Storage:** IPFS
- **Utilities:** ThirdWeb, JSON-RPC
- **Dev Tools:** JavaScript, Ganache

## Getting Started

### Prerequisites

- Node.js (v14+ recommended) and npm or yarn
- npm or yarn for JS dependencies
- A local Ethereum node or test network (Ganache)
- MetaMask wallet for UI testing

### Install & Setup

1. Clone the repository
```bash
git clone git@github.com:SulavBaskota/E-Auction-Using-Blockchain.git
cd E-Auction-Using-Blockchain
```

2. Install dependencies
```bash
cd web3
npm install
```

3. Set up environment variables
```bash
cp .env.example .env
```

### Compile & Test Contracts

Using Hardhat:
```bash
# Compile
npx hardhat compile

# Run tests
npx hardhat test
```

### Deploying Contracts

1. Start a local node:
```bash
# Hardhat local node
npx hardhat node
```

2. Deploy to the local network:
```bash
npx hardhat deploy --network <network>
```

### Frontend

1. Navigate to client directory
```bash
cd client
npm install
```

2. Run the development server
```bash
npm start
# or
yarn start
```

Open the UI at http://localhost:3000.

## Available Scripts
- `npx hardhat compile` — Compile smart contracts
- `npx hardhat test` — Run contract tests
- `npx hardhat node` — Start local development network
- `npx hardhat deploy --network <network>` — Deploy contracts
- `npm start` — Start frontend dev server
- `npm run build` — Build frontend for production

## Key Technologies

| Technology | Purpose |
|---|---|
| Solidity | Smart contract language |
| Hardhat | Local blockchain development & deployments |
| Ethers.js | Interact with contracts from JS |
| React | Frontend UI |
| Ganache | Local test blockchain |
| IPFS | Decentralized File Storage |
| Node.js / npm | Tooling and scripts |
