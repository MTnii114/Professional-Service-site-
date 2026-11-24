# Nexora Labs — Independent AI & Digital Innovation Studio

A production-ready full-stack web platform combining a futuristic dark-obsidian React + TypeScript application (**Project A Frontend + Cloudflare Pages Functions Gateway**) with a complete Google Workspace serverless backend (**Project B Google Apps Script + Google Sheets + Google Drive**).

---

## Platform Highlights

- **Brand Identity:** **Nexora Labs** — *Independent AI & Digital Innovation Studio*
- **Design System:** Red (`#FF315A` / `#C91E49`), Electric Blue (`#287BFF` / `#50B7FF`), and Violet (`#8157FF`) accents on deep obsidian surfaces (`#080A16`, `#101426`, `#171B32`), paired with **Space Grotesk** and **Inter** typography.
- **Public Studio Experience:** Home, About, Services (AI Website Building, AI-Powered Creative Solutions, AI Automation Workflows, AI Model Development & Training, AI Optimization & Fine-Tuning, Website Optimization & Deployment), Portfolio & Case Studies, Transparent BDT/USD Pricing Estimator, FAQ, Legal Pages, and Contact.
- **Authentication Flows:** Split-screen Sign In, Client Registration, 6-digit Email OTP Verification, Forgot Password, and Reset Password.
- **Client Portal (`/dashboard`):** Project milestone & progress tracker, authorized Drive deliverables access, inquiry history & replies, estimate quotes, notifications, and profile settings.
- **Super Admin Console (`/admin`):** Studio KPI overview, Services & Portfolio CRUD, Client management & suspension, Project & Milestone management, Inquiry/Estimate quoting, CMS & Studio-wide Theme switcher (`blue` / `red` / `purple`), Drive Media Upload, and paginated Audit Logs.

---

## Project Structure

```text
/public/                    # Preserved Nexora Labs favicon suite & site.webmanifest
/src/                       # React + TypeScript + Tailwind CSS v4 frontend
  /components/              # Brand logo, UI primitives, motion wrappers, layouts
  /context/                 # Platform state & live API integration context
  /pages/                   # Public, Auth, Client Portal, and Super Admin routes
  /services/                # Frontend API adapters (/api/*)
/functions/                 # Cloudflare Pages Functions Edge API Gateway
  _lib/                     # CORS, KV rate limiter, validation, auth middleware
  api/[[path]].ts           # Catch-all /api/* proxy to Google Apps Script
  README.md                 # Gateway environment & deployment reference
/backend-kit/               # Complete Google Apps Script & documentation suite
  /apps-script/             # All 12 modular .gs backend files + README_SETUP.md
  /docs/                    # Schema, Drive policy, Security, API & Deployment guides
```

---

## Quick Start (Local Frontend Development)

```bash
npm install
npm run dev
```

Runs on `http://localhost:3000`. Configure environment variables using `.env.example` as reference:

- `VITE_BACKEND_CONNECTED=false` *(set `true` when connected to Cloudflare Pages Functions)*
- `VITE_API_BASE_URL=/api`

---

## Production Backend & Deployment Documentation

- **Cloudflare Pages Functions Gateway:** [`/functions/README.md`](./functions/README.md)
- **Apps Script Setup (12 `.gs` Modules):** [`/backend-kit/apps-script/README_SETUP.md`](./backend-kit/apps-script/README_SETUP.md)
- **End-to-End Deployment Guide:** [`/backend-kit/docs/DEPLOYMENT_GUIDE.md`](./backend-kit/docs/DEPLOYMENT_GUIDE.md)
- **API Reference:** [`/backend-kit/docs/API_DOCUMENTATION.md`](./backend-kit/docs/API_DOCUMENTATION.md)
- **24-Tab Google Sheets Schema:** [`/backend-kit/docs/GOOGLE_SHEETS_SCHEMA.md`](./backend-kit/docs/GOOGLE_SHEETS_SCHEMA.md)
- **Google Drive Access Policy:** [`/backend-kit/docs/GOOGLE_DRIVE_SETUP.md`](./backend-kit/docs/GOOGLE_DRIVE_SETUP.md)
- **Security Architecture & Notes:** [`/backend-kit/docs/SECURITY_NOTES.md`](./backend-kit/docs/SECURITY_NOTES.md)
