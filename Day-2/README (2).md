# ⚡ Electric Car Showroom – Agentic AI Day 2

## 📌 Project Overview

An AI-powered customer support chatbot for a fictional electric car showroom inspired by Tesla. Built using Python, Groq API and LangChain in Google Colab, it demonstrates prompt engineering, structured data extraction, conversation memory and error handling.

## ✨ Features

- Electric car model and sample price enquiries
- Budget-based car selection assistance
- English and Telugu customer support
- Few-shot classification into booking, question or complaint
- JSON extraction of booking and test-drive request details
- Sample total price calculation using a Python decorator
- Conversation memory using a recent eight-turn context window
- Customer question history and interactive chat
- API rate-limit and connection error handling
- Admin escalation for unverified showroom information

## 🚘 Sample Car Models and Prices

| Model | Fictional demo price (INR) |
|---|---:|
| Model S | ₹85,00,000 |
| Model 3 | ₹40,00,000 |
| Model X | ₹95,00,000 |
| Model Y | ₹60,00,000 |
| Cybertruck | ₹1,00,00,000 |

**Disclaimer:** These are fictional demonstration prices, not official Tesla prices. This project is educational and is not affiliated with Tesla.

## 🛠️ Technologies Used

- Python 3
- Google Colab
- Groq API and Python SDK
- LangChain (`langchain_groq`)
- LLM: `openai/gpt-oss-120b`
- Python JSON and functools modules

The notebook initializes a LangChain ChatGroq client; the implemented chat, classification and extraction functions call the Groq SDK directly.

## ⚙️ Installation and Setup

1. Open `Electric_Car_Showroom_Day2(1).ipynb` in Google Colab (or the corresponding renamed notebook).
2. Install the required libraries:

   ```bash
   pip install -q langchain_groq groq
   ```

3. Generate a Groq API key at https://console.groq.com/keys.
4. Open the Secrets panel in Google Colab.
5. Add a secret named `GROQ_API_KEY` and enable notebook access.
6. Run the notebook cells sequentially and enter customer messages when prompted.

Never publish your API key in the notebook or GitHub repository.

## 🔄 Project Workflow

```text
Customer message
       ↓
System prompt + recent conversation history
       ↓
Groq API (GPT-OSS 120B)
       ↓
Customer support response
       ↓
Update conversation history
```

Separate notebook demonstrations:

- Message classification using `classify()`
- Structured JSON extraction using `extract_order()`
- Sample price calculation using `get_price()` and `@log_call`

## 📋 Business Rules

- Clearly identify all prices as fictional demo prices.
- Do not invent car specifications or confirm bookings, payments or test drives.
- Refer actual availability, showroom address, test-drive timings, delivery dates, charging specifications, EMI, discounts, on-road prices and booking charges to the admin.
- Use the response "I have to check with the admin." for such enquiries.
- Keep replies brief and use English or Telugu.

## 💬 Example Usage

Example inputs to try:

- `What is the sample price of Model Y?`
- `Which car is suitable for a budget of 50 lakh rupees?`
- `I want to book a white Model 3.`
- `history` — display customer question history.
- `bye` — exit the chat and display question history.

## 🎯 Learning Outcomes

- System prompts and few-shot prompt engineering
- LLM integration through Groq
- Structured JSON responses and missing-value handling
- Python functions and decorators
- Conversation history and context management
- Exception handling and secure API key management

## 🚀 Future Enhancements

- Integrate classification and extraction into the main chatbot workflow
- Connect to verified vehicle inventory and pricing data
- Add a web interface and admin dashboard
- Add persistent conversation storage and human-approved booking workflows

## 📚 Project Information

- **Project:** Electric Car Showroom Customer Support Assistant
- **Program:** DriveReady OPC 2026
- **Task:** Agentic AI – Day 2
- **Platform:** Google Colab

---
Educational AI project for electric vehicle customer support.
