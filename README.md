# 📈 n8n Stock Price Alert (Polygon API → WhatsApp)

This workflow automatically checks a stock's latest **closing price** from the [Polygon.io API](https://polygon.io), compares it to a target price, and sends a **WhatsApp notification** when the condition is met.

---

## 🚀 Features
- Scheduled stock price checks via Polygon.io Free API
- Extracts the latest **close price** (`c` field)
- Compares against a user-defined target
- Sends real-time **WhatsApp alerts** via API
- Beginner-friendly — no coding required

---

## 🛠 Requirements
- [n8n](https://n8n.io) (self-hosted or cloud)
- Polygon.io API key (Free tier supported)
- WhatsApp API provider (Twilio, 360dialog, UltraMsg, etc.)
- Basic knowledge of n8n workflow import

---

## 📂 Workflow Overview
1. **Cron Trigger** – Defines how often to check prices.
2. **HTTP Request** – Calls the Polygon.io Aggregates API for yesterday's close price:  
   `https://api.polygon.io/v2/aggs/ticker/AAPL/prev?adjusted=true&apiKey=YOUR_API_KEY`
3. **Set Node** – Extracts the `c` value (closing price).
4. **IF Node** – Compares price with your target value.
5. **HTTP Request (WhatsApp)** – Sends alert message.

---

## 🔧 Setup Instructions
1. **Clone this repository**
   ```bash
   git clone https://github.com/yourusername/n8n-stock-price-alert.git
   cd n8n-stock-price-alert
   ```
2. **Import Workflow into n8n**:
   - Open n8n Editor
   - Import `workflow/stock_price_alert_polygon.json`
3. **Set Your Environment Variables**:
   - `POLYGON_API_KEY` — from Polygon.io dashboard
   - `WHATSAPP_API_URL` — your provider’s send-message endpoint
   - `WHATSAPP_AUTH` — API key, Basic Auth, or token per your provider
4. **Customize Target Price** in the IF node.
5. **Deploy and test**.

---

## 📸 Screenshots
| Workflow in n8n | WhatsApp Alert |
|-----------------|----------------|
| ![Workflow](screenshotsworkflow-diagram.png) | ![Alert](screenshotswhatsapp-message.png) |

---

## 🌐 Connect With Me
- LinkedIn: [Ahmad Raza](https://www.linkedin.com/in/ahmad-raza-403bbd0278)
- Fiverr: [nitrola](https://www.fiverr.com/nitrola)

---

## 📜 License
MIT License — free to use and modify.

---

## 💡 Ideas for Improvement
- Support multiple stock tickers in one workflow
- Add logging to Google Sheets or Notion
- Include historical price charts in alerts

---

### **Short GitHub Repo Description**
Automated n8n workflow that checks stock prices via Polygon.io API and sends WhatsApp alerts when targets are reached — perfect for traders and investors.
