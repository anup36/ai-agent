
# AI Agent Framework


### 🌟 Key Features
- Agent Deployment: Deploy custom AI agents onto the Solana blockchain.
- Agent Interaction: Use natural language queries to interact with deployed agents.
- Market Analysis: Fetch real-time blockchain data, including market cap, top token holders, and trading activity


### 🛠 Framework Capabilities:
- Token Interaction: Query token metrics such as market cap and top holders.
- Trading Analysis: Identify trending tokens and analyze transaction data.


## 🚀 Quick Start
### Prerequisites
- Node.js (>= 16.x)
- npm (or yarn) installed
- A valid Bitquery API key
- read .env.example for rest of the Prerequisites

### Installation 
1. Clone the repository
``` bash 
git clone https://github.com/ai/ai-framework-v.1.git
cd ai-framework-v.1
```
2. Install dependencies:
``` bash
npm install
```
3. Set up environment variables: Create a .env file in the root directory and add the following variables:
 
```bash
PRIVATE_KEYPAIR=<YOUR_PRIVATE_KEYPAIR>
OPENAI_API_KEY=<YOUR_OPENAI_API_KEY> 
RPC_ENDPOINT=https://api.mainnet-beta.solana.com 
Add your Bitquery API in interactAgent.ts 
```
4. Build the Framework
```bash
npm run build
```

## 📜 Available Commands
1. Ask Queries to an Agent:
```bash
npm run ask {agentName} {yourQuestion}
```
   - example
   ```bash
   npm run ask Aura "What is the market cap of Solana?"
```
2. Deploy an Agent or Token:
- Go to defineAgent.ts and replace placeholders as you want. 
- Then Run,
```bash 
npm run build 
```
```bash
npm run deploy
```
- Deploys a new agent or token to the Solana blockchain.

3. Interact with an Agent:
```bash
npm run interact {agent_name} ask "Your question"
```
- Example 
```bash
npm run interact Aura ask "Trending token 24h"
```
4. Fetch Trending Tokens:
```bash 
npm run interact Aura ask "Trending token 24h"
```
5. Fetch Top Token Holders:
```bash
npm run interact Aura ask "Top holders: {mintAddress}"
```
- Example 
```bash
npm run interact Aura ask "Top holders: 6LKbpcg2fQ84Ay3kKXVyo3bHUGe3s36g9EVbKYSupump"
```
6. Fetch Market Cap Data:
```bash
npm run interact Aura ask "Marketcap count:{count} term:\"{term}\""
``` 
- Example
```bash
npm run interact Aura ask "Marketcap count:50 term:\"pump\""
```
7. Fetch First Top Buyers:
```bash
npm run interact {agentName} ask "First top {count} buyers for: {mintAddress}"
```
- Example 
```bash 
npm run interact Aura ask "First top 10 buyers for: 6LKbpcg2fQ84Ay3kKXVyo3bHUGe3s36g9EVbKYSupump"
```