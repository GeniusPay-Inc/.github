<div align="center">

<img src="https://raw.githubusercontent.com/GeniusGroups/GeniusPay/main/public/assets/logo-white.svg" alt="GeniusPay" width="120" />

# GeniusPay

### L'infrastructure de paiement qui propulse l'Afrique

[![Website](https://img.shields.io/badge/🌐_geniuspay.ci-0066FF?style=for-the-badge)](https://geniuspay.ci)
[![Admin](https://img.shields.io/badge/📊_Dashboard-6366f1?style=for-the-badge)](https://app.geniuspay.ci)
[![Docs](https://img.shields.io/badge/📖_API_Docs-22C55E?style=for-the-badge)](https://docs.geniuspay.ci)
[![Webhook](https://img.shields.io/badge/🐳_Gateway-FF9900?style=for-the-badge)](https://wh.geniuspay.ci)

<br />

**Le produit phare de [GENIUS GROUPS SAS](https://geniusgroups.ci) — opéré par [GeniusPay, INC.](https://geniuspay.ci)**

Une infrastructure de paiement multi-provider, multi-pays et multi-devises conçue pour le marché africain.
Smart Routing, Webhook Gateway dédiée, Wallet, Cash-Out, KYC/KYB, Subscriptions, Merchant API, CRM OS — tout dans une seule plateforme.

<br />

Made with ❤️ in Abidjan, Côte d'Ivoire 🇨🇮

</div>

---

## Vue d'ensemble

GeniusPay n'est pas une seule application — c'est un **écosystème de 20+ services** qui travaillent ensemble pour former une plateforme de paiement complète, du traitement des transactions au support client, en passant par l'onboarding marchand, la surveillance temps réel et les SDK multi-plateformes.

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

## Roadmap

- [ ] **AI Fraud Detection** — détection de fraude en temps réel (ML)
- [ ] **Multi-tenant** — support white-label pour partenaires
- [ ] **Real-time dashboard** — WebSocket pour monitoring live
- [ ] **Provider failover** — bascule automatique entre providers en cas d'incident
- [ ] **Settlement engine** — calcul automatique des règlements marchand
- [ ] **PCI-DSS** — certification pour traitement cartes
- [ ] **GeniusPay Certify** — parcours certifiant marchands (Next.js + Judge0)
- [ ] **GeniusFX** — API de taux de change BCEAO en production

---

## Organisation

**GeniusPay** est développé et opéré par **GeniusPay, INC.**, filiale de **GENIUS GROUPS SAS**.

- 🏢 **GENIUS GROUPS SAS** — [geniusgroups.ci](https://geniusgroups.ci)
- 🏦 **GeniusPay, INC.** — [geniuspay.ci](https://geniuspay.ci)
- 📧 **Contact** — [contact@geniuspay.ci](mailto:contact@geniuspay.ci)
- 📍 Abidjan, Côte d'Ivoire 🇨🇮

---

<div align="center">

**GeniusPay** — *L'infrastructure de paiement qui propulse l'Afrique.*

</div>
