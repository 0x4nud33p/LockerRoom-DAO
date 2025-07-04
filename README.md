# LockerRoom DAO ⚽

> A decentralized autonomous organization platform built for sports teams and fan communities on Chiliz Chain

[![Demo](https://img.shields.io/badge/Demo-Live-green?style=for-the-badge)](https://lockerroom-dao.vercel.app)
[![Video](https://img.shields.io/badge/Demo_Video-Watch-red?style=for-the-badge)](https://youtu.be/VfwJEIsHJMY)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)
[![Chiliz](https://img.shields.io/badge/Built_on-Chiliz_Chain-orange?style=for-the-badge)](https://chiliz.com)

## 🏆 Overview

LockerRoom DAO is a comprehensive DAO platform designed specifically for sports teams and fan communities. Built on Chiliz Chain with Thirdweb SDK integration, it enables teams to create their own DAOs with treasury management, proposal voting, and exclusive access control through NFT membership passes.

### 🎯 Key Features

- **DAO Factory**: Deploy team-specific DAOs with one click
- **ERC721 Access Pass**: Mintable NFT membership system using CHZ
- **Proposal System**: Create and vote on community proposals
- **Treasury Management**: Automated CHZ distribution to successful proposals
- **Modern UI**: Polished interface with smooth animations
- **Mobile Responsive**: Optimized for all device sizes

## 🚀 Live Demo

- **Frontend**: [lockerroom-dao.vercel.app](https://lockerroom-dao.vercel.app)
- **Demo Video**: [Watch on YouTube](https://youtu.be/demo-placeholder)

## 🛠 Tech Stack

### Blockchain
- **Chain**: Chiliz Testnet (via Ankr RPC)
- **Smart Contracts**: Solidity ^0.8.19
- **Development Framework**: Foundry
- **SDK**: Thirdweb SDK v4

### Frontend
- **Framework**: Next.js 14 (App Router)
- **Styling**: TailwindCSS
- **Animations**: Framer Motion
- **Wallet Connection**: Thirdweb Connect
- **Deployment**: Vercel

### Infrastructure
- **RPC Provider**: Ankr
- **IPFS**: Thirdweb Storage
- **Package Manager**: pnpm

## 📦 Deployed Contracts

| Contract  | Description |
|-----------------------|
| DAOFactory | Factory for deploying team DAOs |
| LockerRoomDAO | Main DAO implementation |
| DaoAccessPass | ERC721 membership NFT |
| Treasury | Treasury management contract |

## 🏗 Project Structure

```
lockerroom-dao/
├── contracts/                 # Smart contracts
│   ├── src/
│   │   ├── DAOFactory.sol
│   │   ├── LockerRoomDAO.sol
│   │   ├── DaoAccessPass.sol
│   │   └── Treasury.sol
│   ├── script/               # Deployment scripts
│   ├── test/                 # Contract tests
│   └── foundry.toml
├── frontend/                 # Next.js application
│   ├── app/
│   ├── components/
│   ├── lib/
│   ├── public/
│   └── package.json
└── README.md
```

## 🚦 Getting Started

### Prerequisites

- Node.js 18+
- pnpm
- Foundry
- Git

### 1. Clone Repository

```bash
git clone https://github.com/0x4nud33p/LockerRoom-DAO.git
cd lockerroom-dao
```

### 2. Smart Contract Setup

```bash
cd contracts

# Install Foundry dependencies
forge install

# Compile contracts
forge build

# Run tests
forge test

# Deploy to Chiliz Testnet
forge script script/DeployAll.s.sol --rpc-url $CHILIZ_RPC_URL --private-key $PRIVATE_KEY --broadcast
```

### 3. Frontend Setup

```bash
cd frontend

# Install dependencies
pnpm install

# Start development server
pnpm dev
```

Visit `http://localhost:3000` to view the application.

## ⚙️ Configuration

### Smart Contract Environment Variables

Create `contracts/.env`:

```env
# Chiliz Testnet RPC
CHILIZ_RPC_URL=https://rpc.ankr.com/chiliz_testnet

# Deployment wallet private key
PRIVATE_KEY=your_private_key_here

# Etherscan API key for verification
ETHERSCAN_API_KEY=your_etherscan_api_key
```

### Frontend Environment Variables

Create `frontend/.env.local`:

```env
# Thirdweb Configuration
NEXT_PUBLIC_THIRDWEB_CLIENT_ID=your_thirdweb_client_id
THIRDWEB_SECRET_KEY=your_thirdweb_secret_key

# Chain Configuration
NEXT_PUBLIC_CHAIN_ID=88882
NEXT_PUBLIC_RPC_URL=https://rpc.ankr.com/chiliz_testnet

# App Configuration
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

## 🚀 Deployment

### Smart Contracts (Foundry)

1. **Compile contracts**:
```bash
forge build
```

2. **Deploy to Chiliz Testnet**:
```bash
forge script script/Deploy.s.sol \
  --rpc-url https://rpc.ankr.com/chiliz_testnet \
  --private-key $PRIVATE_KEY \
  --broadcast \
  --verify
```

3. **Verify contracts**:
```bash
forge verify-contract <CONTRACT_ADDRESS> src/DAOFactory.sol:DAOFactory \
  --chain chiliz-testnet \
  --etherscan-api-key $ETHERSCAN_API_KEY
```

### Frontend (Vercel)

1. **Build application**:
```bash
cd frontend
pnpm build
```

2. **Deploy to Vercel**:
```bash
vercel --prod
```

Or connect your GitHub repository to Vercel for automatic deployments.

## 🎮 How to Use

### For Team Admins
1. **Connect Wallet**: Use MetaMask or Thirdweb Connect
2. **Create DAO**: Deploy a new team DAO via the factory
3. **Mint Access Passes**: Create NFT memberships for fans
4. **Manage Treasury**: Set funding allocations and thresholds

### For Fans/Members
1. **Purchase Access Pass**: Mint NFT with CHZ to join DAO
2. **Create Proposals**: Submit funding requests or initiatives
3. **Vote on Proposals**: Participate in community governance
4. **Claim Rewards**: Receive CHZ for successful proposals

## ✨ Features & Bonus Points

### Core Features
- ✅ DAO Factory with team customization
- ✅ ERC721 Access Pass system
- ✅ Proposal creation and voting
- ✅ Treasury management with CHZ distribution
- ✅ Thirdweb SDK integration
- ✅ Foundry deployment pipeline

### Bonus Features
- ✅ **Polished UI**: Clean, modern interface design
- ✅ **Smooth Animations**: Framer Motion micro-interactions
- ✅ **Mobile Responsive**: Optimized for all screen sizes
- ✅ **Dark Mode**: Toggle between light/dark themes
- ✅ **Real-time Updates**: Live proposal and voting status
- ✅ **Gas Optimization**: Efficient contract implementations
- ✅ **Error Handling**: Comprehensive user feedback
- ✅ **Loading States**: Skeleton screens and progress indicators

## 🧪 Testing

### Smart Contracts
```bash
cd contracts

# Run all tests
forge test

# Run with verbosity
forge test -vvv

# Run specific test file
forge test --match-path test/DAOFactory.t.sol

# Coverage report
forge coverage
```

### Frontend
```bash
cd frontend

# Run tests
pnpm test

```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/0x4nud33p)
- Twitter: [@yourtwitter](https://twitter.com/0x4nud33p)

## 🙏 Acknowledgments

- [Chiliz Chain](https://chiliz.com) for the sports-focused blockchain infrastructure
- [Thirdweb](https://thirdweb.com) for the comprehensive Web3 development tools
- [Foundry](https://getfoundry.sh) for the fast and flexible smart contract development
- [Ankr](https://ankr.com) for reliable RPC infrastructure

---

Built with ❤️ for the sports community on Chiliz Chain