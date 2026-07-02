# AX Lens — Finance Dashboard

Live finance dashboard for Alpha X group entities (SG · MY · CN), built on consolidated P&L, cash flow, receivables, and payables data.

🔗 **Live dashboard:** https://axfinance.github.io/AXLENS/

---

## What it shows

| Section | Metrics |
|---|---|
| **Cash Flow** | Bank balance by entity, actual vs. forecast inflow/outflow, projected balance |
| **Receivables** | Collection rate, overdue %, due invoices by project code, future inflow forecast |
| **Payables** | Outstanding AP, overdue %, payable ranking by category |
| **Profit & Loss** | Revenue, COGS, expenses by group, gross & net margin, PO value |

All sections filterable by **Entity** (SG / MY / CN) and **Period** (Month / Quarter / Year).

---

## How to update the data

1. Update `Finance_Data_Conso_Dashboard.xlsx` with the latest figures
2. Go to this repository → **Add file → Upload files**
3. Upload the new Excel file (it will replace the old one)
4. Click **Commit changes**

The dashboard fetches the file live from GitHub — anyone who opens the link after the upload will see the updated numbers automatically. No rebuild needed.

---

## Files in this repo

| File | Purpose |
|---|---|
| `index.html` | The live dashboard (do not edit manually) |
| `Finance_Data_Conso_Dashboard.xlsx` | Source data — update this to refresh the dashboard |
| `Finance Data_Conso.xlsx` | Legacy consolidated file (reference only) |

---

## Source data structure

The dashboard reads from these sheets inside `Finance_Data_Conso_Dashboard.xlsx`:

- **Bank** — monthly bank balances by entity and account
- **AR** — invoice-level receivables (Status, Due Date, Expected Inflow, Payment Date, Amount USD)
- **CF** — cash flow transactions (Status, Entity, Billing/Due/Payment Date, Currency, Amount USD, Category, Group)
- **PO** — purchase order values

---

*Built and maintained by Alpha X Finance team. For issues or updates contact cathfrine_low@alphaxtec.com*
