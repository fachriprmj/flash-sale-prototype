[README.md](https://github.com/user-attachments/files/29943110/README.md)
# Flash Sale Management System — Clickable Prototype

A self-contained HTML/CSS/JS prototype built from a Product Requirements Document (PRD) for a self-service Flash Sale management tool, designed to let a Marketing team create, configure, and publish flash sale campaigns without help from Engineering.

**Live demo:**((https://fachriprmj.github.io/flash-sale-prototype/))

## What this covers

The prototype walks through the core end-to-end flow defined in the PRD:

- **Dashboard** — list of flash sale campaigns with status (Draft / Published / Active) and SKU count.
- **Create flash sale** — campaign name, schedule (start/end time), and a product table with live promo price calculation.
- **Add product modal** — search by SKU or name, a hard limit of 6 SKUs per campaign, and stock-aware selection (out-of-stock products can't be added).
- **Stock and quantity validation** — each product shows available stock; quantity is validated against it, and Publish is disabled until every rule passes.
- **Homepage preview** — how the active flash sale and upcoming schedule would appear to customers.

## Business rules implemented

- Maximum 6 SKUs per flash sale.
- Start time must be earlier than end time.
- Quantity must be greater than 0 and cannot exceed available stock.
- A campaign cannot be published unless it has a name, valid schedule, and at least one product with valid quantity.

## Tech

Plain HTML, CSS, and vanilla JavaScript — no build step, no dependencies beyond the [Tabler Icons](https://tabler.io/icons) webfont loaded from a CDN. Everything runs client-side; there's no backend, so state resets on page reload.

## Running it locally

Just open `index.html` in any modern browser. No installation needed.

## Deploying

**GitHub Pages**
1. Push this repo to GitHub.
2. Go to `Settings > Pages`, set the source branch to `main` and folder to `/root`.
3. Your prototype will be live at `https://<username>.github.io/<repo-name>/`.

**Netlify Drop**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag the folder containing `index.html` onto the page.
3. Netlify gives you an instant public URL.

## Context

This prototype was built as part of a product management case study exercise, based on a full PRD covering user stories, functional requirements, business rules, edge cases, and non-functional requirements for a Flash Sale management system.


Author: Fachri Pramuja
