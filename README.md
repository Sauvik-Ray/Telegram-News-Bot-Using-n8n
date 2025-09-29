# 📰 News Agent with n8n + Telegram

This project is an **n8n workflow** that fetches the latest news from [NewsAPI](https://newsapi.org/) every morning at 9 AM and sends the top 3 headlines to your **Telegram bot**.

You can easily customize the topic (e.g., *technology*, *sports*, *politics*) and number of articles.

---

## 🚀 Features

* Scheduled daily news updates (default: 9 AM).
* Pulls fresh articles using [NewsAPI.org](https://newsapi.org).
* Formats headlines, descriptions, and links.
* Sends the results to your **Telegram bot**.
* Fully customizable (topics, time, channels).

---

## 🛠️ Prerequisites

1. [Install n8n](https://docs.n8n.io/hosting/installation/).
2. [Sign up for NewsAPI](https://newsapi.org/) and get a free API key.
3. [Create a Telegram Bot](https://core.telegram.org/bots#creating-a-new-bot) using **@BotFather** and get your bot token.
4. Get your **Telegram Chat ID** (use [@userinfobot](https://t.me/userinfobot)).

---

## ⚙️ Setup Instructions

1. Import the `workflow.json` file into your n8n instance.
2. Open the workflow in the n8n editor.
3. Update the following fields:

   * In the **HTTP Request** node → Replace `"Your Api Key"` with your NewsAPI key.
   * In the **Telegram Send Message** node → Replace `"Your Chat Id"` with your Telegram chat ID.
   * Ensure your **Telegram credentials** are set up under n8n → Settings → Credentials.
4. (Optional) Update the topic in the **Edit Fields** node:

   ```json
   { "topic": "technology" }
   ```

   Example: change to `"sports"`, `"finance"`, etc.
5. Activate the workflow.

---

## 📂 Project Structure

* `workflow.json` → n8n workflow definition.
* `README.md` → This guide.

---

## 🔄 Workflow Overview

1. **Schedule Trigger** – Runs daily at 9 AM.
2. **Edit Fields** – Defines the topic (default: technology).
3. **HTTP Request** – Calls NewsAPI with the chosen topic.
4. **Code (JavaScript)** – Formats the top 3 articles into a clean Telegram message.
5. **Telegram Node** – Sends the message to your Telegram bot.

---

## 📸 Example Telegram Output

```
📰 Latest News

1. *AI Breakthrough in 2025*
Researchers reveal...

🔗 https://example.com/news1

2. *Tech Giants Merge*
The merger between...

🔗 https://example.com/news2

3. *New Smartphone Launched*
Features include...

🔗 https://example.com/news3
---

## 📜 License

MIT License. Free to use and modify.
