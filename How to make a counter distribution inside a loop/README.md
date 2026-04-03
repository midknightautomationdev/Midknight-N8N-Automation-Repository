
---

# 🔁 Even Work Distribution Workflow

This workflow allows you to **evenly distribute tasks inside a loop**, ensuring that operations are executed in a balanced and controlled manner across iterations.

---

## 📌 Overview

This setup is useful when you want to:

* Distribute actions evenly across loop iterations
* Control execution flow dynamically
* Assign different tasks per loop cycle

---

## 🧩 Workflow Components

The workflow consists of the following nodes:

* **1 Set Node**
* **2 Code Nodes**
* **1 Loop Over Items Node**
* **9 No Operation Nodes**

  * *(7 of these can be replaced with your own logic for distribution)*
* **1 Switch Node**
* **1 Wait Node**

---

## 🏷️ Node Breakdown

### 🔹 Set Values *(Set Node)*

* Optional step
* Define:

  * Input values
  * Number of loop iterations

---

### 🔹 Duplicate Input as Items *(Code Node)*

* Duplicates input items based on the desired loop count
* Prepares data for looping

---

### 🔹 Loop *(Loop Over Items Node)*

* Processes items **one at a time**
* Drives the iteration logic

---

### 🔹 Run Index Counter *(Code Node)*

* Tracks the current loop iteration
* Example:

  * If 3 items → counter runs from **1 → 3**

---

### 🔹 No Operation *(Pass-through Node)*

* Passes values forward without modification
* Used for structuring workflow

---

### 🔹 Distributor *(Switch Node)*

* Core logic for distribution
* Routes execution based on the **Run Index Counter value**

---

### 🔹 Distribution Slots *(7 No Operation Nodes)*

* These are **placeholders**
* Replace them with any nodes you want to execute evenly
* Example use cases:

  * API calls
  * Data processing steps
  * Conditional tasks

---

### 🔹 Wait *(Wait Node)*

* Adds delay between iterations
* Helps with:

  * Rate limiting
  * Preventing overload

---

### 🔹 Final Pass *(No Operation Node)*

* Passes output to the next loop cycle

---

## ⚙️ How It Works

1. Define how many times the loop should run
2. Duplicate input into multiple items
3. Loop processes each item sequentially
4. Counter tracks the current iteration
5. Switch distributes execution across different nodes
6. Each iteration follows a different path (even distribution)
7. Loop continues until all items are processed

---

## 💡 Use Cases

* Load balancing tasks across multiple processes
* Rotating API keys or endpoints
* Distributing automation steps evenly
* Avoiding rate limits in workflows

---

## 🎥 Full Walkthrough

For a complete guide and demo, check out My YouTube channel:

👉 [https://www.youtube.com/@MidknightCodesNAutomations](https://www.youtube.com/@MidknightCodesNAutomations)

---

## 🔗 Connect With Me

* **LinkedIn:** [https://www.linkedin.com/in/joe-angarrovillojr/](https://www.linkedin.com/in/joe-angarrovillojr/)
* **Facebook (Business):** [https://www.facebook.com/joeangarrovillojr/](https://www.facebook.com/joeangarrovillojr/)
* **Creator Profile:** [https://www.facebook.com/midknightuzer/](https://www.facebook.com/midknightuzer/)

---

## 📬 Contact & Inquiries

For questions, collaborations, or automation-related business inquiries, feel free to reach out:

* 📧 **Email:** [midknightautomation@gmail.com](mailto:midknightautomation@gmail.com)

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

👉 **Store:** [https://midknightdigistore.gumroad.com/](https://midknightdigistore.gumroad.com/)

---

### ⚡ Why Get the Full Version?

* ✅ No need to follow long tutorials
* ✅ Fully configured workflows
* ✅ Ready-to-use integrations
* ✅ Save hours of setup time
* ✅ Plug-and-play automation

---
