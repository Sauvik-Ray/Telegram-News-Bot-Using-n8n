# 📰 Daily News Bot with n8n + Telegram

This project is an **automated news delivery workflow** built using [n8n](https://n8n.io/).
It fetches the latest headlines from [NewsAPI](https://newsapi.org/) and sends a formatted daily digest to a Telegram bot.

---

## ✨ Features

* 📅 Automated daily scheduling with **Cron**
* 📰 Fetches headlines from **NewsAPI**
* 🖊️ Formats results into clean Markdown with article titles, summaries, and links
* 📲 Sends news directly to **Telegram chat**
* ⚡ Easy to customize for different categories or number of articles

---

## 🛠️ Workflow Overview

1. **Cron Node** – triggers workflow daily at a set time
2. **HTTP Request Node** – fetches news from NewsAPI
3. **Code Node** – formats top 3 articles into a Markdown message
4. **Telegram Node (Send Message)** – delivers news digest to Telegram bot

---

## 🚀 Setup Instructions

### 1. Prerequisites

* An [n8n](https://n8n.io/) instance (local, cloud, or server)
* A [NewsAPI](https://newsapi.org/) key (free signup)
* A [Telegram Bot](https://core.telegram.org/bots#6-botfather) with token

---

### 2. Import Workflow

* Clone this repo
* Import `daily-news-telegram.json` into n8n

---

### 3. Configure Credentials

* **NewsAPI** → add your API key in the HTTP Request node URL:

  ```
  https://newsapi.org/v2/top-headlines?country=in&pageSize=3&apiKey=YOUR_API_KEY
  ```

* **Telegram** → add your Bot Token in Telegram node credentials

---

### 4. Run the Workflow

* Activate the workflow in n8n
* The bot will automatically send daily news to your Telegram chat

---

## 🖼️ Demo

### Example Telegram Output

```
📰 Latest News

1. Centre provides back-to-back boost for the shipbuilding industry  
Government initiatives aim to revitalize India's shipbuilding sector...  
🔗 https://www.thehindubusinessline.com/...

2. Accenture plans on 'exiting' staff who can't be reskilled on AI amid restructuring  
Accenture CEO Julie Sweet said as advanced AI becomes core...  
🔗 https://www.cnbc.com/...

3. Russia is helping China to prepare for potential invasion of Taiwan, think tank says  
Analysis from the Royal United Services Institute...  
🔗 https://abcnews.go.com/...
```

---

## 📌 Customization

* Change `country=in` or add `category=technology` in the NewsAPI URL for specific categories
* Adjust `pageSize` to get more or fewer articles
* Modify the Cron schedule for different times

---

## ⚖️ License

This project is licensed under the MIT License.

---

💡 *Built with n8n automation magic ✨ and shared for learning + inspiration.*
