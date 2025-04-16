# 🧠 Conversational Avatar Interface | CloneByMe

This project provides a conversational interface with an integrated avatar that sends messages to a webhook (e.g., [n8n](https://n8n.io/) or [Make](https://www.make.com/)), where an AI agent can process them and return a spoken response through the avatar.

## 🚀 Features

- Easy integration with CloneByMe to display an interactive avatar.
- Communication via `iframe` with a custom webhook.
- Compatible with automation platforms like n8n and Make.
- Configurable interface with optional functions (toggle messages or typing dots).

---

## 🛠️ Installation & Usage

1. **Clone this repository**:
   ```bash
   git clone https://github.com/CloneByMe/conversational_avatar_interface.git
   cd your-repo
   ```

2. **Configure your token and webhook**:  
   Open the `index.html` file (or your chosen filename) and replace the following lines:

   ```js
   const AVATAR_TOKEN = "[YOUR CLONEBYME ENTERPRISE TOKEN]";
   const WEBHOOK_URL = "[YOUR WEBHOOK URL]";
   ```

   - `AVATAR_TOKEN`: Get this from your account at [CloneByMe](https://app.clonebyme.com) in Share page.
   - `WEBHOOK_URL`: The URL of your webhook configured in n8n or Make, which receives the question and returns the AI's response as JSON.

3. **Open the file in your browser**:
   Simply open the HTML file in your browser to test it locally.

---

## 📦 Expected Webhook Send Format

The webhook will receive a JSON payload like this:

```json
{
  "question": "Hello!"
}
```

- `question`: The message sent by the user that needs to be processed by your AI agent.

---

## 📦 Expected Webhook Response Format

The webhook should return a JSON response like this:

```json
{
  "response": "Hello! I'm here to help you."
}
```

- `response`: The message that will be spoken by the avatar.

---

## 📋 Optional Features

- `setStateOfTypingDots(true/false)`: Show or hide typing dots.
- `showMessagesContainer(true/false)`: Show or hide the message container inside the iframe.

---

## 🤖 Requirements

- An account on [CloneByMe](https://app.clonebyme.com).
- A webhook configured on n8n, Make, or any backend that can accept and respond with JSON.

---


## 📄 License

Unlicense

---

Enhance your conversational experience by connecting your AI agent to an avatar!
