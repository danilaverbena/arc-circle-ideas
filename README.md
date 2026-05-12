# Arc × Circle — Vibe-codable Ideas

**18 практичных идей для разработки на стеке [Arc Network](https://docs.arc.network) и [Circle Developer Platform](https://developers.circle.com), в двух эпизодах.**

Двухпроходное исследование документации Arc (L1 с USDC как gas) и Circle (CCTP, Gateway, Nanopayments/x402, Modular Wallets, Smart Contract Platform, **StableFX**, **Compliance Engine**, AI Skills, MCP). Каждая идея — с MVP-скоупом, привязанными primitives и оценкой сложности.

## 🌐 Live preview

| Эпизод | Файл | Тема |
|--------|------|------|
| **v1 — Consumer & Agentic** | [`index.html`](./index.html) | 10 идей: AI-payments, кросс-чейн UX, embedded wallets, dev tools |
| **v2 — Institutional & Infra** | [`ideas-v2.html`](./ideas-v2.html) | 8 идей: StableFX corridor, compliance SDK, treasury bot, escrow judge, metered billing |

Откройте файлы локально или [включите GitHub Pages](https://github.com/danilaverbena/arc-circle-ideas/settings/pages) на ветке `main` — обе страницы self-contained, без зависимостей.

## 📚 Что в репозитории

| Файл | Что внутри |
|------|-----------|
| `index.html` | Эпизод 1: capability map + 10 идей (consumer / agentic commerce) |
| `ideas-v2.html` | Эпизод 2: 5 новых primitives + 8 идей (institutional fintech / infra) |
| `README.md` | Этот файл — overview и быстрый список всех 18 идей |
| `LICENSE` | MIT |

## 🧱 Полная capability map

### Arc Network (L1)
- **USDC как gas** — предсказуемые комиссии без волатильности
- **Stable Fee Design** — target ~$0.01/tx через EWMA-сглаживание, max ceiling 1e-3 USDC/gas, 20M gas/sec
- **Sub-second finality** — Malachite (Tendermint BFT) + Reth execution
- **EVM compatible** — Foundry / Hardhat / viem / ethers
- **Opt-in privacy** (roadmap) — TEE → MPC → FHE → ZK с view keys
- **Stablecoin Services** — multi-currency, FX, programmatic settlement
- **Sample apps** — commerce, multichain wallet, AI escrow (Refund Protocol), fintech treasury, P2P passkey

### Circle Developer Platform
- **CCTP V2** — native USDC burn-and-mint между 19+ цепями (Fast ~8-20s)
- **Gateway** — unified balance, <500ms transfers, non-custodial
- **Nanopayments + x402** — gas-free USDC от $0.000001, HTTP 402 protocol
- **StableFX** — RFQ-движок на Arc, USDC↔EURC с PvP escrow settlement (permissioned)
- **App Kit** — единый SDK для Bridge / Swap / Send / Unified Balance
- **Wallets** — developer-controlled / user-controlled (social login) / modular (passkey + ERC-4337/6900)
- **Smart Contract Platform** — templates ERC-20/721/1155, ABI calls, event monitoring
- **Gas Station** (5% fee, card billing) + **Paymaster** (10% fee, USDC payments)
- **Compliance Engine** — AML/CTF screening, allowlists, alerts, reporting (gated access)
- **Managed Payments** — continuous + transient payment intents, Crypto Deposits API
- **Circle Mint** — USDC/EURC payins, off-ramps, FX

### AI infrastructure
- **9 Circle Skills** — LLM-оптимизированные гайды (use-arc, use-gateway, bridge-stablecoin, ...)
- **Circle MCP** — codegen сервер на `https://api.circle.com/v1/codegen/mcp`

## 💡 Все 18 идей одним списком

### Эпизод 1 — Consumer & Agentic

| # | Идея | USP | Время |
|---|------|-----|-------|
| 01 | **MicroPay AI Gateway** | Sub-cent биллинг для AI APIs через x402, без подписок | 2d |
| 02 | **Stripe-for-Agents** | Бюджеты, allowlists и аудит для AI-агентов с passkey wallets | 3-4d |
| 03 | **v0-for-Solidity** | Natural-language → деплоенный DApp на Arc через MCP | 3d |
| 04 | **PayLink Universal** | Stripe Payment Links для USDC, multichain checkout | 2d |
| 05 | **Streampay** | Payroll по секундам на Arc, gas платится из самого стрима | 4d |
| 06 | **Drop-in Wallet Button** | Один `<script>` тег — passkey wallet + USDC pay для любого SaaS | 2d |
| 07 | **TipStream** | Per-second nano-tips для стримеров через x402 | 3d |
| 08 | **Onchain Cashback Engine** | Event-driven loyalty с ERC-1155 reward и Gateway redeem | 3d |
| 09 | **Agent Job Escrow** | Upwork для AI-агентов с on-chain milestone-платежами | 5d |
| 10 | **Multi-Currency Invoice** | EUR-invoice → USDC pay → EURC settlement за секунды | 3d |

### Эпизод 2 — Institutional & Infra

| # | Идея | USP | Время |
|---|------|-----|-------|
| 11 | **EuroPay Corridor** | Cross-border USDC↔EURC через StableFX, 5-10 сек вместо 5 дней | 4d |
| 12 | **Compliance Layer SDK** | Drop-in AML/CTF screening для любого DeFi/wallet проекта | 4d |
| 13 | **TreasuryAutoPilot** | AI-CFO для multichain казны, авто-rebalancing 24/7 | 5d |
| 14 | **AI Escrow Judge** | Refund Protocol + AI-валидация работы для agent freelance | 6d |
| 15 | **Stablecoin Arbitrage Engine** | HFT-арбитраж USDC/EURC через StableFX RFQ, профит от $0.01 fees | 6d |
| 16 | **SaaS Metered Billing** | On-chain pay-per-API-call в USDC, работает только благодаря Arc fees | 3d |
| 17 | **DAO Treasury Vault** | Modular wallet + allowlist module + Compliance Engine для DAO | 4-5d |
| 18 | **Sub — Subscriptions для USDC** | Stripe Subscriptions реплика на continuous payment intents | 5d |

Полные описания, MVP-скоупы, привязанные skills и moat-анализ — в страницах [`index.html`](./index.html) и [`ideas-v2.html`](./ideas-v2.html).

## 🎯 Что брать первым

| Если у вас... | Берите |
|--------------|--------|
| Выходные и хочется wow-демо | **#01 MicroPay AI Gateway** или **#04 PayLink Universal** |
| Неделя на solo-сайд-проект | **#03 v0-for-Solidity** или **#16 SaaS Metered Billing** |
| Команда и амбиции на стартап | **#02 Stripe-for-Agents** или **#12 Compliance Layer SDK** |
| Институциональные клиенты на горизонте | **#11 EuroPay Corridor** или **#13 TreasuryAutoPilot** |
| Любите glue-tech и middleware | **#09 Agent Job Escrow** или **#14 AI Escrow Judge** |

## 🚀 Старт за 5 минут

```bash
# Установить Circle Skills (Claude Code)
/plugin marketplace add circlefin/skills
/plugin install circle-skills@circle

# MCP в Claude Code или Cursor
claude mcp add --transport http circle \
  https://api.circle.com/v1/codegen/mcp \
  --scope user

# Faucet для Arc Testnet
→ https://faucet.circle.com

# Sample apps как стартовая точка
→ https://docs.arc.network/arc/references/sample-applications
```

## 📖 Источники

### Primary docs
- [docs.arc.network/build](https://docs.arc.network/build)
- [developers.circle.com](https://developers.circle.com/)
- [developers.circle.com/ai/skills](https://developers.circle.com/ai/skills)
- [developers.circle.com/ai/mcp](https://developers.circle.com/ai/mcp)

### Deep dive (v2 sources)
- [StableFX](https://developers.circle.com/stablefx) — institutional FX-движок
- [Compliance Engine](https://developers.circle.com/wallets/compliance-engine) — AML/CTF API
- [Stable Fee Design](https://docs.arc.network/arc/concepts/stable-fee-design) — EWMA fee model
- [Sample Apps](https://docs.arc.network/arc/references/sample-applications) — open-source references
- [Circle Mint Crypto Deposits](https://developers.circle.com/circle-mint/crypto-payments-quickstart)
- [EURC overview](https://developers.circle.com/stablecoins/what-is-eurc)
- [github.com/circlefin/skills](https://github.com/circlefin/skills)

## 📝 License

MIT — см. [LICENSE](./LICENSE).
