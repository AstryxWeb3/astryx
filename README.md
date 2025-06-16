# Astryx

Astryx is an open-source infrastructure hub designed for decentralized AI agents. It enables developers to easily create, deploy, and manage intelligent, reactive, and autonomous dApps (AI-driven applications) with high efficiency and minimal costs. Powered by the Solana blockchain, Astryx aims to redefine how AI interacts with decentralized systems.

[![Version](https://img.shields.io/badge/version-1.0-blue)](https://astryx.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![API](https://img.shields.io/badge/api-online-brightgreen)](https://api.astryx.org)

---

## 🌐 Vision

Astryx is built around the idea that AI agents are the natural evolution of smart contracts. These agents are capable of adapting to changing conditions, enabling a new class of applications that are intelligent, autonomous, and responsive.

> “AI agents are not just reactive, they’re proactive. They make decisions, adapt to data, and self-optimize.”

---

## ⚙️ Key Features

* **AI Agent Framework**: Build, register, and manage AI agents using a simple API.
* **On-Chain Interoperability**: Seamlessly integrate AI agents with smart contracts and Solana-based dApps.
* **OpenAI Assistant Integration**: Easily connect to ChatGPT-based agents.
* **Decentralized Execution**: Agents run in a verifiable and trustless way.
* **Real-Time Adaptability**: Agents learn and update based on external events.
* **Developer SDKs**: Available in TypeScript, Python, and Rust.
* **Agent Templates**: Pre-configured starter templates for popular use cases.
* **Agent Marketplace**: Discover, test, and fork public AI agents.
* **Webhooks & Plugins**: Connect agents to off-chain apps.
* **Built-in Monitoring**: Track agent behavior and usage logs.

---

## 🚀 Getting Started

```bash
# Clone the repo
$ git clone https://github.com/astryx-org/astryx.git
$ cd astryx

# Install dependencies
$ npm install

# Start the dev server
$ npm run dev
```

For more detailed developer onboarding, visit: [docs.astryx.org](https://docs.astryx.org)

---

## 🧠 AI Agent Example

```ts
// src/agents/price_monitor.ts
import { createAgent } from 'astryx-sdk';

createAgent({
  id: 'agent_price_watch',
  model: 'gpt-4',
  trigger: 'priceDrop',
  threshold: 10,
  action: async (context) => {
    await context.sendAlert(`Price dropped by 10%! Current: ${context.price}`);
  }
});
```

---

## 📡 API Reference

All requests are made to: `https://api.astryx.org`

### Create Agent

```http
POST /v1/agents
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json

{
  "name": "market-guard",
  "trigger": "onChainData",
  "model": "gpt-4",
  "callback_url": "https://yourdapp.com/agent-handler"
}
```

### Agent Chat

```http
POST /v1/chat
Authorization: Bearer YOUR_API_KEY

{
  "agent_id": "agent_market_guard",
  "message": "What happened to the BTC price today?"
}
```

### Get Agent Logs

```http
GET /v1/agents/{agent_id}/logs
Authorization: Bearer YOUR_API_KEY
```

### Delete Agent

```http
DELETE /v1/agents/{agent_id}
Authorization: Bearer YOUR_API_KEY
```

---

## 🧰 Developer Toolkit

* **SDKs**: `astryx-sdk` (JS/TS), `astryx-py`, `astryx-rs`
* **CLI**: `npx astryx init`
* **Templates**: `astryx/templates`
* **Agent Studio UI**: (Coming soon)
* **Simulation Tools**: Run dry-runs of agents before deployment.
* **Type Definitions**: Built-in schema validation for all agent inputs/outputs.

---

## 🌍 Why Solana?

* **High Throughput**: Supports thousands of transactions per second.
* **Low Fees**: Optimized for microtransactions.
* **Scalability**: Suited for agent-based apps that require frequent updates.
* **Community**: Thriving ecosystem of devs and users.
* **Compression Support**: Reduced data costs for agents using compressed state.

---

## 🔐 Security

* Agent code is verified and stored via IPFS or Arweave.
* On-chain signatures validate external requests.
* Optional zero-knowledge proof support (coming soon).
* Access tokens follow best practices with OAuth2 and JWT.
* Built-in rate limiting and abuse prevention.

---

## 📂 Folder Structure

```
astryx/
├── src/
│   ├── agents/           # AI agents you define
│   ├── lib/              # Helper utilities
│   └── ui/               # React components
├── public/
├── docs/                 # GitBook documentation
├── examples/             # Sample agents
├── README.md
├── package.json
└── tsconfig.json
```

---

## 🧪 Tests

```bash
# Run full test suite
npm run test

# Linting
npm run lint
```

---

## 🧭 Roadmap

* [x] Initial SDKs (TS)
* [x] Basic agent templates
* [ ] Agent Studio (visual interface)
* [ ] ZK-attested agent execution
* [ ] Custom model plugin support
* [ ] DAO-based registry governance
* [ ] Gasless execution via relayers

---

## 💼 Contribute

We welcome contributors! Please:

* Fork the repo and create a feature branch
* Open a PR with clear commit history
* Add tests for your features

For major features, submit a proposal to `/proposals`

---

## 📄 License

MIT License — Copyright (c) 2025 Astryx.org

---

## 🔗 Resources

* Docs: [https://docs.astryx.org](https://docs.astryx.org)
* API: [https://api.astryx.org](https://api.astryx.org)
* Twitter: [@astryx\_ai](https://twitter.com/astryx_ai)
* Website: [https://astryx.org](https://astryx.org)
* Discord: (Coming Soon)
