# SpendWise ◈

> **Track Every Rupee. Own Your Finances.**

SpendWise is a lightweight, modern personal expense tracking web application built with Python, Flask, SQLite, and vanilla CSS/JS. It helps individuals log transactions in seconds, monitor spending habits, and visualize monthly category breakdowns without spreadsheet headaches.

---

## ✨ Features

- **⚡ Fast Expense Logging**: Record transactions instantly with amount, category, date, and description.
- **📊 Interactive Dashboard**: View monthly spending totals, remaining budget, and transaction counts at a glance.
- **📅 Flexible Date Range Filtering**: Filter spending history across multiple presets (All Time, Last Month, Last 3 Months, Last 6 Months) or custom ranges.
- **🏷️ Category Breakdown**: Clear visual breakdown across categories (Food, Transport, Bills, Health, Entertainment, Shopping, Other).
- **✏️ Complete Expense Management**: Easily edit existing entries or delete them with an intuitive confirmation prompt.
- **🔐 User Authentication**: Secure registration and login featuring password hashing (`scrypt` via Werkzeug) and session protection.
- **🎨 Modern Fintech Aesthetic**: Polished, responsive UI crafted with custom CSS variables, smooth transitions, and typography using DM Serif Display & DM Sans.

---

## 🛠️ Tech Stack

- **Backend**: Python 3.10+, Flask
- **Database**: SQLite3 (automatic schema migration & seeding, foreign key enforcement)
- **Frontend**: Server-rendered Jinja2 templates, Vanilla CSS, Vanilla JavaScript
- **Testing**: `pytest`, `pytest-flask`

---

## 📁 Project Structure

```text
SpendWise/
├── app.py                  # Main Flask application and route definitions
├── database/
│   ├── __init__.py
│   ├── db.py               # SQLite connection helpers, init_db(), seed_db()
│   └── queries.py          # Parameterized SQL query helpers (CRUD, stats, filters)
├── templates/
│   ├── base.html           # Master layout with navbar, footer, flash alerts
│   ├── landing.html        # Marketing hero page with interactive demo modal
│   ├── login.html          # User authentication sign-in
│   ├── register.html       # New user account registration
│   ├── profile.html        # Main dashboard and filtered transaction history
│   ├── add_expense.html    # Transaction entry form
│   ├── edit_expense.html   # Transaction modification form
│   ├── analytics.html      # Spending analytics preview
│   ├── privacy.html        # Privacy policy
│   └── terms.html          # Terms and conditions
├── static/
│   ├── css/
│   │   ├── style.css       # Global design tokens and layout styling
│   │   ├── landing.css     # Landing page styles
│   │   ├── profile.css     # Dashboard & transaction table styles
│   │   ├── add_expense.css # Form styles
│   │   └── analytics.css   # Analytics preview styles
│   └── js/
│       └── main.js         # Client-side interactions
├── tests/
│   ├── test_06_date_filter_profile.py
│   ├── test_07-add-expense.py
│   └── test_delete_expense.py
├── requirements.txt        # Project dependencies
├── pytest.ini              # Test runner configuration
└── README.md
```

---

## 🚀 Getting Started

### 1. Prerequisites
- Python 3.10 or higher
- Git

### 2. Clone the Repository
```bash
git clone https://github.com/Ankitkumar1141/SpendWise.git
cd SpendWise
```

### 3. Create and Activate a Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

### 5. Run the Application
```bash
python app.py
```
Open your browser and navigate to:
```text
http://127.0.0.1:5001
```

> **Note**: On first startup, SpendWise automatically initializes `spendwise.db` and seeds sample expenses for the default user account.

### Default Login
- **Email**: `am0287883@gmail.com`
- **Password**: `demo123`

*(You can also click **Get Started** to create your own account at `/register`)*

---

## 🧪 Running Tests

To run the automated test suite:
```bash
pytest
```

To run a specific test file:
```bash
pytest tests/test_delete_expense.py
```

---

## 👤 Author

- **Ankit Kumar**
- Email: [am0287883@gmail.com](mailto:am0287883@gmail.com)
- GitHub: [@Ankitkumar1141](https://github.com/Ankitkumar1141)

---

## 📄 License

This project is licensed under the MIT License - feel free to use and modify for personal or commercial projects.
