# Warehouse Control Tower

A single-page control tower for port-side warehouse operations: inbound containers and trucks, outbound orders, forwarding files, demurrage and detention, value-added services and SOPs, with role-based access.

Live demo: https://nvo-warehouse.vercel.app

## Demo access

| Role | What it sees | Password |
|---|---|---|
| Administrator | Everything, including edit rights | `admin123` |
| Warehouse Operator | Two warehouses, CT Entry, Warehouse Units, SOP | `admin123` |
| Sales Representative | Dashboards, VMF, Sales Dem/Det, SOP | `admin123` |
| Customer: Summit Polymers | Own shipments and invoices only | `admin123` |
| Customer: Cerix | Own shipments and invoices only | `admin123` |
| General Viewer | Dashboards, read only | `admin123` |

## How it runs

The app is pure frontend (`index.html` plus `va.html` for the Warehouse Unit pages). A built-in mock API intercepts all `/api` calls, so no server or database is needed.

All data is fictional. It is generated deterministically from 5 January 2026 up to the current date, plus three weeks of announced arrivals, so the demo always looks current. Records keep their identity between visits and only move forward through their lifecycle as days pass.

Edits made in the app (CT Entry sheet, Warehouse Unit orders, SOP steps) are saved in the browser's localStorage. Use **Reset demo data** in the sidebar footer to start over.

## Run locally

Serve the folder with any static server, for example:

```
npx serve .
```

Opening `index.html` directly from disk also works, but the Warehouse Unit pages need a server so `/va` resolves to `va.html`.

## Deploy

The repository is connected to Vercel. Every push to `main` deploys to production. `vercel.json` enables clean URLs and routes unknown paths to `index.html`.

A user handbook (PDF) describing every screen is distributed separately.
