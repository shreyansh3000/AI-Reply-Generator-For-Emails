# AI-Reply-Generator-For-Emails

This project provides a **Gmail Chrome Extension** that automatically generates context-aware email replies using the **Gemini API**, helping users reply to emails faster and more efficiently. It features a **Spring Boot backend** that handles AI-powered response generation and real-time email tracking.

---

## ✨ Features

- ⚡️ **AI-Powered Responses**: Leverages Gemini API to generate smart, contextual replies to incoming emails.
- 📬 **Gmail API Integration**: Tracks received emails in real time to ensure accurate and relevant responses.
- 🧠 **Smart UI Integration**: Dynamically adds an "AI Generate" button beside Gmail's "Send" button using `MutationObserver`.
- 🚀 **Spring Boot Backend**: Efficient response generation and email tracking handled on the server side.

---

## 📁 Project Structure

- `mutation-observer-extension/`: Chrome Extension folder. Contains the MutationObserver code that modifies Gmail UI.
- `springboot-backend/`: Java Spring Boot project responsible for AI generation and managing email content.

---

## 🧩 How It Works

1. **Add Extension**:
   - Load the extension folder (`mutation-observer-extension/`) as an **unpacked extension** in Chrome.
   - Once enabled, it injects an "AI Generate" button right beside the **Send** button in Gmail's email composer.

2. **Track Emails**:
   - The extension uses the Gmail API to detect new emails and fetch their content.

3. **Generate Replies**:
   - On clicking the **AI Generate** button, the extension sends email content to the Spring Boot backend.
   - The backend calls the **Gemini API** to generate a contextual reply and sends it back.
   - The generated response is inserted into the Gmail reply box automatically.

---

## 🔧 Installation

### 🧱 Backend (Spring Boot)

1. Clone the repo and navigate to `springboot-backend/`
2. Configure environment variables or `application.properties` for Gemini API key, Gmail credentials, etc.
3. Run the application:
   ```bash
   ./mvnw spring-boot:run
