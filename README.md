# Expense Tracker

Expense Tracker is a private, browser-based personal finance dashboard for recording spending, monitoring a monthly budget, and understanding category totals.

## Features

- Dashboard summary for monthly spending, remaining budget, and transaction count
- Add expenses with merchant, amount, date, category, and note
- Validation and success feedback
- Search and category filtering
- Delete transactions
- Category breakdown and budget progress visualizations
- Settings screen for changing the budget or clearing local data
- Responsive desktop and mobile layout
- Persistence with browser `localStorage`

## Technology

- React 19
- TypeScript
- Vite
- Lucide React
- Custom CSS
- Vercel deployment

## Run Locally

```bash
npm install
npm run dev
```

Open the local URL printed by Vite. The production build can be checked with:

```bash
npm run build
npm run preview
```

## Project Files

- `PLAN.md` contains the reviewed development and deployment plan.
- `src/App.tsx` contains the dashboard state, calculations, form validation, and views.
- `src/App.css` contains the responsive visual system.

## Data and Privacy

Expenses and the monthly budget are stored only in the current browser using `localStorage`. There is no account, server, or external database in this release. Clearing browser storage removes the saved data.

## Deployment

This is a static Vite application and can be deployed by importing the GitHub repository into Vercel. Use `npm run build` as the build command and `dist` as the output directory.

GitHub Repository: https://github.com/NikhilGITHUB1/https-github.com-NikhilGITHUB1-https-github.com-my-expense-tracker

Live Application: https://expense-tracker-rose-mu-53.vercel.app

## Verification

- `npm run build` passes TypeScript compilation and Vite bundling.
- `npm run lint` passes ESLint.
- The add-expense workflow was verified in the local browser, including validation feedback and a successful transaction notice.