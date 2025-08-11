# XpenseWise — CLI Expense Tracker

XpenseWise is a lightweight, command‑line expense tracker written in Python. It lets you quickly log expenses, categorizes them, and shows a monthly budget summary — all in a single CSV file.

---

## ✨ Features

- **Quick entry**: Add an expense (name, amount, category) via prompts.
- **Smart categories**: 🍔 Food, 🏠 Home, 💼 Work, 🎉 Fun, 🤷 Misc.
- **CSV storage**: Appends entries to `expenses.csv` for easy portability.
- **Auto‑summary**: Totals spending, breaks down by category, and shows:
  - Remaining budget
  - Days left in the current month
  - Suggested **budget per day** to stay on track

---

## 🚀 Quickstart

> Requires **Python 3.10+**. No external libraries needed.

1) **Clone** this repo
```bash
git clone https://github.com/<your-username>/XpenseWise.git
cd XpenseWise
```

2) **Run** the tracker
```bash
python Xpense_track.py
```

By default, the app:
- Writes to: `expenses.csv`
- Uses a monthly **budget of 5000** (you can change this in `Xpense_track.py`)

---

## 🧑‍💻 Usage (example run)

```
Welcome to XpenseWise!
🎯 Running Expense Tracker
🎯 Getting User Expense
Enter name of expense: Burger
Enter amount spent on expense: 8.50
Select a category: 
1.🍔 Food
2.🏠 Home
3.💼 Work
4.🎉 Fun
5.🤷 Misc
Enter a Category number [1 - 5]: 1
🎯 Saving User Expense: <Expense: Burger, 🍔 Food, $8.50> to expenses.csv
🎯 Summarizing User Expense
Expenses by Category 📈:
   🍔 Food:  $28.50
   💼 Work:  $145.00
💰 Total Spent: $173.50
✅ Budget remaining: $4826.50
Remaining days in this month: 11
👉 Budget Per Day: $438.77
```

---

## 🗂️ Data format

Expenses are stored (appended) to `expenses.csv` with this schema:

```
name,category,amount
Burger,🍔 Food,8.5
Gas,💼 Work,70
NEPA,🏠 Home,59
```

You can open this CSV in Excel/Sheets for filtering and charts.

---

## 🛠️ Project Structure

```
XpenseWise/
├─ Xpense_track.py        # Main CLI app (entry point)
├─ expense.py             # Expense class (name, category, amount)
├─ expenses.csv           # Your data (created/updated at runtime)
└─ README.md              # This guide
```

---

## ⚙️ Configuration

Open `Xpense_track.py` to customize:
- `expense_file_path` — default `"expenses.csv"` (line near the top)
- `budget` — default `5000`

You can also pre-create an empty CSV with headers if desired:
```csv
name,category,amount
```

---

## 🧭 Roadmap 

- Validate numeric input and category selection more robustly
- Monthly rollovers / multi-file support (one CSV per month)
- Optional JSON/SQLite storage
- Export summary to Markdown or PDF
- Simple TUI (text UI) for keyboard-only navigation

---

## 📝 License

This project is licensed under the **MIT License**. See `LICENSE` for details.
```
