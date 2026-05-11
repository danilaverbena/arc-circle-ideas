# Arc × Circle — Vibe-codable Ideas

**10 практичных идей для разработки на стеке [Arc Network](https://docs.arc.network) и [Circle Developer Platform](https://developers.circle.com).**

Краткий бриф по итогам изучения документации Arc (L1 с USDC как gas) и Circle (CCTP, Gateway, Nanopayments/x402, Modular Wallets, Smart Contract Platform, Paymaster, AI Skills, MCP). Каждая идея — с MVP-скоупом, привязанными primitives и оценкой сложности.

## 🌐 Live preview

Откройте [`index.html`](./index.html) локально или [включите GitHub Pages](https://github.com/danilaverbena/arc-circle-ideas/settings/pages) на основной ветке — страница self-contained, без зависимостей.

## 📚 Что в репозитории

| Файл | Что внутри |
|------|-----------|
| `index.html` | Презентационная страница с картой capabilities и 10 идеями |
| `README.md` | Этот файл — overview и быстрый список идей |
| `LICENSE` | MIT |

## 🧱 Capability map стека

### Arc Network (L1)
- **USDC как gas** — предсказуемые комиссии без волатильности
- **Sub-second finality** — Malachite (Tendermint BFT) + Reth execution
- **EVM compatible** — Foundry / Hardhat / viem / ethers
- **Opt-in privacy** (roadmap) — TEE → MPC → FHE → ZK с view keys
- **Stablecoin Services** — multi-currency, FX, programmatic settlement

### Circle Developer Platform
- **CCTP V2** — native USDC burn-and-mint между 19+ цепями (Fast ~8-20s)
- **Gateway** — unified balance, <500ms transfers, non-custodial
- **Nanopayments + x402** — gas-free USDC от $0.000001, HTTP 402 protocol
- **App Kit** — единый SDK для Bridge / Swap / Send / Unified Balance
- **Wallets** — developer-controlled / user-controlled (social login) / modular (passkey + ERC-4337/6900)
- **Smart Contract Platform** — templates ERC-20/721/1155, ABI calls, event monitoring
- **Gas Station + Paymaster** — sponsor gas или плати gas в USDC
- **Managed Payments** — continuous payment intents для приёма USDC

### AI infrastructure
- **9 Circle Skills** — LLM-оптимизированные гайды (use-arc, use-gateway, bridge-stablecoin, ...)
- **Circle MCP** — codegen сервер на `https://api.circle.com/v1/codegen/mcp` с live сигнатурами и адресами

## 💡 10 идей одним списком

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

Полное описание, MVP-скоуп, привязанные skills и стек — в [`index.html`](./index.html).

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
```

## 📖 Источники

- [docs.arc.network/build](https://docs.arc.network/build)
- [developers.circle.com](https://developers.circle.com/)
- [developers.circle.com/ai/skills](https://developers.circle.com/ai/skills)
- [developers.circle.com/ai/mcp](https://developers.circle.com/ai/mcp)
- [github.com/circlefin/skills](https://github.com/circlefin/skills)

## 📝 License

MIT — см. [LICENSE](./LICENSE).
