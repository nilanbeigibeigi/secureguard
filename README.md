# SecureGuard — Browser-Based Security Suite

A hands-on cybersecurity demo that runs **entirely in the browser**: a live threat dashboard, a phishing checker, and a password lab. No backend, no data leaves the page.

**Live demo:** https://nilanbeigibeigi.github.io/secureguard/
**Author:** Nilan Beigi — [portfolio](https://nilanbeigibeigi.github.io/Nilan-Portfolio/) · [GitHub](https://github.com/nilanbeigibeigi)

---

## The problem

Small teams and individuals rarely have access to enterprise security tooling, and security concepts stay abstract. SecureGuard makes them tangible with tools you can actually try — while keeping everything local and private.

## What it does

- **Threat dashboard** — live metrics: threats blocked (24h), active alerts, monitored endpoints, critical incidents, an attack-type breakdown, and an incident feed with timestamps.
- **Phishing check** — paste a suspicious email/message; it's scored against **20+ real scam signals** (urgency, credential requests, mismatched links, etc.) and returns a risk score with the reasons.
- **Password lab** — estimates password **entropy (bits)** and **crack-time**, and explains what makes a password strong.
- **Protection overview** — how the pieces map to real defensive practices (endpoint protection, email filtering, MFA, SOC monitoring, compliance).

## How it works

All analysis runs client-side in JavaScript. The phishing checker uses a transparent, rule-based signal set (each flagged reason is shown), and the password lab computes entropy from the character space and length. Nothing is transmitted — you can run it offline.

## Tech

- HTML / CSS / JavaScript, fully static
- Client-side detection rules + entropy math
- Deployed on GitHub Pages

## Run locally

```bash
git clone https://github.com/nilanbeigibeigi/secureguard
cd secureguard
# open index.html, or:
npx serve .
```

## Threat model & scope

This is an **educational** tool, not production security software. It demonstrates detection *logic* and security literacy. It does not scan real traffic, store data, or replace real endpoint/email protection.

## Roadmap

- Real log ingestion and a documented detection ruleset
- A written threat model (assets, adversaries, mitigations)
- Exportable incident reports

*Part of my path toward cybersecurity — pairing defensive fundamentals with things I can build and ship.*
