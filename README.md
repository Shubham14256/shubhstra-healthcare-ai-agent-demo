# 🏥 Shubhstra Healthcare AI Agent & WhatsApp CRM
**Autonomous Patient Management **

> 🔒 **PROPRIETARY SHOWCASE NOTICE**
> This repository serves as an architectural showcase and technical documentation for a production-grade AI agent built by **Shubhstra Tech**. The core source code is closed-source and strictly proprietary, as it is actively deployed for live US Healthcare clients and processes sensitive data.

## 🚀 System Overview
Administrative burnout is the #1 enemy of medical practices. This system is a high-throughput, AI-native WhatsApp bot that acts as a 24/7 virtual front-desk for clinics. It handles intelligent patient routing, autonomous appointment booking, live queue management, and AI-powered medical report analysis with zero human intervention.


## 🛠️ Architecture & Tech Stack
Engineered for scale, low latency, and real-time execution.
* **Core Framework:** Next.js, Node.js
* **AI & Vision:** Google Gemini API (LLM & Multimodal Vision)
* **Infrastructure:** Meta Cloud API (WhatsApp Webhooks), Vercel
* **Database & Auth:** Supabase (PostgreSQL), Redis (Caching)
* **Architecture Pattern:** Event-Driven Webhook Architecture

## 🧠 Core Autonomous Capabilities

### 1. AI Health Triage & Vision Analysis
* **NLP Symptom Checker:** Dynamically parses unstructured patient queries (e.g., "I have a severe headache") and provides preliminary health advice/home remedies.
* **Medical Report Vision (OCR):** Patients can upload images of blood tests or X-rays. The AI extracts abnormal values and structures the data for the doctor's review.

### 2. Intelligent Patient Workflow
* **Dynamic Queue Management:** Real-time O(1) queue status retrieval. Patients can check their exact position and estimated wait time.
* **Automated Scheduling:** Natural language appointment booking seamlessly integrated into the clinic's calendar.
* **Growth Engine:** Automated referral code generation and post-visit Rating/Google Review workflows.

### 3. 'God-Mode' Doctor Commands (Admin)
Secure, role-based execution triggered exclusively from authorized doctor numbers:
* `/search [Name]`: Instantly retrieves patient history from Supabase.
* `/queue`: Fetches the live daily patient queue.
* `/report [Name]`: Generates a PDF summary of the patient's interactions.

---

## 🔬 System Execution Logs (Proof of Work)
*Below is a real-time terminal output demonstrating the event-driven webhook processing an AI triage request:*

```bash
📨 Incoming webhook data:
═══════════════════════════════════════
{
  "object": "whatsapp_business_account",
  "entry": [{"id": "xxx", "changes": [{"value": {"messages": [...]}}]}]
}
═══════════════════════════════════════

📞 Display Phone Number (Doctor's Number): +91XXXXXXXXXX
✅ Doctor Identified: Dr. Demo Doctor
👤 Patient Name from WhatsApp: John Doe
💾 Patient record updated (ID: xxx-xxx-xxx)

📱 Message Details:
  From (Patient): 91XXXXXXXXXX
  Type: text
  Text: I have a severe headache and slight fever

🤖 Processing text message logic...
🤖 Health query detected - Consulting AI...
🤖 AI Query: "I have a severe headache and slight fever..."
✅ AI Response: "I understand you're experiencing..."
✅ AI health triage payload dispatched successfully (Latency: 1.2s)
