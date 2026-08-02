<div align="center">

<img src="https://geniuspay.ci/assets/logo-white.svg" alt="GeniusPay" width="120" />

### The Payment Operating System for Africa

<p>
  <em>Building the most comprehensive payment infrastructure on the continent.</em>
</p>

[![Website](https://img.shields.io/badge/🌐_geniuspay.ci-0066FF?style=for-the-badge)](https://geniuspay.ci)
[![Admin](https://img.shields.io/badge/📊_Dashboard-6366f1?style=for-the-badge)](https://app.geniuspay.ci)
[![Docs](https://img.shields.io/badge/📖_API_Docs-22C55E?style=for-the-badge)](https://docs.geniuspay.ci)
[![Webhook](https://img.shields.io/badge/🐳_Gateway-FF9900?style=for-the-badge)](https://wh.geniuspay.ci)

<br />

**A [GENIUS GROUPS SAS](https://geniusgroups.ci) company — operated by [GeniusPay, INC.](https://geniuspay.ci)**

<br />

<table>
<tr>
<td align="center">🌍 <b>1.4B people</b><br/><sub>addressable market</sub></td>
<td align="center">📱 <b>$1.3T</b><br/><sub>mobile money by 2030</sub></td>
<td align="center">🚀 <b>20+ services</b><br/><sub>shipping in production</sub></td>
<td align="center">🇨🇮 <b>Abidjan</b><br/><sub>built in Africa, for Africa</sub></td>
</tr>
</table>

<br />

> **Our mission:** Become the financial rails that power every transaction in Africa —
> from the street vendor accepting their first mobile payment to the enterprise processing millions.


</div>

---

## The Opportunity

### Why Africa, Why Now

Africa is the **fastest-growing mobile money market in the world**. The continent processes over **$700B annually** in mobile money transactions, growing 20%+ year-over-year. Yet payment infrastructure remains fragmented across:

- **50+ countries**, each with different currencies, regulations, and providers
- **20+ mobile money operators** (Orange, MTN, Wave, Moov, Airtel, Safaricom…)
- **No unified API layer** — merchants must integrate each provider separately
- **Sub-30% card penetration** — mobile money is the dominant rail, not cards

### The Problem We Solve

Every African merchant faces the same nightmare:

1. **Fragmentation** — 10+ payment providers, each with its own API, webhook format, and dashboard
2. **No reconciliation** — matching transactions across providers is manual and error-prone
3. **No wallet** — consumers can't store funds; every payment requires a fresh USSD flow
4. **No onboarding** — KYC/KYB processes are paper-based and take weeks
5. **No support tooling** — customer service teams have no unified view of transactions

### Our Answer: One Platform, Every Rail

GeniusPay is a **single integration** that gives merchants access to every payment method in Africa — with built-in reconciliation, wallet, KYC, subscriptions, CRM, and developer tooling that rivals Stripe.

---

## Vision: The Path to Unicorn

<div align="center">

```
  ┌─────────────────────────────────────────────────────────────────┐
  │                     THE GENIUSPAY THESIS                        │
  │                                                                 │
  │  Stripe unified payments in the US → $70B valuation             │
  │  Adyen unified payments in Europe → $50B valuation              │
  │  PhonePe unified payments in India → $12B valuation             │
  │                                                                 │
  │  Nobody has unified payments in Africa yet.                     │
  │                                                                 │
  │  That's what GeniusPay is building.                             │
  └─────────────────────────────────────────────────────────────────┘
```

</div>

### What Makes Us Different

| Moat | Description |
|------|-------------|
| **Multi-provider orchestration** | 10+ payment providers unified behind a single API — no competitor in West Africa offers this breadth |
| **Smart Routing engine** | Automatic provider selection based on cost, success rate, and latency — reduces transaction failure by up to 40% |
| **Wallet + Identity layer** | Genius Wallet (PWA) + GeniusAuth (OIDC/Passkeys) create a network effect — every new user increases value for every merchant |
| **Full-stack ecosystem** | Not just payments: CRM OS, KYC/KYB onboarding, partner commissions, certification program, FX rates, invoicing — all native |
| **Developer-first** | 5 SDKs (Flutter, React, Laravel, WooCommerce, GeniusAuth) + API Playground + MCP Server for AI-assisted integration |
| **Built in Africa** | Team based in Abidjan — we understand the market, the regulators, and the users better than any foreign player |

### Business Model

| Revenue stream | Mechanism |
|----------------|-----------|
| **Transaction fees** | 1.5–3.5% per transaction (volume-based pricing) |
| **Subscription tiers** | SaaS plans for CRM, analytics, advanced features |
| **Wallet float** | Interest on stored balances (Genius Wallet) |
| **Partner commissions** | Revenue share with distribution partners |
| **FX margin** | Spread on currency conversions (GeniusFX) |
| **Certification** | Premium training & certification for merchants |
| **Enterprise contracts** | Custom integrations for banks & telcos |

### Traction & Growth Signals

- **20+ services** already shipping in production — not a prototype, a real platform
- **10+ payment providers** integrated and live (Paystack, Wave, PawaPay, CinetPay, Stripe, PaiementPro, Orange, MTN, Moov, PAL)
- **5 SDKs** published across pub.dev, npm, and Packagist
- **Multi-market ready** — Côte d'Ivoire live, expansion planned for Senegal, Benin, Togo, Burkina Faso, Mali
- **Self-hosted infrastructure** — Coolify + Docker, keeping cloud costs 10x lower than AWS-native competitors
- **AI-native operations** — MCP Server, DIA voice assistant, AI-powered ticket classification

---

## The Ecosystem

GeniusPay is not a single application — it's a **vertically integrated ecosystem of 20+ services** covering the entire payment lifecycle: from transaction processing to merchant onboarding, customer support, developer tooling, and financial infrastructure.

### Architecture de l'écosystème

```
                    ┌──────────────────────────────────────────────────────┐
                    │                    UTILISATEURS                       │
                    │   Marchands    │   Clients    │   Partenaires      │
                    └───────┬────────┴──────┬────────┴────────┬───────────┘
                            │               │                 │
                    ┌───────▼───────┐ ┌─────▼──────┐ ┌───────▼────────┐
                    │  Merchant     │ │  Genius    │ │   GeniusPay    │
                    │  Mobile App   │ │  Wallet    │ │   Partners     │
                    │  (Flutter)    │ │  (PWA)     │ │  (Laravel+React)│
                    └───────┬───────┘ └─────┬──────┘ └───────┬────────┘
                            │               │                 │
                    ┌───────▼───────────────▼─────────────────▼─────────┐
                    │                   GENIUSPAY CORE                     │
                    │              (Laravel 12 — API principale)           │
                    │  API · Checkout · Wallet · KYC · Subs · Fees         │
                    └───────────────────────┬────────────────────────────┘
                                            │
                    ┌───────────────────────▼────────────────────────────┐
                    │              WEBHOOK API GATEWAY                     │
                    │              (FastAPI — microservice Python)         │
                    └───────────────────────┬────────────────────────────┘
                                            │
                    ┌───────────┬───────────┬┴──────────┬─────────────────┐
                    ▼           ▼           ▼           ▼                 ▼
              ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌────────────┐
              │ Waitlist │ │  Scale   │ │ Tracking │ │   API    │ │    SDK     │
              │ Service  │ │ Monitor  │ │   UI     │ │PlayGround│ │  (Flutter, │
              │(Laravel) │ │ (React)  │ │ (React)  │ │   (PHP)  │ │  Laravel,  │
              └──────────┘ └──────────┘ └──────────┘ └──────────┘ │  React,    │
                                                                     │  WooCommerce)│
                    ┌────────────────────────────────────────────┐ └────────────┘
                    │              SERVICES SUPPORT               │
                    │  CRM OS · DIA Monitor · MCP Server          │
                    │  Certify · GeniusFX · GeniusAuth            │
                    └────────────────────────────────────────────┘
```

---

## Catalogue des repositories

### Plateforme Core

| Repo | Stack | Rôle |
|------|-------|------|
| **GeniusPay** | Laravel 12 + PHP 8.3 + PostgreSQL + Redis | API principale — orchestrateur de paiement multi-provider (10+ providers), Smart Routing, Wallet, KYC/KYB, Subscriptions, Checkout, Merchant API |
| **GeniusDemo** | Laravel + Docker + Coolify | Environnement de staging/démo de GeniusPay — déploiement Coolify, docker-compose production |
| **GeniusPayLoad** | Laravel | Plateforme de paiement interne v1 (legacy) — gestion centralisée des paiements GENIUS GROUPS, reconciliation comptable |

### Microservices

| Repo | Stack | Rôle |
|------|-------|------|
| **GeniusPayWebhookAPIGateway** | Python + FastAPI + PostgreSQL | Microservice de réception webhooks — vérification de signature, idempotency, fan-out, retry, archivage, recovery, dashboard admin |
| **GeniusPayWaitlist** | Laravel 13 + Filament 5 + PostgreSQL + Redis | Microservice d'onboarding marchand — inscription multi-étapes, KYC/KYB, validation documentaire, activation, provisionnement clés API |
| **GeniusPartners** | Laravel + React | Microservice partenaires — API commission engine, wallet partenaires, onboarding |
| **GENIUS_CRM_OS** | Laravel 13 + React 19 + PostgreSQL + Redis + Reverb | CRM/Support OS — prise en charge réclamations, incidents, tickets, feedbacks, moniteur vocal, écran mural Spacewalk, classification IA |

### Applications Frontend

| Repo | Stack | Rôle |
|------|-------|------|
| **GeniusWallet-App** | React 19 + TypeScript + Vite + TailwindCSS + Zustand + TanStack Query | Wallet client PWA — top-up Mobile Money, paiement biométrique (WebAuthn/Face ID), checkout instantané, assistant Geni |
| **geniuspay_merchant_mobile** | Flutter + Dio + FlutterBloc + GoRouter + Firebase | App mobile marchand — gestion transactions, payouts, wallet, notifications push, auth biométrique |
| **geniuspay-tracking-ui** | React 18 + TypeScript + Vite + Turborepo + shadcn/ui + TanStack Query | Micro-frontend tracking transactions temps réel — marchands, clients (guests), admins |
| **GeniusPayScaleMonitor** | React 19 + TypeScript + Vite + Recharts + TailwindCSS | Dashboard KPI live — suivi croissance 90 jours (marchands, transactions, volumes, revenus), mode TV plein écran |

### Monitoring & Intelligence

| Repo | Stack | Rôle |
|------|-------|------|
| **JarvisMonitor** | PHP + JavaScript + SSE | DIA (Digital Intelligence Assistant) — interface de surveillance temps réel style JARVIS, synthèse vocale, commandes vocales, statistiques live |
| **GeniusPayMCPServer** | Laravel + MCP (SSE) | Serveur Model Context Protocol — permet aux assistants IA (Claude, Cursor, Windsurf) d'accéder à la doc API et aux logs d'erreurs pour déboguer l'intégration |

### Éducation & Certification

| Repo | Stack | Rôle |
|------|-------|------|
| **GeniusPayCertify** | Next.js 14 + Prisma + PostgreSQL + Judge0 + Monaco Editor | Parcours certifiant marchands — formation interactive, exercices de complétion, playground de code, scoring, certificat PDF, partage LinkedIn |
| **GeniusPayAPIPlayGround** | PHP | Sandbox de test API — formulaires de test pour l'intégration marchand, visualiseur de logs webhook |

### Infrastructure Financière

| Repo | Stack | Rôle |
|------|-------|------|
| **GeniusFX** | Python 3.13 + FastAPI + PostgreSQL + Redis + APScheduler | API de taux de change — données officielles BCEAO, scraper, cache, dashboard admin React |
| **genius-invoice** | API REST + GeniusPay intégré | Genius Invoice — workspace de facturation intelligent pour l'Afrique, intégration GeniusPay, Genius Identity SSO |

### Identité & Authentification

| Repo | Stack | Rôle |
|------|-------|------|
| **GeniusAuth_** | Multi-composants (geniusauth, vault, opsdashboard, js-sdk, laravel-sdk) | Plateforme d'identité GeniusPay — OIDC, Passkeys, Identity Linking, GeniusID lookup, apps connectées |

### SDKs officiels

| Repo | Stack | Rôle |
|------|-------|------|
| **geniuspay-flutter** | Flutter / Dart | SDK Flutter — paiements Wave, Orange Money, MTN Money, Moov Money, carte bancaire. Publié sur pub.dev |
| **geniuspay-react** | React / TypeScript | SDK React — composants `<PaymentButton>`, `<PaymentForm>`, `<PaymentStatus>`, hooks `useGeniusPay()`, `usePayment()`. Publié sur npm |
| **geniuspay-laravel** | Laravel / PHP | SDK Laravel — Facade `GeniusPay`, Trait `HasGeniusPayPayments`, webhooks automatiques, events. Publié sur Packagist |
| **geniuspay-woocommerce** | WordPress / PHP | Extension WooCommerce — paiement Mobile Money + carte, webhooks, compatible HPOS. Publié (v1.1) |
| **geniusauth-react** | React / TypeScript | SDK React GeniusAuth — OIDC + PKCE, Identity Linking, GeniusID lookup, composants `<AuthCallback>`, `<LinkHandler>`. Publié sur npm |

---

## Providers de paiement supportés

| Provider | Type | Pays couverts |
|----------|------|---------------|
| **Paystack** | Cartes + Mobile Money | NG, GH, CI, ZA, KE |
| **Wave** | Wallet | SN, CI |
| **PawaPay** | Mobile Money Multi-Pays | 12+ pays africains |
| **CinetPay** | Mobile Money + Cartes | CI, SN, CM, BF, TG… |
| **Stripe** | Cartes internationales | Global |
| **PaiementPro** | Mobile Money | CI |
| **PAL** | Wallet local | CI |
| **Orange Money** | Mobile Money | CI, SN, ML… |
| **MTN MoMo** | Mobile Money | CI, UG, CM, RW… |
| **Moov Money** | Mobile Money | CI, BF, TG… |

---

## Stack technique globale

| Couche | Technologies |
|--------|-------------|
| **Backend** | PHP 8.3 (Laravel 12/13), Python 3.13 (FastAPI), Node.js (Next.js 14) |
| **Frontend** | React 19, TypeScript 6, Vite 8, TailwindCSS 4, shadcn/ui, Zustand, TanStack Query |
| **Mobile** | Flutter, Dart, FlutterBloc, GoRouter, Firebase |
| **Bases de données** | PostgreSQL 15/16, Redis 7, Prisma |
| **Temps réel** | Laravel Reverb (WebSockets), SSE (Server-Sent Events) |
| **Infrastructure** | Docker, Coolify (self-hosted PaaS), AWS S3, Cloudflare |
| **CI/CD** | GitHub Actions, Coolify auto-deploy |
| **Monitoring** | Horizon (queues), Spatie Activity Log, DIA Monitor, Scale Monitor |
| **IA** | OpenRouter (classification), Gemini (embeddings), MCP Server, DIA |

---

## URLs de production

| Service | URL |
|---------|-----|
| App principale | `https://app.geniuspay.ci` |
| Website | `https://geniuspay.ci` |
| API Docs | `https://docs.geniuspay.ci` |
| Webhook Gateway | `https://wh.geniuspay.ci` |
| Admin Dashboard | `https://app.geniuspay.ci/admin` |

---

## Roadmap to Scale

### Phase 1 — Dominate West Africa (2025–2026)

- [x] Core payment platform live in Côte d'Ivoire
- [x] 10+ payment providers integrated
- [x] Wallet PWA with biometric authentication
- [x] CRM OS for merchant support
- [x] 5 SDKs published (Flutter, React, Laravel, WooCommerce, GeniusAuth)
- [ ] **AI Fraud Detection** — real-time ML-based fraud scoring
- [ ] **Provider failover** — automatic failover between providers on incident
- [ ] **Settlement engine** — automated merchant settlement calculation
- [ ] **GeniusPay Certify** — merchant certification program (Next.js + Judge0)
- [ ] **GeniusFX** — BCEAO exchange rate API in production
- [ ] **Multi-country expansion** — Senegal, Benin, Togo, Burkina Faso, Mali

### Phase 2 — Pan-African Scale (2026–2027)

- [ ] **20+ countries** live across West, East, and Central Africa
- [ ] **Multi-tenant** — white-label platform for banks & telcos
- [ ] **PCI-DSS Level 1** — certification for card processing
- [ ] **Real-time dashboard** — WebSocket-based live monitoring
- [ ] **1M+ active merchants** on the platform
- [ ] **$1B+ annual transaction volume**

### Phase 3 — The Unicorn (2027–2028)

- [ ] **Series A → B** — raise institutional capital at unicorn valuation
- [ ] **B2B2C network** — Genius Wallet as the default consumer payment identity
- [ ] **Lending & BNPL** — leverage transaction data for merchant credit scoring
- [ ] **Cross-border payouts** — enable merchants to pay suppliers across Africa
- [ ] **$10B+ annual transaction volume**
- [ ] **IPO-ready** — regulatory compliance, audited financials, governance

---

## Why We'll Win

1. **We're not building a feature — we're building infrastructure.** Payment providers come and go. GeniusPay sits above them all, routing intelligently, reconciling automatically, and owning the merchant relationship.

2. **We own the full stack.** From the wallet on the consumer's phone to the CRM on the merchant's desk to the webhook gateway in the back — no competitor in Africa has this depth.

3. **We're developer-obsessed.** 5 SDKs, an API playground, an MCP server for AI-assisted integration, and a certification program. We're building the Stripe-level developer experience that Africa has never had.

4. **We're born in Africa.** Our team lives the problems we solve. We understand Wave, Orange Money, MTN MoMo — not as API docs, but as daily reality.

5. **We're capital-efficient.** Self-hosted on Coolify, Docker-native, lean team. We ship like a 100-person company with 10. That's how you build a unicorn without burning $100M.

---

## Organisation

**GeniusPay** is developed and operated by **GeniusPay, INC.**, a subsidiary of **GENIUS GROUPS SAS**.

- 🏢 **GENIUS GROUPS SAS** — [geniusgroups.ci](https://geniusgroups.ci)
- 🏦 **GeniusPay, INC.** — [geniuspay.ci](https://geniuspay.ci)
- 📧 **Contact** — [contact@geniuspay.ci](mailto:contact@geniuspay.ci)
- 📍 Abidjan, Côte d'Ivoire 🇨🇮

---

<div align="center">

**GeniusPay** — *The Payment Operating System for Africa.*

*Building the next African unicorn — one transaction at a time.* 🦄

</div>
