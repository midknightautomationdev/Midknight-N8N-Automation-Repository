# 🤖 AI Call Center Agent – Main Workflow

This workflow serves as the **core automation for an AI-powered call center agent**, integrating multiple services to handle conversations, scheduling, and data management.

---

## 🔗 Integrations

This workflow connects with:

* 📊 Google Sheets
* 📄 Google Docs
* 📅 Google Calendar
* 💬 Facebook Messenger API
* 🤖 Multiple LLM Providers (Grok & Gemini)

---

## 🧩 Workflow Components

### Core Nodes

* **1 Webhook**
* **1 Filter Node**
* **4 Code Nodes**
* **4 Google Sheets Nodes**

  * 2 × Read
  * 2 × Append / Update
* **1 If Node**
* **1 Execute Workflow Node**
* **1 Switch Node**
* **2 HTTP Request Nodes (POST)**

---

### 🛠️ AI & Tools

* **6 Call n8n Workflow Tools**
* **1 Think Tool**
* **1 Calculator Tool**
* **1 Google Docs Tool (Read)**
* **1 Google Calendar Tool**
* **2 Model Selectors**
* **7 Grok LLM Nodes**
* **7 Gemini LLM Nodes**

---

## 🏷️ Node Breakdown

### 🔹 Webhook1

* Entry point of the workflow
* Receives incoming messages from Messenger

---

### 🔹 Filter

* Allows only messages with text to pass through

---

### 🔹 Persistent Value

* Stores relevant webhook data
* Ensures the workflow **remembers context across executions**

---

### 🔹 Get Sender ID

* Checks if the sender already exists in the database

---

### 🔹 Sender Status

* Prepares fields used by the AI agent
* Helps determine how to handle the sender

---

### 🔹 Get Chat

* Retrieves existing chat history

---

### 🔹 If Excess Webhook

* Prevents duplicate processing
* Checks:

  * Message ID
  * Message content
* Avoids spam or repeated execution

---

### 🔹 Chat Summary

* Formats chat history for AI understanding
* Helps the agent maintain context

---

### 🔹 Execute Counter

* Generates a number from **1 to 7**
* Used to evenly distribute LLM usage

---

### 🔹 AI Agent

* Main instruction node for the LLM
* Defines:

  * Behavior
  * Tool usage
  * Response logic

---

## 🧠 Tools System

### 🔹 Think Tool

* Acts as a **scratchpad for reasoning**
* Helps the agent perform multi-step logic

---

### 🔹 Script Tool

* Contains the **knowledge base**
* Gives the agent identity and service awareness

---

### 🔹 Chat Storage Tool

* Stores conversation history
* Uses the same Google Sheet as **Get Chat**

---

### 🔹 Info Storage Tool

* Stores sender/user data
* Uses the same Google Sheet as **Get Sender ID**

---

### 🔹 Calculator Tool

* Handles arithmetic computations

---

## 🔄 Workflow Automation Tools

These tools call **separate n8n workflows**:

* 📧 **Send_Email_Verification_TOOL** – Handles email verification
* 📅 **Get_Schedule_Availability_TOOL** – Fetches available time slots
* 📋 **Get_All_Booked_Slots_TOOL** – Retrieves booked schedules
* 📌 **Book_A_Meeting_TOOL** – Books appointments
* 🔁 **ReBook_A_Meeting_TOOL** – Reschedules appointments
* ❌ **Cancel_A_Meeting_TOOL** – Cancels bookings
* ✏️ **Change_Email_Tool** – Updates user email

---

## 🤖 Model Distribution System

### 🔹 Model Selector (AC Free Model Switcher) 1 & 2

* Dynamically selects which LLM to use
* Based on the **Execute Counter**

---

### 🔹 LLM Nodes

* **Grok LLM (1–7)**

  * Same model
  * Uses different accounts

* **Gemini LLM (1–7)**

  * Same model
  * Uses different accounts

✅ This setup helps:

* Avoid rate limits
* Distribute load evenly
* Improve reliability

---

## ⚙️ How It Works

1. Webhook receives a message
2. Message is filtered and validated
3. Sender and chat history are retrieved
4. Duplicate messages are ignored
5. Context is prepared for the AI agent
6. Execute Counter assigns a model slot (1–7)
7. Model Selector routes to an LLM
8. AI Agent processes the request using tools
9. Response is sent back via HTTP request
10. Data is stored for future interactions

---

## For more info refer to these clickable links below

---

## 🎥 Full Walkthroughs

For more info you can check out My YouTube channel:

👉 [Youtube-@MidknightCodesNAutomations](https://www.youtube.com/@MidknightCodesNAutomations)

---

## 🔗 Connect With Me

* **LinkedIn:** [LN-Proffessional Joe-an Garrovillo](https://www.linkedin.com/in/joe-angarrovillojr/)
* **Facebook (Business):** [FB-Business Joe-an Garrovillo](https://www.facebook.com/joeangarrovillojr/)
* **Creator Profile:** [FB-Creator MidknightUzer](https://www.facebook.com/midknightuzer/)

---

## 📬 Contact & Inquiries

For questions, collaborations, or automation-related business inquiries, feel free to reach out:

* 📧 **Brand-Email:** [midknightautomation@gmail.com](mailto:midknightautomation@gmail.com)
* 📧 **Business-Email:** [joeangarrovillojr@gmail.com](mailto:joeangarrovillojr@gmail.com)

---

### 💼 Let’s Work Together

If you're looking to:

* Automate your business processes
* Build AI-powered workflows
* Integrate tools like n8n, Google Workspace, or APIs

I'm open to projects and collaborations.

---

## 🛒 Get the Full Automation

Want to skip the manual setup and get everything ready-to-use?

You can get the **complete automation workflow**, fully configured and ready to deploy:

👉 **Store:** [Midknight-Digistore](https://midknightdigistore.gumroad.com/)

---

### ⚡ Why Get the Full Version?

* ✅ No need to follow long tutorials
* ✅ Fully configured workflows
* ✅ Ready-to-use integrations
* ✅ Save hours of setup time
* ✅ Plug-and-play automation

---
