# mnee-automatic-finance-os
MNEE Autonomic Finance OS is a programmable finance system where the MNEE stablecoin enforces on-chain policies to move, pause, or freeze funds automatically. It features negative-permission execution, self-healing behavior, and dry-run simulation for safer autonomous payments.
MNEE Autonomic Finance OS
Overview
MNEE Autonomic Finance OS is a programmable finance system built using the MNEE USD-backed stablecoin on Ethereum.
The project demonstrates how money can operate autonomously using on-chain policies instead of relying on manual approvals.
Funds are locked into a smart contract treasury, and from that point onward, predefined rules decide whether money should execute, pause, or freeze. Payments happen automatically by default unless a blocking condition such as time restrictions or risk flags is detected.
Problem Statement
Even with stablecoins, most financial workflows still depend on manual approvals. Someone must release funds, approve transactions, or intervene during disputes. This creates friction, delays, and human risk.
This project explores a different model where money itself enforces rules, similar to real financial infrastructure.
Solution
MNEE Autonomic Finance OS introduces:
A policy-driven treasury smart contract
Negative-permission execution (execute unless blocked)
Dry-run simulation before real transfers
Self-healing behavior when risk conditions change
The system separates decision logic from execution logic, making financial behavior predictable and transparent.
Key Features
🔐 Treasury Locking
Funds are deposited and locked into a smart contract.
⏱️ Time-Based Execution
Payments execute only after a defined release time.
🚨 Risk Flag Control
Execution freezes automatically when risk is active.
🧪 Dry-Run / Simulation
Test execution outcomes without moving real tokens.
⚙️ Negative-Permission Model
Money moves by default unless explicitly blocked.
🔁 Self-Healing Finance
Execution resumes automatically once risk is removed.
Architecture
code:

User Wallet (MetaMask)
        ↓
Frontend (Netlify / Web)
        ↓
Smart Contract (Ethereum Sepolia)
        ↓
MNEE ERC-20 Stablecoin

Frontend: Static web app
Backend: Ethereum smart contract
Data Layer: Blockchain (no traditional database)
Tech Stack
Solidity – Smart contracts
Ethereum (Sepolia Testnet) – Blockchain network
MNEE Stablecoin (ERC-20) – Programmable money
React / Web Frontend – User interaction
Netlify – Free frontend deployment
MetaMask – Wallet connection
How It Works
User connects wallet
User deposits MNEE into treasury
Contract evaluates execution policies
Simulation can be run (no funds move)
Execution happens automatically if allowed
Risk flag instantly freezes or resumes execution
Deployment
Smart Contract
Deployed on Ethereum Sepolia Testnet
Tools: Remix / Hardhat
Frontend
Deployed for free on Netlify
Only compiled frontend files are hosted
Demo Flow
Connect wallet
Deposit MNEE
Run dry-run simulation
Observe automatic execution
Trigger risk → execution freezes
Remove risk → execution resumes
Use Cases
Autonomous treasuries
Automated payouts
Policy-controlled finance
AI-assisted spending systems
Trust-minimized financial coordination
Why This Matters
This project shows how stablecoins can evolve from passive assets into active, policy-driven financial systems.
Instead of humans controlling every step, rules define behavior — and money follows them.
Author
Tharun
Hackathon Project – Programmable Finance & Automation
License
MIT License
