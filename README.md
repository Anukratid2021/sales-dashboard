# Sales Dashboard (Next.js 15 + TypeScript + Tailwind + Recharts)

A simple atomic-structured dashboard that visualizes mock Kaggle-like sales for **2022, 2023, 2024** with **bar, line, and pie** charts using **Recharts**. Includes:

- Next.js 15 + App Router + TypeScript
- Tailwind CSS
- Atomic component structure (atoms, molecules, organisms)
- Mock data (monthly sales) and a mock **/api/sales** endpoint
- **Chart switcher** (Bar / Line / Pie)
- **Custom threshold filter** (min sales)
- **Empty dashboard page** where components are added
- Clear README with setup steps

---

## Project Structure

```
app/
  dashboard/
    page.tsx           # Dashboard page (empty page that composes components)
  api/sales/route.ts   # Mock API endpoint returning the same mock data
  layout.tsx
  page.tsx
components/
  atoms/FilterInput.tsx
  molecules/ChartSwitcher.tsx
  organisms/SalesChart.tsx
  ui/Card.tsx
data/
  salesData.ts         # Kaggle-like mock monthly sales for 2022–2024
lib/
  types.ts
tailwind.config.ts
postcss.config.js
tsconfig.json
next.config.mjs
```

---

## Setup & Run

```bash
# 1) Install
npm install

# 2) Dev
npm run dev
# Visit http://localhost:3000

# 3) Build & Start
npm run build
npm start
```

> **Note:** The project references `next@15`. If the exact 15.0.0 tag is not yet published on your machine, you can switch to the latest available Next.js version temporarily:
>
> ```bash
> npm i next@latest
> ```

---

## What I Implemented

- Atomic structure: small **atoms** (FilterInput), **molecules** (ChartSwitcher), **organisms** (SalesChart), composed inside the **dashboard page**.
- **Multiple chart types** using Recharts with a neat switcher.
- **Threshold filter** to hide/show months below a sales value.
- **Mock API** (`/api/sales`) that returns the same mock dataset for easy future integration.
- Tailwind styling with a clean, minimal aesthetic.
- TypeScript everywhere for safety.
- Accessible labels and keyboard-friendly controls.

---

## Enhancements (Suggested)

- Wire `/api/sales` to a real backend or third-party API.
- Add a date range picker or per-quarter toggle.
- Add CSV import (drag-and-drop) to load external Kaggle files.
- Add unit tests (React Testing Library + Vitest).

---

## Deploy

- Create a new **GitHub** repo and push the project:
  ```bash
  git init
  git add .
  git commit -m "feat: initial sales dashboard"
  git branch -M main
  git remote add origin https://github.com/<your-username>/<repo-name>.git
  git push -u origin main
  ```
- Deploy on Vercel with one click; it autodetects Next.js.
