# Klierbook

[![CI](https://github.com/SerjCallier/klierbook/actions/workflows/ci.yml/badge.svg)](https://github.com/SerjCallier/klierbook/actions)
![React](https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-FF6D5A?style=flat-square&logo=n8n&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)

**English** | [Español](README.es.md)

> **Zero-subscription booking SaaS** that turns any professional service into a 24/7 self-scheduling machine — powered by React 19, TypeScript, n8n webhook orchestration, and Google Sheets/Calendar.

---

## Why Klierbook?

Most booking tools lock small businesses into **$30–$80/month subscriptions** before they've even validated demand. Klierbook flips that model: a white-label React frontend connected to a **serverless n8n + Google Sheets backend**, delivering an enterprise-grade booking experience at **zero recurring database cost**.

**Built for:** Spas, barbershops, dental clinics, fitness studios, and service-based businesses.

---

## Features

| Feature | Description |
| :--- | :--- |
| **Frictionless Booking Flow** | Multi-step wizard: service → professional → date/time → confirmation. Zero page reloads. |
| **Dynamic Theming Engine** | Curated niche palettes via `useNicheTheme` (barbershops, beauty salons, clinics, gastronomy, sports). |
| **Mobile-First Conversion** | Thumb-friendly responsive layout built with Tailwind CSS. |
| **n8n Webhook Integration** | Fires booking payloads to an n8n workflow (`n8n_create_booking_workflow.json`) syncing Google Sheets, Calendar, and email confirmations. |
| **i18n Ready** | Full bilingual support (EN/ES) with `react-i18next` and `date-fns` locale formatting. |

---

## Architecture

```mermaid
sequenceDiagram
    participant User as End Client
    participant App as Klierbook Frontend
    participant n8n as n8n Orchestrator
    participant GCP as Google Sheets & Calendar
    participant Mail as Transactional Mail

    User->>App: Selects service, pro & slot
    App->>App: Client-side validation & preview
    App->>n8n: POST /webhook (booking payload)
    n8n->>GCP: Append row -> Google Sheets
    n8n->>GCP: Create event -> Google Calendar
    n8n->>Mail: Send confirmation email
    Mail-->>User: Booking confirmed
```

---

## Quick Start

```bash
git clone https://github.com/SerjCallier/klierbook.git
cd klierbook

npm install
npm run dev      # Local development server at http://localhost:5173
npm run build    # TypeScript check + Vite production bundle
```

---

## License

MIT © [Sergio Callier](https://github.com/SerjCallier)
