# proceptdocs

Documentation for [procept.tech](https://procept.tech) — the website of **Procept Technologies Corp.**, a Delaware corporation backed by Georgia Tech.

## Mission

> Driving the world's transition to AGI. We make frontier intelligence effortless to deploy and transform breakthrough research into industry value.

## Products

### 1. AI-Powered Supply Chain Platform (the "Aegis" agent suite)

Positioned as *"The Holistic Action Center for your AI-Powered Supply Chain"* — an autonomous procurement/operations agent that attaches directly to ERPs, 3PL platforms, and unstructured email. It isolates errors and formats structured resolution tasks for single-click human approval, with every action audited against agent rules and the ERP log.

Agent workspace queues:
- **Forecasting** — burn-rate detection, stockout prediction, expedited air-freight PO generation
- **Order errors** — e.g. "phantom lead times" (SAP says 30 days, vendor actually takes 45), invoice/PO discrepancies
- **Vendor onboarding** — extracts W-9s and banking details from messy emails and stages them into the ERP master record

Key capabilities:
- **Invoice dispute automation** — catches a $12.50 invoice vs a $10.00 PO, blocks AP processing, drafts a structured dispute to the vendor
- **Shortage claims** — intercepts warehouse shortage logs, cross-references the original PO, drafts credit-claim packets and blocks vendor invoices
- **3PL cross-checking** — holds fulfillment on cuts/cancels/address mismatches until the warehouse explicitly acknowledges
- **Tariff calculation & reconciliation** — replaces manual tariff-to-PO/SKU matching
- **Live vendor scorecards** — replaces manual vetting with real-time supplier analytics
- **Vendor SMS notifications, accounting & invoice automation**
- Full Spanish localization of the supply-chain content

Case study referenced on-site: **"TraxTech — Why AI Fails in Supply Chain"** (also published in Spanish).

### 2. Frontier Intelligence Platform

A fully maintained, self-hosted AI stack, deployed in days and owned by the customer:

- **Self-Hosted Stack** — open-weight models implemented in your environment; you own the weights, Procept handles the engineering. Includes small language models (SLMs) "compressed to the task."
- **RSI Harness** — the recursive self-improvement loop, end to end: data, training, inference, evaluation. Models train on your workflows, not generic benchmarks.
- **GPU Abstraction** — cheapest GPUs brokered in real time; dedicated inference, "no GPU surfing."
- **Flat Pricing** — one plan, one flat linear rate; no per-token billing. "Business outcomes, not vanity benchmarks."

## Site structure

Single-page React app (Vite build) with these routes:

| Route | Page |
| --- | --- |
| `/` | Home (hero video, product sections, pricing, case study) |
| `/agent-suite` | Supply chain agent suite |
| `/plans` | Pricing |
| `/demo` | "Aegis Demo Request" form |
| `/daily-brief` | Intelligence report |
| `/agent-files`, `/history`, `/settings` | Agent workspace |
| `/queues/forecasting`, `/queues/order-errors`, `/queues/vendor-onboarding` | Agent queues |
| `/privacy`, `/terms-of-service`, `/data-processing-addendum` | Legal |

## Tech stack (as deployed)

- React SPA bundled with Vite; React Router; Framer Motion; Recharts; markdown rendering
- English/Spanish localization
- Fonts: Instrument Sans, Instrument Serif, JetBrains Mono
- Dark theme (`#050505`), video hero background
- SEO meta: `og:title`, `og:description`, `og:image`, apple-touch-icon, SVG favicon

## Contact & legal

- Email: `hello@procept.tech` · `accounting@procept.tech`
- LinkedIn: [linkedin.com/company/procept-tech](https://www.linkedin.com/company/procept-tech/)
- Legal entity: Procept Technologies Corp. (Delaware), © 2026
