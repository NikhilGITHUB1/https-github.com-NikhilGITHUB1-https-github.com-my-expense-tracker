# Expense Tracker Plan

## Application Name
Expense Tracker

## Problem Statement
People need a simple way to record everyday spending, understand where their money goes, and quickly spot whether they are staying within a monthly budget. The app should make this useful without requiring an account or a backend.

## Target Users
- Individuals tracking personal and household expenses
- Students and first-time budgeters who want a low-friction tool
- Anyone who wants a private, browser-only expense log

## Main Features
- Dashboard with total spending, current-month spending, transaction count, and remaining budget
- Add an expense with amount, category, date, merchant, and optional note
- Client-side validation with clear success and error feedback
- Expense list with category, merchant, date, amount, and delete action
- Search and category filtering
- Monthly budget setting with progress indicator
- Spending breakdown by category
- Persistent data using browser `localStorage`
- Responsive layout for mobile and desktop
- Empty, loading-safe, and no-results states

## Pages / Screens
The application will be a focused single-page dashboard with these functional areas:

1. **Overview**: summary metrics, budget progress, and category breakdown
2. **Add Expense**: validated expense entry form
3. **Transactions**: searchable and filterable expense history
4. **Settings**: monthly budget control and data reset action

## Technology Stack
- Vite
- React
- TypeScript
- CSS with custom responsive design tokens
- Browser `localStorage` for persistence
- Lucide React for interface icons
- Vercel for public deployment

## Project Folder Structure
```text
expense-tracker/
├── public/
├── src/
│   ├── components/
│   │   ├── AddExpenseForm.tsx
│   │   ├── BudgetCard.tsx
│   │   ├── CategoryBreakdown.tsx
│   │   ├── ExpenseList.tsx
│   │   ├── Header.tsx
│   │   └── SummaryCards.tsx
│   ├── data/
│   │   └── categories.ts
│   ├── hooks/
│   │   └── useLocalStorage.ts
│   ├── types/
│   │   └── expense.ts
│   ├── App.tsx
│   ├── App.css
│   ├── index.css
│   └── main.tsx
├── .gitignore
├── index.html
├── package.json
├── PLAN.md
├── README.md
├── tsconfig.json
└── vite.config.ts
```

## Data To Store

### Expense
- `id`: unique string
- `merchant`: string
- `amount`: positive number
- `category`: one of the supported categories
- `date`: ISO date string (`YYYY-MM-DD`)
- `note`: optional string
- `createdAt`: ISO timestamp

### Settings
- `monthlyBudget`: positive number

The expense collection will be stored under `expense-tracker-expenses`, and settings under `expense-tracker-settings` in `localStorage`.

## Development Steps
1. Scaffold the Vite React TypeScript project.
2. Install the icon dependency and establish application types and category data.
3. Build the single-page dashboard layout and responsive visual system.
4. Implement local persistence for expenses and budget settings.
5. Implement expense creation, validation, feedback, and deletion.
6. Add search, category filtering, monthly totals, budget progress, and category aggregation.
7. Add reset-data safeguards and empty/no-results states.
8. Write README documentation and verify the production build.
9. Run the app locally and test the primary workflows in a browser.
10. Push the complete project to GitHub and connect the repository to Vercel.
11. Verify the public deployment after refresh and document the URLs.

## Deployment Approach
- Store source code in a GitHub repository named `expense-tracker`.
- Import the repository into Vercel.
- Use the default Vite build settings: `npm run build` with output directory `dist`.
- No environment variables or server database are required.
- The app is intentionally client-only; each browser keeps its own expense data.

## Verification Checklist
- `npm run build` completes successfully.
- The app starts with `npm run dev`.
- Adding a valid expense updates the dashboard and list.
- Invalid or incomplete form input is rejected with visible messages.
- Search and category filtering return the expected records.
- Deleting an expense updates totals and category breakdown.
- Budget changes update the progress state.
- Data remains after a page refresh.
- The production URL loads and supports the same core workflows.

## Plan Review
This plan covers the required application scope, user needs, screens, stored data, development flow, local verification, GitHub handoff, and Vercel deployment. The client-only architecture is appropriate for a small personal tracker and avoids introducing authentication or backend infrastructure that the assignment does not require. A future version could add accounts, shared budgets, CSV export, and a server database, but those are intentionally outside the first release.
