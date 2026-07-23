# Educational Travel Adventures

We've specialized in operating customized educational tours, school trips & performance tours for students since 1991. So let us know where you want to go!

This GitHub organization hosts the software that runs the business — booking, operations, finance, and the customer/guide-facing portals.

→ Company site: https://etadventures.com · Contact: it@etadventures.com

## What we build

**Tourbot** is the central custom ERP that sales, operations, accounting, and management use to run the business. It's a long-lived PHP / MySQL monorepo that also powers three outward-facing portals, all sharing the same database and integration services.

The four surfaces served from the Tourbot monorepo:

| Surface | Audience |
| --- | --- |
| **mtourbot** | Internal staff (sales, ops, accounting, management) |
| **customerweb** | Group leaders, parents & students |
| **guides** | Tour-guide contractors |
| **api** | REST API for internal services and the in-flight SPA |

## Tech stack

- **Core:** PHP 8 & MySQL 8
- **API:** Slim 3 JSON REST API
- **Architecture:** monorepo — modern PSR-4 / object-oriented code under `src/` and `neuron/`, alongside long-lived procedural code
- **Runtime:** Apache web server; PM2 for long-running PHP daemons; ~50 scheduled cron jobs
- **Auth:** Google OAuth (internal staff), group-code login (customers), email/password (guides)
- **Integrations:** Twilio, Mandrill, Mailchimp, Pusher, and NMI / M&T for payments

## Repositories

The two repositories worked in day to day:

- **`tourbot`** — the monorepo: the ERP, the REST API, the customer and guide portals, and most of ETA's web properties.
- **`manager-tourbots`** — Docker Compose + config for the manager-sandbox containers.

## Documentation

Internal engineering documentation lives at https://docs.etadventures.com (access-restricted). It covers the company overview, infrastructure, the Tourbot application and API, and how code ships to production.

---

<sub>🌍 Operating student travel adventures since 1991.</sub>
