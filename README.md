🎙️ Voice-Controlled Local AI Agent

📌 Overview
This project implements a Voice-Controlled Local AI Agent that takes audio input, converts it into text, detects user intent, and performs appropriate actions on 
the local system.

The system follows a hybrid approach:
- A Large Language Model (LLM) is used for intent classification and general chat
- A Hugging Face transformer model is used specifically for text summarization

This design makes the system modular, efficient, and scalable.

---

🚀 Features

- 🔊 Speech-to-Text (STT)
  - Converts audio into text using local or API-based models

- 🧠 Intent Detection
  - Uses LLM to classify user intent

- ⚙️ Task Execution
  - Create files
  - Generate and write code
  - Summarize text
  - General chat

- 📄 Pipeline Output
  - Displays transcription, intent, and final output

---

🧠 Supported Intents

- Create File
- Write Code
- Summarize Text
- General Chat

---

🏗️ System Architecture

Audio Input  
↓  
Speech-to-Text (STT)  
↓  
LLM (Intent Classification)  
↓  
Task Router  
├── File Operations  
├── Code Generation  
├── Text Summarization (Hugging Face Model)  
└── General Chat (LLM)  
↓  
UI Output  

---

⚙️ Tech Stack

- Frontend: React / HTML / CSS  
- Backend: Python  
- Summarization: Hugging Face Transformers  
- File Handling: Python OS module  

---

🧩 Implementation Details

Summarization Approach
For summarization, a dedicated Hugging Face transformer model is used instead of the LLM.

Flow:
- User inputs a long paragraph
- System detects "Summarize Text" intent
- Paragraph is passed to the transformer model
- Model generates a concise summary (7–8 lines)

Reason:
- Faster execution
- Consistent output
- Modular design

File Safety
All files are created inside a restricted folder:

/output/

This prevents accidental modification of system files.
---
