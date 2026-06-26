# MCAPS OS — Overview Site

<div align="center">

![Microsoft](https://img.shields.io/badge/Microsoft-MCAPS%20OS-0078D4?style=for-the-badge&logo=microsoft)

## MCAPS OS — one operating system, every persona

*A digital field team that builds, an outcome-first pipeline that governs, and the window that drives it.*

**Live (Microsoft-internal preview):** https://billwhalenmsft.github.io/mcaps-os/

</div>

---

### What is MCAPS OS?

It started as **SE-OS** — one Solution Engineer's operating system. It's grown into **MCAPS OS**:
the same core, activated for every persona in the MCAPS field motion. One app, one front door —
seen through the lens of whoever you are.

| Lens | Unit | Personas | Endpoint |
|---|---|---|---|
| **MCAPS OS** | the whole system | every persona | [`/`](https://billwhalenmsft.github.io/mcaps-os/) |
| **ATU OS** | Account Team Unit | AE · ATS · ATM | [`/atu/`](https://billwhalenmsft.github.io/mcaps-os/atu/) |
| **STU OS** | Specialist Team Unit *(most built-out)* | SSP · SE + managers | [`/stu/`](https://billwhalenmsft.github.io/mcaps-os/stu/) |
| **CSU OS** | Customer Success Unit | CSAM · CSA | [`/csu/`](https://billwhalenmsft.github.io/mcaps-os/csu/) |

Same core, four motions: ATU owns the account, STU proves the technical case, CSU makes the win real and grows it.

---

### 🔒 Microsoft-internal soft gate

Every page is wrapped by `gate.js`, a **render-blocking Microsoft-internal interstitial**: the page
will not paint until the visitor confirms a Microsoft identity (an `@microsoft.com` address), and the
choice is remembered per browser.

> **This is a soft (display) gate, not a security boundary.** GitHub Pages is static hosting with no
> server-side auth, so a determined external user can still read the raw HTML over the wire. The durable
> **hard gate** is MSAL.js against a single-tenant (microsoft.com) Entra app registration, or moving the
> content behind Azure Static Web Apps Standard. Tracked in the main repo backlog as
> `mcapsos-identity-msal-corp-tenant`.

---

### 📁 In this repo

```
mcaps-os/
├── index.html        MCAPS OS umbrella overview (Clawpilot theme, self-contained)
├── gate.js           Microsoft-internal soft gate (loaded first in <head> on every page)
├── lens.css          Shared theme + components for the unit sub-OS pages
├── atu/index.html    ATU OS — Account Team Unit lens
├── stu/index.html    STU OS — Specialist Team Unit lens (most built-out)
├── csu/index.html    CSU OS — Customer Success Unit lens
├── prototypes/       Embedded prototypes (mobile decision inbox)
├── img/              Screenshot assets
└── README.md         This file
```

**Technology:** HTML5, CSS3 (light/dark via `prefers-color-scheme` + `?scoutTheme=`), vanilla JS. No build step.

---

### 🔗 Resources

- **Live site:** https://billwhalenmsft.github.io/mcaps-os/ *(formerly `/se-os-overview/` — GitHub redirects renamed-repo Pages after propagation)*
- **Main repo:** [billwhalenmsft/SE-OS](https://github.com/billwhalenmsft/SE-OS) — see `/AGENTS.md` for deep-dive docs

---

This is part of the **Microsoft Discrete Manufacturing Agentic Center of Excellence**.
