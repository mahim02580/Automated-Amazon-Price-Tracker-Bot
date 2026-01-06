# Amazon Price Tracker – Python Script

This script monitors the price of an Amazon product and automatically sends an email alert if the price drops below your desired buying threshold. It’s useful if you want to grab a deal without checking the product page repeatedly.

### 🚀 Features
* Scrapes live product price & title from Amazon
* Compares current price against a preset BUY_PRICE
* Sends email notification if the price drops
* Uses `.env` variables for secure credential handling
* Simple and lightweight — no database or server needed

### 📌 Requirements

Python 3.8+

Install dependencies:
`pip install -r requirements.txt`


### ⚙️ Environment Setup

Create a `.env` file and fill in the values:

AMAZON_PRODUCT_URL="https://www.amazon.com/dp/PRODUCT_ID"

BUY_PRICE=200.00

EMAIL_ADDRESS="your_email@example.com"

EMAIL_PASSWORD="EMAIL_PASSWORD_OR_APP_PASSWORD"

SMTP_ADDRESS="SMTP_ADDRESS_OF_YOUR_MAIL_SERVER" e.g. "smtp.gmail.com" for Gmail

_Tip: If you're using Gmail, enable App Password and use that instead of your real password._

### 🧠 How It Works

* Loads configuration from `.env`
* Requests HTML from Amazon using realistic browser headers
* Parses price and product title using BeautifulSoup
* Compares with `BUY_PRICE`
* Sends an email if the current price is cheaper

### ▶️ Run the Script
`python main.py`

### 🛡️ Note
Amazon may block scraping if requests are too frequent or headers are missing.
Use responsibly, adhere to Amazon's Terms of Service.
It might not work as expected if Amazon makes any changes to its website!

### 📬 Example Output (Email)

`Subject: Amazon Price Alert!

Logitech MX Master 3S Mouse is on sale for $89.99!

https://www.amazon.com/dp/XXXXX`

### 📑 License
This project is free for personal use.
