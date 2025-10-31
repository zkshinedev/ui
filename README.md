# zkShine DApp Interface

![Solana](https://img.shields.io/badge/Built_for-Solana-14F195?logo=solana&logoColor=white)
![UI](https://img.shields.io/badge/Frontend-Next.js_React-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Version-0.3.0--alpha-yellow)

> **zkShine UI** is the decentralized application (DApp) interface for zkShine — providing a unified dashboard for privacy transactions, zk compute, VPN routing, and node management on **Solana**.

---

## 🧠 Overview

zkShine UI connects directly to Solana wallets and zkShine nodes, offering end-users and operators a **privacy-first Web3 experience**.

```console
Wallet → zkShine DApp → Privacy Relayer → zkCompute Node → Solana Blockchain

Core Features
Feature	Description
💸 Private Transactions	Send & receive SOL or SPL tokens through zkShine relay.
🧠 ZK Compute Dashboard	Visual interface for confidential proof generation.
🌐 Web3 VPN Gateway	Activate on-chain VPN sessions for private RPC and browsing.
🔒 Confidential Vault	Manage encrypted files, credentials, and zkKYC proofs.
🛰️ Node Operator Console	Monitor uptime, relay count, and compute load of zkShine Nodes.
🧱 Solana Native Integration	Seamless Phantom, Backpack, and Solflare wallet support.

⚙️ Tech Stack
- Next.js 14 (App Router)
- React + TailwindCSS
- Solana Wallet Adapter
- TypeScript
- Framer Motion (UI animations)
- Recharts (data visualization)

Installation
Prerequisites
Node.js >= 18
Yarn or npm

Clone and Run
git clone https://github.com/zkshinedev/ui.git
cd ui
yarn install
yarn dev


Then open:
👉 http://localhost:3000

Directory Structure
/app
  /dashboard
  /wallet
  /vpn
  /relay
  /vault
  /node
/components
  /ui
  /charts
  /modals
/lib
  /solana
  /zkshine
/public
  /assets

Wallet Integration
import { useWallet } from "@solana/wallet-adapter-react";

export const ConnectWallet = () => {
  const { connect, connected, publicKey } = useWallet();

  return (
    <button onClick={connect}>
      {connected ? `Connected: ${publicKey.toBase58().slice(0, 6)}...` : "Connect Wallet"}
    </button>
  );
};

Build for Production
yarn build
yarn start


Deploy to Vercel or zkShine’s DApp Gateway:

https://dapps.zkshine.xyz

Documentation
- DApp Integration Guide: https://docs.zkshine.xyz/ui
- Wallet Setup: https://docs.zkshine.xyz/ui/wallet
- VPN Gateway Docs: https://docs.zkshine.xyz/vpn
- Node Dashboard API: https://docs.zkshine.xyz/node

