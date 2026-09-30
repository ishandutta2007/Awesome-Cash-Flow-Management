# Awesome-Cash-Flow-Management

## Top Cash Flow Management Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Cash Forecasting, Liquidity Planning, Scenario Analysis & Working Capital Optimization*

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Cash Flow Management**. These tools help finance teams, founders, and CFOs project cash positions, identify runway risks, model scenarios, and optimize working capital—moving beyond static spreadsheets to dynamic, real-time liquidity visibility.



**Examples** include Pulse, Fathom, Float, CashFlow Frog, Dryrun, Fluidly, Agicap, PlanGuru, Jirav, and Cube (the category leaders).



**Open-source emphasis**: Cash flow management has a **developing open-source ecosystem**. Unlike adjacent categories with mature platforms, open-source cash flow tools are primarily **focused utilities and research prototypes**. **Firefly III** (24k+ stars, AGPL-3.0) provides self-hosted double-entry bookkeeping with cash flow reporting . **Actual Budget** (29k+ stars, MIT) offers local-first envelope budgeting with cash flow views . **Equilibrium** implements quantum-inspired payment scheduling using QUBO optimization . **cfo-cli** delivers terminal-first cash flow forecasting with AI insights . **AFIS** provides ML-based 12-month cash flow projections with NIST AI RMF alignment . This section documents these focused solutions honestly.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Pulse](https://www.pulseapp.com/)**

  Cash flow forecasting and management platform for startups and SMBs. Provides real-time cash visibility, scenario planning, and runway projections.



- **[Fathom](https://www.fathomhq.com/)**

  Financial analysis and reporting platform with cash flow forecasting. Provides KPI dashboards, benchmarking, and multi-entity consolidation for advisory firms and businesses.



- **[Float](https://floatapp.com/)**

  Cash flow forecasting software for businesses. Integrates with accounting software to provide real-time cash flow projections and scenario planning.



- **[CashFlow Frog](https://www.cashflowfrog.com/)**

  Cash flow forecasting and management platform. Provides cash flow projections, scenario modeling, and alerts for SMBs.



- **[Dryrun](https://www.dryrun.com/)**

  Cash flow forecasting and scenario planning platform. Integrates with QuickBooks, Xero, and Excel to provide 12-month cash flow projections.



- **[Fluidly](https://fluidly.com/)**

  AI-powered cash flow forecasting and management platform for accountants and businesses.



- **[Agicap](https://agicap.com/)**

  European cash flow management platform. Provides cash flow forecasting, cash positioning, and treasury management for SMBs and mid-market companies.



- **[PlanGuru](https://www.planguru.com/)**

  Budgeting, forecasting, and financial analysis software. Provides cash flow projections and scenario planning for businesses and advisors.



- **[Jirav](https://www.jirav.com/)**

  Financial planning and analysis platform with cash flow forecasting. Provides driver-based modeling, scenario planning, and board-ready reporting.



- **[Cube](https://www.cubesoftware.com/)**

  Spreadsheet-native FP&A platform with cash flow forecasting. Connects to ERP for real-time financial data and reporting.



## Open-Source GitHub Projects



### Personal & Small Business Cash Flow Management



- **[Firefly III](https://github.com/firefly-iii/firefly-iii)**

  **The most widely adopted open-source personal finance manager with cash flow capabilities.** **24,286+ GitHub stars**, **AGPL-3.0 licensed** . Self-hosted double-entry bookkeeping system. **Key features**: Track transactions, budgets, and accounts; multi-currency support; rule engine for automated categorization; REST API; cash flow reporting . **Deployment**: Docker, self-hosted. **Best for**: Individuals and very small businesses tracking cash flow with full data ownership.



- **[Actual Budget](https://github.com/actualbudget/actual)**

  **Privacy-focused personal finance app with envelope budgeting and cash flow views.** **29,224+ GitHub stars**, **MIT licensed** . **Key features**: Envelope budgeting (assign real cash on hand to categories); **cash flow reports** built-in; bank sync (goCardless EU/UK, SimpleFIN US/Canada); QIF, OFX, QFX, CAMT.053, CSV import; optional end-to-end encryption; self-hosted sync server . **Deployment**: Self-hosted or cloud. **Best for**: Individuals and households wanting local-first budgeting with cash flow visibility.



- **[cfo-cli](https://github.com/Neskys/cfo-cli)**

  **Open-source financial CLI for freelancers, consultants, and small teams.** **MIT licensed** . **Key features**: Budget planning; expense and income tracking; **cash flow forecasting** with base, optimist, and pessimist scenarios; CSV and PDF reports; multi-currency with cached exchange rates; **AI insights** via Claude, OpenAI, or free local Gemma (Ollama); **MCP Server** for AI assistant integration . **Local-first**: SQLite database in `~/.cfo/`, zero cloud dependency. **Installation**: `pip install cfo-cli` or from source . **Best for**: Technical users wanting terminal-first cash flow management.



### Cash Flow Forecasting & Optimization



- **[Equilibrium](https://github.com/mtahakeles/equilibrium)**

  **Cash flow forecasting with quantum-inspired payment scheduling for small businesses.** **Key innovation**: Projects cash position over the next **10 weeks**, then reschedules outstanding bills using a **QUBO-style cost function** solved with **Simulated Annealing**—the same technique used to benchmark quantum annealers . **Cost function combines**: Linear term (discount captured or penalty incurred for early/late payment); quadratic term (penalty on `(buffer − balance)²` for every week projected balance dips under safety buffer, plus hard penalty for negative balance) . **Interactive dashboard**: Renders forecast, optimizer convergence, and side-by-side schedule comparison with safety-buffer slider . **No dependencies**: Vanilla JavaScript, HTML5 Canvas . **Best for**: Small businesses wanting automated payment scheduling to optimize cash flow.



- **[AFIS](https://github.com/afild/AFIS)**

  **Open-source AI-driven financial intelligence framework for SMEs.** **Three integrated layers**: **ETL Ingestion** (CSV imports from QuickBooks/Xero, validation, deduplication, NIST-aligned governance audit trail, SQLite storage); **Predictive Analytics** (Ridge regression models for 12-month projections of revenue, expenses, and net cash flow with 95% confidence intervals; exposes burn rate, runway, net margin, cash position via Chart.js dashboards); **AI Interpretation** (natural-language management narratives, financial red flags, actionable recommendations; LLM Mode via Anthropic Claude or **Offline Mode** with deterministic rule-based heuristics—no API key required) . **Local-first**: All transaction data stays on the SME's machine; optional LLM integration transmits only computed metrics, never raw transactions . **API surface**: `/api/ingest`, `/api/kpis`, `/api/forecast`, `/api/forecast/whatif`, `/api/chat`, `/api/nist-audit` . **Stack**: FastAPI, scikit-learn, SQLite, Chart.js . **Best for**: SMEs wanting ML-powered cash flow forecasting with privacy and NIST governance.



- **[pycashflow](https://github.com/H3-Consulting/pycashflow)**

  **Python Flask application for future cash flow calculation and management.** **Key features**: Recurring scheduled transactions; **90-day cash flow projections** with running-balance projection; **what-if scenario modeling**; risk scoring with detailed breakdown; Plaid integration for bank connections; **REST API** with Bearer token authentication (30-day tokens, SHA-256 hashed); **AI Insights** via OpenAI or DigitalOcean GenAI Agent . **Data endpoints**: `/api/v1/dashboard` (current balance, risk score, upcoming transactions, 90-day minimum balance), `/api/v1/projections` (running-balance projection data), `/api/v1/risk-score` (detailed cash-flow risk assessment) . **All monetary values as decimal strings** to avoid floating-point precision issues . **Stack**: Flask, PostgreSQL, Fernet encryption for API keys . **Best for**: Developers wanting a REST API for cash flow forecasting.



### Personal Finance & Budgeting Foundations



- **[Money Manager Ex](https://github.com/moneymanagerex/moneymanagerex)**

  **Free, open-source, cross-platform personal finance software.** **Key features**: Checking, credit card, savings, stock investment, and asset accounts; reminders for recurring bills and deposits; **budgeting and cash flow forecasting**; simple one-click reporting with graphs and pie charts; import from CSV, QIF; **non-proprietary SQLite database with AES encryption**; available in 24 languages . **Runs from USB key** (no install required) . **Best for**: Individuals wanting desktop personal finance with cash flow forecasting.



- **[Econumo](https://github.com/econumo/econumo)**

  **Self-hosted budgeting web app with envelope budgeting.** **MIT licensed**, in development since 2020, open-sourced November 2024 . **Key features**: Envelope budgeting; household sharing with per-item access; PWA mobile support; multi-currency; CSV import; **REST API with Swagger** . **Stack**: Go, SQLite or PostgreSQL . **Best for**: Households wanting self-hosted envelope budgeting with API access.



### Cash Flow Forecasting Skills & Frameworks



- **[cash-flow-forecaster Skill](https://skillsmp.com/zh/creators/miketreml/missioncontrol/library-business-finance-accounting-skills-cash-flow-forecaster)**

  **Comprehensive AI Agent Skill for cash forecasting.** **Capabilities**: Direct method forecasting (cash receipts, disbursements, payroll timing, tax scheduling, debt service, capex); Indirect method reconciliation (net income to cash flow bridge, working capital changes); **Working capital optimization** (DSO targets, DPO optimization, cash conversion cycle); **Liquidity stress scenarios** (revenue decline, customer concentration, supply chain disruption); Bank balance aggregation; Cash position optimization . **Integration**: Treasury management system APIs (Kyriba, GTreasury), bank connectivity platforms . **Best for**: Treasury and finance teams using AI assistants.



- **[financial-modeling](https://github.com/77it/financial-modeling)**

  **JavaScript-based financial modeling with cash flow forecast.** **Key features**: Financial modeling, business valuation, cash flow forecast, financial ratios, balance sheet . **Best for**: Developers wanting a lightweight financial modeling foundation.



### Additional Strong Open-Source Options



- **Personal Finance**: **Firefly III** (24k+ stars, double-entry, AGPL-3.0) , **Actual Budget** (29k+ stars, envelope budgeting, MIT) , **Money Manager Ex** (desktop, cash flow forecasting) , **Econumo** (self-hosted, envelope budgeting) .

- **CLI/Technical**: **cfo-cli** (terminal-first, AI insights, MCP server) .

- **Forecasting & Optimization**: **Equilibrium** (QUBO payment scheduling) , **AFIS** (ML projections, NIST governance) , **pycashflow** (Flask REST API, risk scoring) .

- **AI Skills**: **cash-flow-forecaster** (comprehensive treasury forecasting) , **financial-modeling** (JavaScript modeling) .

- **Small Business Accounting**: **Invoice Ninja** (10k+ stars, invoicing + cash flow) , **Akaunting** (10k+ stars, accounting with cash flow) .



**Frameworks for building custom systems**: Combine **Firefly III** or **Actual Budget** for the core ledger and cash flow reporting, **cfo-cli** for terminal-first forecasting with AI insights, **Equilibrium** for payment scheduling optimization, **AFIS** for ML-based 12-month projections, and **pycashflow** for REST API integration. Add **PostgreSQL** for persistence and **Docker** for deployment.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Cash flow management platforms handle sensitive financial data; ensure compliance with accounting standards and data protection regulations.

- **Open-source reality**: The open-source ecosystem for cash flow management is **developing but fragmented**. **Firefly III** and **Actual Budget** provide mature personal/small business finance management with cash flow reporting . **cfo-cli**, **Equilibrium**, **AFIS**, and **pycashflow** offer focused cash flow forecasting and optimization capabilities . However, **commercial platforms** (Pulse, Fathom, Float, Agicap) provide **integrated multi-entity consolidation, real-time bank feeds, scenario modeling at scale, and enterprise support** that open-source alternatives require significant assembly and engineering investment to match. The open-source path is most viable for **personal finance, small business cash flow, or technical teams building custom forecasting tools**.



---



**Made for CFOs, finance teams, founders, accountants, and treasury professionals.**

Let's make cash flow management more open, transparent, and predictive.
