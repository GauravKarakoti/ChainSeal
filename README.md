# ChainSeal: Blockchain Document Notarization  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  
> **Immutable proof-of-existence for contracts, IP, and legal documents**  

## 🔍 Overview  
ChainSeal anchors document hashes to Ethereum/Polygon, issuing NFT certificates for tamper-proof verification. Designed for Korean SMEs and global Web3 teams.  

## ✨ Features  
- **1-Click Notarization**: Upload documents → mint NFT certificates.  
- **ZK Verification**: Prove document integrity without revealing content.  
- **Korea-Compliant**: Integrates PASS for KYC and meets FSC guidelines.  
- **DeFi Ready**: Embed certificates in DAO proposals or tokenized asset contracts.  

## 🛠 Tech Stack  
| Layer          | Technology              |  
|----------------|-------------------------|  
| **Blockchain** | Ethereum, Polygon       |  
| **ZK Proofs**  | Circom, SnarkJS         |  
| **Storage**    | IPFS, Filecoin          |  
| **Frontend**   | Next.js, Chakra UI      |  
| **Backend**    | Hardhat, Node.js, Express|  

## 🚀 Getting Started  

### Prerequisites  
- Node.js v18+  
- MetaMask (or Kaikas for Korean users)  
- IPFS node (Pinata or Infura)  

### Installation  
```bash  
git clone https://github.com/chainseal/chainseal-core.git  
cd chainseal-core  
npm install  
cp .env.example .env  # Set ETH_RPC_URL, POLYGON_RPC_URL, IPFS_API_KEY
```

## Deployment
```bash
# Deploy contracts (Ethereum + Polygon)  
npx hardhat run scripts/deploy.js --network ethereum  
npx hardhat run scripts/deploy.js --network polygon  

# Generate ZK circuits  
npx circom circuits/docProof.circom --r1cs --wasm
```

## Run Frontend
```bash
cd frontend  
npm install  
npm run dev  # http://localhost:3000
```

## 📖 Usage
1. Notarize a Document:
  - Upload a PDF at `/upload` → metadata hashed → NFT minted on Polygon.
  - Receive a QR-verifiable certificate.
2. Verify via ZK Proof:
  - Go to `/verify` → submit document + proof → confirm integrity on-chain.

## 🌍 Partners
- Korea: PASS identity system, Seoul Fintech Lab.
- Global: Chainlink (oracles), Filecoin (storage).
