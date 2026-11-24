# Klierbook

[![CI](https://github.com/SerjCallier/klierbook/actions/workflows/ci.yml/badge.svg)](https://github.com/SerjCallier/klierbook/actions)
![React](https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-FF6D5A?style=flat-square&logo=n8n&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Licencia](https://img.shields.io/badge/license-MIT-green?style=flat-square)

[English](README.md) | **Español**

> **SaaS de reservas sin suscripción** que convierte cualquier servicio profesional en una máquina de auto-agendamiento 24/7 — impulsado por React 19, TypeScript, orquestación con webhooks n8n y Google Sheets/Calendar.

---

## ¿Por qué Klierbook?

La mayoría de las herramientas de turnos cobran **$30–$80/mes** antes de que el negocio valide su demanda. Klierbook invierte el modelo: un frontend white-label en React conectado a un **backend serverless con n8n + Google Sheets**, ofreciendo una experiencia de reservas profesional con **costo fijo de base de datos igual a cero**.

**Diseñado para:** Spas, barberías, clínicas odontológicas, estudios de fitness y negocios de servicios por turnos.

---

## Características

| Funcionalidad | Descripción |
| :--- | :--- |
| **Flujo sin Fricción** | Wizard multi-paso: servicio → profesional → fecha/hora → confirmación sin recargas de página. |
| **Motor de Temas Dinámico** | Paletas curadas por rubro mediante `useNicheTheme` (barberías, salones, clínicas, gastronomía, deportes). |
| **Conversión Mobile-First** | Diseño responsive optimizado para pantallas táctiles con Tailwind CSS. |
| **Integración n8n** | Dispara payloads de reserva a un workflow n8n (`n8n_create_booking_workflow.json`) que sincroniza Google Sheets, Calendar y confirmaciones. |
| **Soporte i18n** | Bilingüe completo (EN/ES) con `react-i18next` y formateo de fechas por locale con `date-fns`. |

---

## Inicio Rápido

```bash
git clone https://github.com/SerjCallier/klierbook.git
cd klierbook

npm install
npm run dev      # Servidor local en http://localhost:5173
npm run build    # Typecheck TypeScript + bundle de producción Vite
```

---

## Licencia

MIT © [Sergio Callier](https://github.com/SerjCallier)
