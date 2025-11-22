# Ethereum Interop Layer — React Demo

WARNING: DURING ETHGLOBAL BUENOS AIRES YOU **MUST** TO USE THE AMBIRE WALLET VERSION AVAILABLE AT THE EF EIL BOOTH OR ON OUR TELEGRAM. THIS DEMO APPLICATION WILL ONLY WORK WITH THIS VERSION OF THE AMBIRE WALLET.

A demonstration application showcasing the **Ethereum Interoperability Layer (EIL)** SDK for building trustless cross-chain applications using React, Viem and Wagmi in TypeScript.

## 🌟 Overview

This project demonstrates how to use the [EIL SDK](https://github.com/eth-infinitism/eil-sdk) to create seamless cross-chain user experiences.
It features a "Capture The Flag" game that operates across multiple chains simultaneously, showcasing three key EIL capabilities:

1. **Multi-Chain Execution** - Execute atomic operations across multiple chains.
2. **Cross-Chain Asset Transfers** - Move tokens between chains using EIL's voucher system.
3. **Dynamic Variables** - Use on-chain data to compute values at runtime.

## 📚 What is EIL?

The Ethereum Interoperability Layer (EIL) is a trustless protocol for cross-L2 interoperability.

**Learn more:**
- [EIL Official Documentation](https://docs.ethereuminteroplayer.com/)
- [EIL Blog Post](https://blog.ethereum.org/2025/11/18/eil)
- [EIL Research Paper](https://ethresear.ch/t/eil-trust-minimized-cross-l2-interop/23437)
- [EIL SDK Repository](https://github.com/eth-infinitism/eil-sdk)
- [EIL Contracts Repository](https://github.com/eth-infinitism/eil-contracts)

## 🛠️ Technology Stack

- **EIL**: @eil-protocol/sdk, @eil-protocol/accounts
- **Frontend**: React 19, TypeScript, Material-UI
- **Web3**: Wagmi, Viem, Reown AppKit, WalletConnect
- **Smart Contracts**: Hardhat, OpenZeppelin Contracts
- **State Management**: TanStack Query
- **Build Tool**: Vite

## 📋 Prerequisites

- Node.js (v24 or higher recommended)
- Yarn Classic package manager
- Testnet ETH and USDC on supported chains
- EIL-enabled version of Ambire wallet, or another Web3 wallet with explicit support for EIL\
  **Note: As of this writing, this experimental Ambire wallet version is only available on the EIL Discord server upon request.**

## 🔧 Installation

1. **Clone the repository:**

2. **Preprocess dependencies and compile contracts**
   ```bash
   yarn preprocess
   ```

3. **Start the development server:**
   ```bash
   yarn dev
   ```

4. **Open the application in your browser**

## 🎮 How to Use

1. **Connect Your Wallet**: Click the "Connect" button and link your Web3 wallet
2. **View Multi-Chain State**: The app displays account balances and flag holders on both chains
3. **Ensure Sufficient Balance**: Your account will need to pay ETH for gas on the origin chain
4. **Capture Flags**: Try three different demonstration modes:
    - **Simple Capture**: Execute independent operations on both chains
    - **Capture with Transfer**: Move USDC between chains while capturing flags
    - **Capture with Dynamic Variable**: Use on-chain computed values for transfer amounts

## 🔑 Key Concepts Demonstrated

### Multi-Chain Smart Account

The demo uses the `AmbireMultiChainSmartAccount` which implements the `IMultiChainSmartAccount` interface.

This provides:
- A single account address across multiple chains
- Unified signature management
- Atomic multi-chain execution

### Voucher System

EIL's voucher system enables trustless cross-chain asset transfers.

### Runtime Variables

Compute values on-chain during execution.

## 🌐 Supported Networks

WARNING: This demo is currently preconfigured for the EIL testnet chains operated by Tenderly.
It is not recommended to use this demo on other public chains.
