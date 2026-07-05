# 🟠 Stellar Crowdfund - Orange Belt

A complete end-to-end decentralized crowdfunding dApp built on Stellar Testnet with Soroban smart contracts, full test coverage, and live deployment.

## 🌐 Live Demo

**[https://stellar-orangebelt.vercel.app](https://stellar-orangebelt.vercel.app)**

## 🎥 Demo Video

**[Watch 1-minute Demo on Google Drive](https://drive.google.com/file/d/11J72K3sNyohxmhqD0uChJvoWd_aY8IoK/view?usp=drive_link)**

## 🚀 Features

- 🔗 Multi-wallet support (Freighter, Lobstr, xBull)
- 📊 Real-time campaign progress bar with % complete
- ⏱️ Basic caching implementation (15s cache with timestamp)
- ⏳ Loading states and progress indicators
- 💝 Donate XLM directly to Soroban smart contract
- 🔄 Transaction status tracking (pending/success/failed)
- ❌ 3 error types handled: wallet not found, rejected, insufficient balance
- 📜 Contract info with deploy TX hash

## 📋 Contract Info

- **Contract ID:** `CDCWAY4OJ4QC3KEPOWJTIMQSRT66TV4ISXCP7MR4MX2K52IP322A22S4`
- **Network:** Stellar Testnet
- **Deploy TX:** `ded012df0cb2c784b2255597bbd247c5ffa3bc11c7911b71e191676ca5ac806e`
- **Initialize TX:** `a7ec37425b868850b3e0afa36376738504621d4ea6df5f55988ffcf794cf1e0b`

## 🧪 Tests

4 tests passing ✅

```
running 4 tests
test test::test_initialize ... ok
test test::test_goal_not_reached ... ok
test test::test_donate ... ok
test test::test_goal_reached ... ok
test result: ok. 4 passed; 0 failed
```

![Test Output](./screenshots/tests-passing.png)

## 🛠️ Tech Stack

- React + Vite
- Rust + Soroban SDK
- @stellar/stellar-sdk
- @stellar/freighter-api
- Stellar Testnet (Horizon + Soroban RPC)
- Vercel (deployment)

## ⚙️ Setup Instructions

### Prerequisites
- Node.js (v18+)
- Rust + Cargo
- Stellar CLI
- Freighter Wallet browser extension

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Open `http://localhost:5173`

### Smart Contract Setup

```bash
cd crowdfund-contract
stellar contract build
stellar contract deploy \
  --wasm target/wasm32v1-none/release/hello_world.wasm \
  --source deployer \
  --network testnet
```

### Run Tests

```bash
cd crowdfund-contract
cargo test
```

### Contract Functions

- `initialize(owner, goal, deadline)` - Initialize campaign
- `donate(donor, amount)` - Donate XLM in stroops
- `get_state()` - Get campaign state
- `is_goal_reached()` - Check if goal is met

## 📸 Screenshots

### Main App
![Main App](./screenshots/main-app.png)

### Wallet Options
![Wallet Modal](./screenshots/wallet-modal.png)

### Donation Successful
![Donation Success](./screenshots/donation-success.png)

## 🔗 Links

- **Live Demo:** https://stellar-orangebelt.vercel.app
- **Demo Video:** https://drive.google.com/file/d/11J72K3sNyohxmhqD0uChJvoWd_aY8IoK/view?usp=drive_link
- **Contract on Stellar Expert:** https://stellar.expert/explorer/testnet/contract/CDCWAY4OJ4QC3KEPOWJTIMQSRT66TV4ISXCP7MR4MX2K52IP322A22S4

## Built For

[Stellar Orange Belt Challenge](https://risein.com) 🟠
