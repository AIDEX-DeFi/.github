# AIDEX — Repository Index

Welcome to **[AIDEX](https://ai-dex.io)** — a millisecond-latency DEX aggregator and execution layer for autonomous AI agents trading on-chain.

---

## What is AIDEX?

AIDEX is a lightning-fast DEX aggregator for swapping tokens on-chain. The pipeline is optimised for minimal latency between an agent's decision and the moment the signed transaction hits the network. The gap between intent and execution is where price moves against you, and AIDEX is built to minimise it.

Use AIDEX when you want to give your users or their autonomous agents low-latency on-chain swap execution through a public, JSON-first HTTP interface.

The organization is split across a small number of focused repositories:

| Repository | Purpose | Primary language |
|---|---|---|
| [`router`](https://github.com/AIDEX-DeFi/router) | On-chain router contract that executes AIDEX swaps | Solidity |
| [`genesis-key`](https://github.com/AIDEX-DeFi/genesis-key) | ERC-721 smart contracts for the AIDEX Genesis Key | Solidity |
| [`skills`](https://github.com/AIDEX-DeFi/skills) | AIDEX skill for AI agents (OpenClaw) — swap, quote, balance, verify | JavaScript |
| [`Documentation`](https://github.com/AIDEX-DeFi/Documentation) | AIDEX Agents API reference — endpoints, OpenAPI spec, playground | Markdown |

---

## [`router`](https://github.com/AIDEX-DeFi/router)

**AIDEX Router** — the on-chain smart contract that executes token swaps across multiple liquidity pools and exchanges, chaining them into optimal multi-step routes. The trader specifies the input and output tokens, and the router executes the entire swap sequence in a single transaction. Every AIDEX swap settles through this contract — whether it originates from the [ai-dex.io](https://ai-dex.io) web interface, the Agents API, or the OpenClaw skill.

**Stack:** Solidity.
**License:** MIT.

---

## [`genesis-key`](https://github.com/AIDEX-DeFi/genesis-key)

**AIDEX Genesis Key** — a transferable ERC-721 that grants its holder **execution priority** inside AIDEX.

Each Key carries **Priority Points** that determine how early a holder's transactions are processed by AIDEX. Earlier processing means earlier submission to the network, better block placement, and better effective rates.

**Status:** live on Ethereum mainnet.
**NFT contract:** [`0x8f1e9B958c157D922DBDf0252C753122Ba2Ad0C8`](https://etherscan.io/address/0x8f1e9B958c157D922DBDf0252C753122Ba2Ad0C8)
**Stack:** OpenZeppelin upgradeable contracts (UUPS + AccessControl), Hardhat.
**License:** MIT.

Learn more: [ai-dex.io/key](https://ai-dex.io/key)

---

## [`skills`](https://github.com/AIDEX-DeFi/skills)

**AIDEX Skills** — turn your AI agent into an on-chain trading desk.

This repository packages AIDEX as a skill for [OpenClaw](https://github.com/AIDEX-DeFi/skills#installation). Once installed, your agent can search tokens, quote exchange rates, read wallet balances, and execute swaps via the AIDEX DEX aggregator — with **client-side transaction signing** so private keys never leave the user's machine.

**License:** MIT.

Start here: [installation guide](https://github.com/AIDEX-DeFi/skills#installation) · [security model](https://github.com/AIDEX-DeFi/skills#security)

---

## [`Documentation`](https://github.com/AIDEX-DeFi/Documentation)

**AIDEX Agents API** — a public, JSON-first HTTP interface for autonomous AI agents and AI-driven trading. Covers the full swap lifecycle: token search, exchange rates, wallet balances and swaps.

**Base URL:** `https://api.ai-dex.io`
**Spec:** [OpenAPI 3.1](https://api.ai-dex.io/openapi/agent.json) · [interactive playground](https://api.ai-dex.io/scalar/agent)

Start here: [API reference](https://github.com/AIDEX-DeFi/Documentation)

---

## Links

- Website: [ai-dex.io](https://ai-dex.io)
- Genesis Key: [ai-dex.io/key](https://ai-dex.io/key)
- Contact: `info@ai-dex.io`

---

## License

Unless a repository states otherwise, AIDEX open-source code is released under the **MIT License**.
