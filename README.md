# MumbaiVote
A decentralized voting smart contract for ETHGlobal Mumbai 2026.

## Overview
MumbaiVote is a decentralized voting smart contract designed to enable transparent, tamper-proof, and trustless decision-making on the Ethereum blockchain.

The system ensures one vote per user using address-based tracking and stores all voting data on-chain, making results verifiable and immutable. The contract is deployed on the Sepolia testnet and demonstrates core governance mechanisms such as proposal management, vote validation, and result computation.

This project represents an iteration and improvement of my earlier voting system, with cleaner structure, improved validation logic, and better alignment with real-world DAO governance patterns.

## 🧠 Problem Statement
Traditional voting systems lack transparency and are prone to manipulation. This project explores how blockchain-based voting can ensure immutability, transparency, and trustless participation.

## ⚙️ Architecture
User → MetaMask → Smart Contract (MumbaiVote.sol)

- Voting state stored on-chain using mappings
- Each address allowed only one vote
- Results computed dynamically from stored data

## 🔐 Security Considerations
- Prevents double voting using address-based mapping
- Input validation using require statements
- Uses Solidity ^0.8.x (built-in overflow protection)

## Deployment
- **Network**: Sepolia Testnet
- **Contract Address**: [https://sepolia.etherscan.io/address/0xd751cea6971bc0e213aed278ef6dfba49fce412c](https://sepolia.etherscan.io/address/0xd751cea6971bc0e213aed278ef6dfba49fce412c)

## Features
- **Proposals**: Predefined options ("Proposal A", "Proposal B").
- **Voting**: Users vote once for a proposal, tracked to prevent double-voting.
- **Result**: View the winning proposal with the highest votes.
- **Security**: Uses safe math (Solidity ^0.8.20) and input validation.

## Code Breakdown
`MumbaiVote.sol` implements a voting system:                                                 
- **Constructor**: Initializes the owner and two proposals ("Proposal A", "Proposal B").
- **Vote**: Allows one vote per user, tracked via a `voters` mapping, and emits a `Voted` event.
- **GetWinningProposal**: Returns the proposal with the most votes by iterating through a `Proposal` struct array.
- **Security**: Uses `require` to prevent double-voting and invalid proposals.

I learned how structs organize data, mappings track user actions, and loops determine results. Deploying via Remix was a smooth experience.

## Files
- **`MumbaiVote.sol`**: Defines the voting contract.
- **`LICENSE`**: MIT License, allowing open-source use.
- **`.gitignore`**: Node.js template with `artifacts/` for clean commits.
- **`README.md`**: This file, detailing my project and journey.

## 📈 Future Improvements
- Add frontend interface for better usability
- Integrate DAO-style governance
- Add off-chain identity verification (e.g., zk proofs)
- Deploy on Layer 2 for scalability

## Source
Built using [Solidity by Example’s voting template](https://docs.soliditylang.org/en/latest/solidity-by-example.html#voting), licensed under MIT. I customized the contract name and proposals while learning from the code.
  
## 🎯 Key Learnings
- Designed on-chain state management using mappings and structs  
- Implemented secure voting logic with input validation  
- Gained experience deploying and verifying smart contracts on testnet  

## Usage
- Compile and deploy `MumbaiVote.sol` in Remix (Solidity 0.8.20).
- Vote for a proposal via MetaMask.
- Check the winning proposal using `getWinningProposal`.
- Verify on Etherscan.

## License
Licensed under the MIT License—see [LICENSE](LICENSE).

## Contact
Email me at rishabhgupta78470@gmail.com or find me on X @rishabh_guptaz. Excited to connect at ETHGlobal Mumbai 2026!
