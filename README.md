# Commercial Representation CRM

![HTML](https://img.shields.io/badge/HTML%2FCSS%2FJS-vanilla-orange) ![Node](https://img.shields.io/badge/Node.js-18%2B-green) ![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)

**A CRM built for one specific job: managing commercial representation of several logistics companies at the same time — pipeline, quotes, approvals and commissions — without mixing one principal's numbers with another's.**

> Built by **Marcelo Gurgel Carvalho** — 15+ years in commercial management for ports, shipping and logistics in Northeast Brazil.

## The business problem

A commercial representative selling for several logistics providers (shipping, freight forwarding, cabotage) works the same customer for more than one principal. Off-the-shelf CRMs treat each deal as one company/one product, so pipeline value, forecast and commissions get mixed — and reports sent to a principal risk exposing another principal's data.

## What it does

| Module | Delivers |
|---|---|
| **Pipeline (Kanban)** | Salesforce-style stages with win probabilities; drag & drop; filter by principal |
| **Multi-principal opportunities** | One opportunity per customer, one line per principal — each with its own stage, volume (containers/month) and history |
| **Revenue & commission** | Annual revenue from quoted items; monthly and probability-weighted commission per principal, with FX conversion |
| **Quotes** | Product catalog × quantity × discount, auto-numbered proposals, printable customer document (no internal data) |
| **Approval matrix** | Three sequential approval levels with suggested discount and comments |
| **Calendar & email sync** | Imports meetings and emails as activities |
| **Compliance** | CNPJ validation, including Brazil's 2026 alphanumeric format |
| **Reports** | Report per principal (never shows another principal's data) and CSV export |

## Technical decisions

- **Single-file app:** HTML, CSS and vanilla JavaScript — no framework, no build step.
- **Pluggable data layer:** the app talks to a small database interface (`collection / doc / onSnapshot`). Locally, a zero-dependency Node server persists it to JSON; the same interface can be pointed to SQLite, Supabase or Firebase.
- **Derived fields computed on save** so the pipeline, forecast and commission views stay consistent per principal.

---

## 🇧🇷 Resumo em português

CRM criado para **representação comercial de várias empresas de logística ao mesmo tempo**. Cada oportunidade tem uma linha por representada, com fase, volume e histórico próprios, então funil, previsão e comissão nunca se misturam. Inclui cotação com catálogo de produtos, matriz de aprovação em 3 níveis, documento para o cliente sem dados internos, sincronização de agenda e e-mail, validação de CNPJ (inclusive alfanumérico de 2026) e relatório por representada. App em arquivo único (HTML/JS puro) com servidor local em Node sem dependências.

*Source code is private. Demo available on request.* · [LinkedIn](https://www.linkedin.com/in/marcelo-gurgel-b-carvalho-04770886)
