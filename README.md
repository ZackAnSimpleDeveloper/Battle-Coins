# ⚔️ Case Study: Online Multiplayer Game (REST-Based Economy & Security)

**Role:** Lead Game & Backend Developer  
**Tech Stack:** C#, Unity 2D/3D, REST APIs, Google Play Billing API, Token Authentication  
**Status:** Completed (Proprietary System / Case Study)

> ⚠️ *Note: The source code for this game and backend is private. This repository serves as a case study to showcase the architecture, security, and game economy implementations.*

---

### 🎥 Visual Demonstration

<p align="center">
  <img src="https://raw.githubusercontent.com/ZackAnSimpleDeveloper/Battle-Coins/main/image/fight1.jpeg" alt="Combat System" width="260"/>
  <img src="https://raw.githubusercontent.com/ZackAnSimpleDeveloper/Battle-Coins/main/image/bet_ur_coin.png" alt="Wagering System" width="260"/>
  <img src="https://raw.githubusercontent.com/ZackAnSimpleDeveloper/Battle-Coins/main/image/buy_skins.jpeg" alt="In-App Store" width="260"/>
</p>

---

### 🚨 The Technical Challenge
Building a competitive online game with real-money or virtual currency wagering requires high security and cost control:
- **Server Cost Optimization:** WebSockets and persistent server connections can quickly become expensive for early-stage games.
- **In-App Purchase Fraud:** Client-side purchase validation is highly vulnerable to hacking and spoofing.
- **Session Security:** Preventing unauthorized account access and state manipulation during online matches.

### 💡 The Solution
I engineered **Battle Coins**, a C# Unity online game built with a cost-effective, REST-driven backend architecture and server-side payment verification:

- **Cost-Optimized REST Architecture:** Instead of maintaining expensive persistent WebSocket connections, I implemented a lightweight RESTful API structure for matchmaking and turn-based wagering, drastically reducing infrastructure costs until scaling.
- **Server-Side Google Play Validation:** Implemented a secure In-App Purchase (IAP) workflow. Purchase tokens generated on the client side are sent directly to the backend server, which validates the payment status against Google Play Billing APIs before granting virtual coins or skins.
- **Token-Based Authentication:** Integrated time-limited access tokens for user login sessions, ensuring secure API calls and protecting user economy states.
- **Economy & Wagering System:** Developed a coin-staking mechanic where players wager virtual currency on battles, alongside a shop interface for unlocking character skins.

### 📈 Key Highlights
- **100% Secure Purchases:** Zero risk of local purchase tampering due to strict server-to-server verification.
- **Cost-Effective Infrastructure:** Reduced server overhead costs significantly while maintaining a smooth competitive gameplay loop.
- **Cross-Domain Expertise:** Seamlessly blended frontend game development in Unity with backend security and database integration.

---

### 🏗️ Technical Architecture Overview
1. **Client (Unity/C#):** Handles UI/UX, animations, local input, and sends REST requests with bearer tokens.
2. **Authentication Layer:** Issues short-lived JWT/Access Tokens to authorize player actions.
3. **Backend Service:** Processes matchmaking queues, validates Google Play receipts server-side, and manages player inventory database states.
