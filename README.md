# Expense Assistant

A personal finance management and tracking application. This project helps users manage their income, expenses, set financial goals, and provides AI-powered budget suggestions and stock analysis.

## Features

- **Dashboard:** Overview of income and expenses.
- **Expense Tracking:** Add, view, and analyze daily/monthly expenses.
- **AI Budget Suggestions:** Get AI-driven recommendations to manage your budget better.
- **Goal Setting:** Plan savings and set smart financial goals.
- **Deep Learning Predictions:** Predict future expenses based on past data.
- **Chatbot:** Interact with an AI assistant for financial queries.
- **Admin Panel:** Manage users, datasets, and monitor system performance.

## Technology Stack

- **Backend:** C# / ASP.NET Web Forms
- **Database:** Local Database / CSV
- **AI/ML:** Integration via OpenRouter API (requires setting the `OPENROUTER_API_KEY` in `Web.config`)

## Setup

1. Clone the repository.
2. Open the project in Visual Studio.
3. In `FinanceAssistant/Web.config`, set your `OPENROUTER_API_KEY` to enable AI features.
4. Run the project on a local IIS server.
