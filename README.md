<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/hero-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/hero-light.svg">
  <img alt="Mohamed Ouaked — Systems that trade, think, and ship" src="assets/hero-dark.svg" width="100%">
</picture>

<br>

### Mohamed Ouaked

**I build the full stack of a trading idea** — the research, the engine, and the screen that makes it legible.

<sub>📍 Tizi Ouzou, Algeria · UTC+1 &nbsp;·&nbsp; Open to remote & relocation</sub>

<br>

[**Work**](#03--featured-work) &nbsp;·&nbsp; [**Stack**](#02--technical-arsenal) &nbsp;·&nbsp; [**Method**](#05--how-i-build) &nbsp;·&nbsp; [**Track record**](#07--track-record) &nbsp;·&nbsp; [**Contact**](#08--get-in-touch)

</div>

<br>

<img src="assets/divider.svg" width="100%" alt="">

## <samp>01</samp> &nbsp;— &nbsp;Current Mission

<table>
<tr>
<td valign="top" width="50%">

**⚡ &nbsp;Building**

`KESH QUANT` &nbsp;24/7 perps engine on Hyperliquid. Python on GCP, Next.js terminal on Vercel.

`ORB TERMINAL` &nbsp;Backtest and paper-trade environment with candle-by-candle replay.

</td>
<td valign="top" width="50%">

**◎ &nbsp;Learning**

`MICROSTRUCTURE` &nbsp;Order books, slippage, and why a backtest fill lies.

`REGIME DETECTION` &nbsp;Knowing *when* to switch a strategy off.

`AGENTIC SYSTEMS` &nbsp;LLM pipelines doing real operational work.

</td>
</tr>
</table>

<br>

<img src="assets/divider.svg" width="100%" alt="">

## <samp>02</samp> &nbsp;— &nbsp;Technical Arsenal

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/arsenal-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/arsenal-light.svg">
  <img alt="Technical domains: frontend, backend, AI, data, quant, devops" src="assets/arsenal-dark.svg" width="100%">
</picture>

| | |
| :--- | :--- |
| **Frontend** | TypeScript · Next.js 14 · React · Tailwind · shadcn/ui · Recharts · `lightweight-charts` |
| **Backend** | Python 3.11 · FastAPI · Node · Bun · REST + WebSocket services · JWT sessions · cron workers |
| **AI** | Claude API · LLM signal rationale · multi-phase agent pipelines · deterministic fallbacks |
| **Data** | Neon Postgres · Drizzle · Prisma · SQLite · pandas / NumPy · time-series normalisation |
| **Quant** | Backtest engines · risk & sizing · Black-Scholes N(d₂) · ORB · ICT/SMC · expectancy & R-multiples |
| **Venues** | Hyperliquid · MetaTrader 5 · Capital.com · Polymarket · Deribit · CME FedWatch |
| **DevOps** | GCP · Vercel · GitHub Actions · Pytest · Vitest · Telegram alerting |

<br>

<img src="assets/divider.svg" width="100%" alt="">

## <samp>03</samp> &nbsp;— &nbsp;Featured Work

<br>

### <samp>01</samp> &nbsp;Kesh Quant &nbsp;<sub>· autonomous perps engine + terminal</sub>

> Markets run 24/7. Traders don't.

**Problem** &nbsp;Running unattended means trusting a process you can't watch.
<br>**Built** &nbsp;Hyperliquid WebSocket → features → confluence filter → risk-sized orders, continuously on GCP. A separate Next.js terminal reads engine state over an authenticated tunnel, so watching never blocks trading.
<br>**Result** &nbsp;Runs unattended and stays inspectable in real time.

`Python` `FastAPI` `Hyperliquid` `WebSockets` `Next.js` `GCP`

[**Repository →**](https://github.com/nate0004/crypto-bot) &nbsp;<sub>🔒 private deployment</sub>

<br>

### <samp>02</samp> &nbsp;ORB Terminal &nbsp;<sub>· backtesting + paper-trading research</sub>

> A win rate without a replay is a rumour.

**Problem** &nbsp;Summary stats hide *why* a strategy loses — so you can't fix it.
<br>**Built** &nbsp;Every backtested trade replays candle-by-candle against the higher-timeframe ICT/SMC bias that allowed it. Persistent paper account, engine under test so refactors can't silently rewrite history.
<br>**Result** &nbsp;Iteration moved from arguing about averages to watching trades fail.

`Next.js 14` `Drizzle` `Neon` `lightweight-charts` `Vitest`

<sub>🔒 Private repo — walkthrough on request.</sub>

<br>

### <samp>03</samp> &nbsp;Polymarket vs. Wall Street &nbsp;<sub>· probability divergence dashboard</sub>

> Two markets, one event, two prices. The spread is the signal.

**Problem** &nbsp;Prediction markets and derivatives venues price identical events differently — in incompatible units.
<br>**Built** &nbsp;Normalises both into one probability space: CME FedWatch futures-implied for rate events, Deribit BTC options via Black-Scholes N(d₂) for crypto, CME for equity-linked events like SPY.
<br>**Result** &nbsp;Retail-vs-institutional spread readable live. **Sub-100 ms** ingestion via in-memory LRU caching.

`Next.js 14` `TypeScript` `Deribit` `CME FedWatch` `Black-Scholes`

[**Repository →**](https://github.com/nate0004/polymarket-vs-wallstreet) &nbsp;<sub>🔒 no hosted instance</sub>

<br>

### <samp>04</samp> &nbsp;ICT 2022 Signal Bot &nbsp;<sub>· signal-only intraday engine, NAS100</sub>

> The hard part of automation is choosing what *not* to automate.

**Problem** &nbsp;Any drift between backtested rules and live rules invalidates the research.
<br>**Built** &nbsp;One engine, two modes — detection logic is pure functions with zero I/O. Live feeds it closed M1 bars from a socket; backtest replays history through the identical path. Signals scored, annotated by an LLM with a deterministic fallback, stored with outcomes.
<br>**Result** &nbsp;Backtest and live match structurally. Every alert becomes a datapoint. It never places an order.

`Python` `WebSockets` `Capital.com` `SQLite` `Telegram`

[**Repository →**](https://github.com/nate0004/ict-signal-bot)

<br>

<details>
<summary><b>&nbsp;Also in the workshop</b> &nbsp;<sub>— six more</sub></summary>

<br>

| Project | What it does |
| :--- | :--- |
| **[TradeJournal](https://github.com/nate0004/trading-journal)** | CSV-first journal built on the metrics that reveal an edge — expectancy, profit factor, R:R, equity curve, splits by pair/tag/session. |
| **[Outreach Pipeline v2](https://github.com/nate0004/outreach-dashboard-v2)** | Four-phase autonomous B2B pipeline: leads → AI mockup pages → AI cold email → follow-up cron. |
| **[Stock Checker](https://github.com/nate0004/stock-checker)** | Multi-ticker scanner: RSI, Stochastic, Bollinger, Donchian, Williams %R, ATR stops, weighted signal scoring. |
| **[OVN Breakout Bots](https://github.com/nate0004/ovn-breakout-bot)** | Overnight-range breakout productionised across [NAS100](https://github.com/nate0004/nas100-ovn-bot) and [MNQ](https://github.com/nate0004/mnq-ovn-bot) via MetaTrader 5. |
| **[Kesh Investment](https://github.com/nate0004/Kesh-Investment)** | Investment-facing surface for the Kesh systems. |
| **[Gamified Journal](https://github.com/nate0004/gamified-journal)** | Trading discipline as a game loop — streaks and scoring on process, not P&L. |

</details>

<br>

<img src="assets/divider.svg" width="100%" alt="">

## <samp>04</samp> &nbsp;— &nbsp;The Journey

<details>
<summary><b><samp>2024</samp> &nbsp;Foundations</b> &nbsp;<sub>— market data, Python, indicator maths</sub></summary>

<br>

Indicator maths from first principles rather than a library I didn't understand. Most of it was thrown away on purpose — the output wasn't code, it was knowing how price data behaves once you touch it.

</details>

<details>
<summary><b><samp>2025</samp> &nbsp;Research</b> &nbsp;<sub>— backtesting, ICT/SMC, opening-range breakout</sub></summary>

<br>

Built the backtest harness before the strategies. Started measuring in expectancy and R-multiples instead of win rate. The rule that stuck: if it can't survive out-of-sample, it doesn't deploy.

</details>

<details>
<summary><b><samp>2026 · H1</samp> &nbsp;Terminals</b> &nbsp;<sub>— Next.js, Postgres, replay</sub></summary>

<br>

The bottleneck wasn't strategy quality, it was visibility. Journals with real analytics, research terminals with chart replay. Every engine got a face.

</details>

<details>
<summary><b><samp>2026 · H2</samp> &nbsp;Autonomy</b> &nbsp;<sub>— 24/7 engines, agentic pipelines</sub></summary>

<br>

Systems that run without me: a continuous engine on GCP, agent pipelines executing multi-phase workflows unattended. The current problem is making autonomy *trustworthy* — observable, bounded, reversible.

</details>

<br>

<img src="assets/divider.svg" width="100%" alt="">

## <samp>05</samp> &nbsp;— &nbsp;How I Build

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/pipeline-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/pipeline-light.svg">
  <img alt="Pipeline: research → data → backtest → risk → interface → deploy → observe, looping back to research" src="assets/pipeline-dark.svg" width="100%">
</picture>

<sub>**The loops matter more than the line.** Failing the backtest is cheap. Decaying in production is not — the observation layer is what tells me when. Nothing ships without the last two stages.</sub>

<!--
  ── SIGNALS PANEL (lowlighter/metrics) ────────────────────────────────────
  Uncomment AFTER running .github/workflows/metrics.yml once, so the SVGs
  exist. Referencing them before that renders broken images.

<div align="center">
  <img src="assets/metrics/isocalendar.svg" alt="Isometric contribution calendar" width="49%">
  <img src="assets/metrics/languages.svg" alt="Language distribution" width="49%">
</div>
-->

<br>

<img src="assets/divider.svg" width="100%" alt="">

## <samp>06</samp> &nbsp;— &nbsp;Roadmap

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/roadmap-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/roadmap-light.svg">
  <img alt="Roadmap: shipped and in-flight milestones across now and next" src="assets/roadmap-dark.svg" width="100%">
</picture>

<br>

<img src="assets/divider.svg" width="100%" alt="">

## <samp>07</samp> &nbsp;— &nbsp;Track Record

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/credentials-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/credentials-light.svg">
  <img alt="Experience timeline, education, certifications and languages" src="assets/credentials-dark.svg" width="100%">
</picture>

<br>

<img src="assets/divider.svg" width="100%" alt="">

## <samp>08</samp> &nbsp;— &nbsp;Get in Touch

<div align="center">

<sub>Open to remote quantitative engineering and full-stack roles, and to relocation.<br>EU hours with US East overlap.</sub>

<br><br>

| | | | |
| :---: | :---: | :---: | :---: |
| **[LinkedIn](https://linkedin.com/in/mohamed-ouaked)** | **[GitHub](https://github.com/nate0004)** | **[X](https://x.com/berso444)** | **[Résumé](https://app.notion.com/p/Moha-Resume-f107974e66328298a95f013d754e75c0)** |
| <sub>the record</sub> | <sub>the work</sub> | <sub>the thinking</sub> | <sub>the summary</sub> |

<br>

**[✉️ &nbsp;okd.moha@gmail.com](mailto:okd.moha@gmail.com)**

</div>

<br>

<img src="assets/divider.svg" width="100%" alt="">

<div align="center">

<br>

### *"Alpha decays. Systems compound."*

<sub>Built by **Mohamed Ouaked** &nbsp;·&nbsp; <samp>nate0004</samp></sub>

<br>

</div>
