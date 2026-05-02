# Smart Spending with AI - Finance Assistant

A comprehensive, next-generation personal finance management web application built with ASP.NET. This platform goes beyond basic tracking by integrating rule-based financial algorithms, a custom-built Machine Learning engine, and LLM-powered chatbot assistance to provide intelligent financial insights.

## 🌟 Key Features

### User Features
* **Financial Dashboards:** Intuitive overview of total income, expenses, and current budget constraints.
* **Income & Expense Tracking:** Record daily transactions with categorized labels (Food, Rent, Transport, Entertainment, Emergency).
* **AI Budget Suggestions:** Get algorithmic budget breakdowns (e.g., 50/30/20 rule variations) based on your exact income, along with trend-based predictions for future months.
* **Smart Financial Advisor (Chatbot):** An integrated chatbot powered by **Llama-3-8b-instruct** (via OpenRouter API) that offers personalized financial advice, answers money management questions, and analyzes user queries.
* **Savings Planner & Smart Goals:** Set long term financial goals and track your progress.
* **Stock & Investment Analysis:** Dedicated modules to plan stock investments.
* **Reporting:** Visual representations and monthly breakdowns of spending habits.

### Admin & Data Science Features
* **Admin Dashboard:** Monitor total user base, total platform-wide income, expenses, and budgets.
* **User Management:** View, manage, and monitor all registered users and their transaction records.
* **Machine Learning Pipeline:** A complete, custom-built ML pipeline directly inside the admin panel:
  * **Dataset Upload:** Upload raw financial CSV datasets.
  * **Data Preprocessing & Label Encoding:** Clean data and encode categorical labels.
  * **Feature Selection:** Select independent variables and target columns for training.
  * **Custom Model Training:** The system trains a **Logistic Regression** model entirely from scratch using Gradient Descent algorithms implemented in pure C#, without relying on external Python libraries.
  * **Evaluation:** Test the model and view accuracy/probability metrics directly in the browser.

## 🛠️ Technology Stack

* **Frontend:** HTML5, CSS3, JavaScript, Bootstrap 5.3
* **Backend:** C#, ASP.NET Web Forms (.NET Framework 4.8.1)
* **Database:** SQL Server (LocalDB/Express) using ADO.NET (`SmartFinance` Database)
* **AI Integration:** OpenRouter API (LLM Integration via HttpClient)
* **Machine Learning:** Custom C# implementations for Gradient Descent & Logistic Regression.
* **Icons & Fonts:** Bootstrap Icons, Google Fonts (Poppins)

## 🚀 Setup & Installation

### Prerequisites
1. Visual Studio 2019 or later (with ASP.NET and web development workloads).
2. SQL Server or SQL Server Express.

### Steps to Run
1. **Clone the repository:**
   ```bash
   git clone https://github.com/aditya-sebi/Expense-Assistant.git
   ```
2. **Database Setup:** 
   Ensure you have a SQL Server instance running locally. The project expects a database named `SmartFinance` (ConnectionString: `Data Source=.;Initial Catalog=SmartFinance;Integrated Security=True`). Run the necessary SQL scripts to create tables (`QA_Bot`, users, expenses, etc.) if provided.
3. **API Configuration:**
   Open `FinanceAssistant/Web.config` and insert your OpenRouter API key to enable the AI Chatbot features:
   ```xml
   <appSettings>
       <add key="OPENROUTER_API_KEY" value="YOUR_API_KEY_HERE" />
   </appSettings>
   ```
4. **Run the Project:**
   Open the solution/website directory in Visual Studio and run the application (IIS Express). The entry point is `HomePage.aspx`.

## 🔒 Security Note
Do **not** commit your real `OPENROUTER_API_KEY` to public repositories. Always use environment variables or keep it private.

---
*Developed as a Final Year Project by Aditya Sebi.*
