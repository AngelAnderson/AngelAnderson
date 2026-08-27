# Angel Anderson

**I build verified local data infrastructure for Puerto Rico.**

Solo operator. Air Force veteran (20 years). MBA. Cabo Rojo, Puerto Rico. No employees, just AI.

Most local data is scraped, inherited, and never checked again. Every office you call makes you re-prove what another office already proved. I am building the opposite: a substrate where the check is the product, and where the check says who did it and when.

---

## The scoreboard

Verified against the live database on 2026-08-27. The query is in [MapaDeCaboRojo-v1.0](https://github.com/AngelAnderson/MapaDeCaboRojo-v1.0).

| Number | What it is |
|---|---|
| **35,621** | Published records across Puerto Rico |
| **78** | Municipalities covered (all of them) |
| **30,622** | Records matched to the federal NPPES registry |
| **292** | Records a **human** actually confirmed |
| **676** | Real demand signals from 374 real people, last 90 days |
| **0** | Employees |

That fourth row is the honest one: **0.8%**. Everything else is imported, and imported is not verified. A record copied from a federal registry is the same record the insurance plan already has, so it inherits nothing and I do not sell it as a check. Closing that gap is the actual work, and I publish the number every time it moves.

If a directory does not show you this ratio, it has one too.

---

## Where the system ends

Named on purpose, because these are the seams:

- **The phone call.** Of 157 provider numbers measured against Twilio Lookup, only 39.5% are mobile. A text does not reach the rest. Confirming "does this office still take her plan" ends at a human dialing a front desk during business hours, and that human is me.
- **The claim form nobody fills out.** Crowdsourced confirmations are the cheapest path to a verified record and the slowest one in practice.
- **Absence.** Proving a town has no cardiologist is harder than listing the ones it has, and it is the fact that actually changes what a family does next.

---

## How a record gets verified

Five rules, each one paid for with a real incident:

1. **Imported is not verified.** The claim is partitioned by source or it is not made.
2. **A synthetic filter is defined by the source of the traffic, never by the channel.** Every new channel arrives unfiltered by default.
3. **A zero is not evidence.** A section with no instrumentation reports "not measured", not "none".
4. **The seal names who confirmed it.** Three levels: a person, a corroborating source, or a registry copy that claims nothing.
5. **An internal fact expires too.** Every number carries the date it was checked, including the ones in this file.

---

## What is running

| | |
|---|---|
| [**registromedicopr.com**](https://registromedicopr.com/registro) | Puerto Rico medical specialists, matched to NPPES. Search by symptom, town, or insurance plan. Bilingual |
| [**mapadecaborojo.com**](https://www.mapadecaborojo.com) | Verified map and directory for Cabo Rojo |
| [**puertoricosinfiltros.com**](https://puertoricosinfiltros.com) | Civic records: the number, the source, and what to do with it |
| [**caborojo.com**](https://www.caborojo.com) | The local publication the whole thing feeds |
| **El Veci** | Text **787-417-7711** or [WhatsApp](https://wa.me/17874177711). Answers in Spanish, 24/7, since 2026 |

**For machines:** [api.vecinoai.com](https://api.vecinoai.com/?action=docs) is open. There is also an MCP server, `pr-publico`, that publishes its own error bars: ask it `verificacion_estado` and it tells you how much of the data is fresh **before** you use it.

```bash
curl 'https://api.vecinoai.com?q=pizza'
```

Unique to this substrate: the historical archive of provider directories published by Puerto Rico health plans, paired against NPPES. It can answer whether a doctor is still in network and whether the phone number the plan printed is the right one. Nobody else kept those files.

---

## Stack

`TypeScript` `Supabase` `Postgres` `Deno` `Vercel` `Next.js` `Twilio` `MCP` `OpenAI` `Anthropic`

Designed, built, deployed, and operated by one person using AI as the entire engineering team. The code is real, the users are real, and the revenue is real.

---

## One door

If you run a newsroom, a health plan, or a municipality and you need Puerto Rico data with a verifiable check on it, write me: **angel@angelanderson.com**. Tell me what you are trying to prove. No deck, no call needed.

If you are here for the method instead of the data, take it. That is what this file is for.

[angelanderson.com](https://angelanderson.com) · [@angelfanderson](https://x.com/angelfanderson) · Cabo Rojo, Puerto Rico
