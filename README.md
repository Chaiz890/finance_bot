# 💸 FinanceBOT — Personal Finance Assistant

**FinanceBOT** is a cross-platform personal finance tracking tool with Google Sheets integration, a web interface (Streamlit), a Telegram bot, and a REST API (FastAPI). Simple, transparent, and accessible from anywhere.

---

## 🚀 Features

- 📲 **Telegram Bot**: Quickly log expenses and income from your phone.
- 🌐 **Web Interface** (Streamlit): Manual entry and report viewing via browser.
- 🔌 **REST API** (FastAPI): Integrate with external systems or automate workflows.
- 📊 **Weekly Reports**: Category-based summaries.
- ☁️ **Google Sheets storage**: Transparent and convenient data storage.

---

## 🛠️ Tech Stack

- Python
- FastAPI
- Streamlit
- Telegram Bot API (`python-telegram-bot`)
- Google Sheets API (`gspread`, `oauth2client`)

---

## 📦 Installation

1. Clone the repository:

```bash
git clone https://github.com/your_username/financebot.git
cd financebot
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Add your `credentials.json` (Google Service Account key) to the project root.

4. (For the Telegram bot) Create a `.env` file with your bot token:

```env
TELEGRAM_TOKEN=your_bot_token
```

---

## 🔧 Usage

### 📱 Telegram Bot

Start the bot with:

```bash
python telegram_bot.py
```

Supported message format:

- `food 500`
- `income job 30000`
- `/report` — weekly report

---

### 🌐 Web Interface (Streamlit)

```bash
streamlit run interface.py
```

Use this to manually log entries and view reports in the browser.

---

### 🧩 API Server (FastAPI)

```bash
uvicorn main:app --reload
```

Example POST request to log a transaction:

```http
POST /add
Content-Type: application/json

{
  "category": "Cafe",
  "amount": 750,
  "type": "Expense",
  "comment": "Lunch with coworkers"
}
```

---

## 📌 Google Sheets Structure Example

| Date       | Category | Amount | Type    | Comment         |
|------------|----------|--------|---------|-----------------|
| 21.06.2025 | Food     | 500    | Expense | telegram        |
| 21.06.2025 | Salary   | 30000  | Income  | job             |

---

## 📅 Roadmap

- Multi-currency support
- Visual dashboards and charts
- Advanced report filtering
- Default categories and templates

---

## 📄 License

MIT License
