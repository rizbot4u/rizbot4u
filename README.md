# Rizwan Ali

**I build multi-tenant AI agent infrastructure.**

Solo founder of Nova Global Keys — a full-stack crypto trading platform and MCP-based AI agent stack, running in production on a self-managed Ubuntu VPS.

Bybit Tier-3 Institutional Broker (Kr000820) · Live on Base Mainnet · Open to remote roles

---

## What I've Built

### 🏦 [nova-global-keys-](https://github.com/rizbot4u/nova-global-keys-)
Production crypto trading platform. 9 microservices (auth, broker, gateway, market, trade, user, p2p, telegram, shared) behind Nginx, managed by PM2, running as a systemd service. Redis-backed sessions, Bybit V5 OAuth 2.0 integration, multi-strategy engine (DCA, DEX, triangle arbitrage, grid).

**Stack:** Python · FastAPI · Redis · Nginx · systemd · PM2 · Next.js · Docker · Kubernetes

### 🌉 [nova_mcp](https://github.com/rizbot4u/nova_mcp)
MCP bridge that exposes trading and on-chain functions as tools to LLMs (Claude, Cursor). Per-tenant AES-256-GCM encrypted vaults, HMAC-SHA256 signing, EIP-55 address validation, policy enforcement (spend caps, allowlists, `confirm: true`), full JSON audit logging.

**Stack:** Node.js · ethers.js v6 · MCP SDK · Bybit V5 · Base Mainnet

### 🧠 [nova-skills-registry](https://github.com/rizbot4u/nova-skills-registry)
Multi-tenant AI skill catalog. Immutable versioning, JSON Schema validation, JWT auth, strict org-level isolation, audit trails. LLM uses this to route natural language to the right tool.

**Stack:** Python · FastAPI · SQLAlchemy · Pydantic · Docker

### 📱 [nova-global-keys--bot](https://github.com/rizbot4u/nova-global-keys--bot)
Telegram frontend for the whole stack. Natural-language trading + on-chain transfers, with a review-and-confirm flow before any signed action.

### 📦 [nova-trading-sdk](https://pypi.org/project/nova-trading-sdk)
Published Python SDK wrapping Bybit V5 and Binance REST APIs. `pip install nova-trading-sdk`

---

## How the Pieces Connect

```
AI Agent (Claude / Cursor)
        │
        ▼
nova_mcp  ──── policy · vault · audit ──── nova-skills-registry
        │                                         │
        ▼                                         ▼
nova-trading-sdk ── Bybit V5 / Binance ── Base Mainnet (EVM)
        ▲
        │
nova-global-keys- (9 services · Redis · Nginx · PM2)
        ▲
        │
nova-global-keys--bot (Telegram)
```

Four layers. Each one has a single job. No layer trusts the one above it.

---

## Live Proof

- **Bybit Broker:** Kr000820 — [verification](https://www.bybit.com/en/verification/)
- **OAuth Client:** `x9dmxAGkDDoa`
- **On-chain:** DKHYR ERC-20 on Base Mainnet, EIP-7702 Type-4 delegations
- **Recent trading volume:** $14.8M (30-day)

---

## Tech I Work With

`Python` `FastAPI` `Node.js` `Next.js` `Redis` `SQLite` `PostgreSQL` `Nginx` `systemd` `PM2` `Docker` `Kubernetes` `ethers.js` `MCP` `Bybit V5` `Binance` `Base Mainnet` `Telegram Bot API`

---

## What I'm Doing Now

Building the safe half of autonomous finance — agentic infrastructure where an LLM can move real money without ever touching a private key.

Open to:
- Remote engineering roles (AI agents, MCP, crypto infra)
- Founding engineer conversations
- Technical co-founder discussions

**Reach me:** [LinkedIn](https://www.linkedin.com/in/rizwan-ali-974073377) · [Telegram](https://t.me/Novaglobalkeysbot)

---

*Built solo. Two years ago I couldn't write a for-loop.*
