# 3Pals-08.14.25
**Projects-Payments-Platform Pals** 08.14.25 <br>
ENS-PayPal Staked Commerce @ ETHGlobal Hackathon: A decentralized comprehensive project platform - propose, design and create; underwrite, track, participate, build - featuring dynamic escrow-staking system using ENS domains (e.g., supplier.project.eth) to structure milestones, events, certifications, and payments. Chainlink oracles verify real-world milestones, while PayPal/PYUSD - Circle bridges fiat &amp; crypto. Enables dynamic performance staked projects, contracts, tasks, etc. 

# Title: Looking for partners to build this...

### Core (already chosen)
* **ENS + Chainlink Functions/Automation + PayPal (PYUSD)**
* **Walrus (sidecar storage):** store invoices/PoD media; put `sha256` + `walrus://id` on-chain.

---

## Hackathon Fit-Check: Easiest Add-ons from Sponsors

### LayerZero — _Omnichain state mirror_
* **Why:** Qualify for the **Best Omnichain Interaction** prize.
* **Hook:** On each milestone release, push a message to a mirror contract on a second chain. This logs the state change across chains.

    ```solidity
    releaseLog(projectId, milestoneId, proofHash);
    ```

### Circle — USDC Power-ups
* **CCTP v2:** Offer merchants "desired chain" payouts. The escrow is on one chain (e.g., Base), but the payment is delivered in USDC on the merchant's preferred chain.
* **Paymaster:** Let users pay gas fees in USDC, creating a smoother user experience by removing the need for native tokens.
* **Gateway (testnet):** Use this to give users a single USDC balance, enabling a chain-abstracted checkout experience.

### ENS — Prize Alignment
* **Best use of ENS:** Use milestone subnames (e.g., `2.supplier-alice.project.eth`), store Walrus URIs in ENS text records, and use CCIP-Read for L2 resolution.
* **L2 Primary Names:** Set reverse records on a supported L2 (Base, Optimism, Linea, or Arbitrum) for all project participants.

### Hardhat 3 — Tooling Prize
* **Why:** Hardhat is the standard for Solidity development. You're already using Solidity, so building and testing with Hardhat is a natural fit.
* **Hook:** Build and test your project with Hardhat 3. Include well-documented scripts and a clean README for your code.

### Dynamic or Privy — Embedded Wallets
* **Why:** These services can help you compete for "Best Consumer App" prizes by providing dead-simple onboarding. Users (suppliers and buyers) don't need to be crypto-native.
* **Hook:** Integrate embedded wallets with social or passkey login. Allow users to fund their accounts with PayPal/PYUSD or USDC.

### Lit Protocol (Vincent) — Delegation & Safety Rails
* **Why:** This adds a governance and operational layer to your project.
* **Hook:** Create a "Vincent Policy" that governs agent actions. For example, a policy could state: "An agent may call `requestRelease(milestoneId)` only if the oracle proof hash matches on-chain and the action is taken before a specific deadline."

### Walrus — Storage Prize
* **App use:** Build a feature for uploading invoices and proof-of-delivery documents (`invoice.json` / `deliveryProof.jpg`) to Walrus. Store the file hash on-chain for verification.
* **Dev tool angle:** Create a small Command Line Interface (CLI) that uploads files to Walrus and prints the `{ hash, uri }` to be used in continuous integration (CI) workflows.

Thank you. 
**Have your AI call my AI sometimes...**

--- 
This README contains two sections: 
1. **Project Overview** – a detailed description of …………. and its intended use.  
2. **License & Notices** – patent, usage restrictions, and licensing terms.

For inquiries, contact:  
Email: 1@1000x10.com  
dba: HalfHashd<sup>™</sup>

The HalfHashd welcomes inquiries for partnerships, licensing arrangements, and collaborative developments. Public good, government, and educational uses are invited to inquire for free use considerations.

## 2. License & Notices

### COPYRIGHT NOTICE

### MIT License + Commons Clause Restriction
Copyright (c) 2025 HalfHashd (dba)
---

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to use, copy, modify, merge, publish, and distribute the Software for personal, educational, or non-commercial purposes, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software. Certain aspects of this software and/or its underlying methods are patent pending. 

**Commercial Use Restriction:**  
The "Commons Clause" License Condition v1.0 is hereby added to the MIT License: 
You may not sell, rent, lease, offer as a service, or otherwise use the Software for a commercial purpose without express prior written permission from the copyright holder, except where specific free use permission is granted for public-interest or educational projects.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
