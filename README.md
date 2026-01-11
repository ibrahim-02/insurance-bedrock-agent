# Insurance Claim Lifecycle Agent using Amazon Bedrock

This project demonstrates an end-to-end **AI-powered insurance agent** built using **Amazon Bedrock Agents**, designed to handle real-world insurance workflows such as claim creation, status retrieval, and document reminders.

The focus of this project is **agent orchestration and reasoning**, not just prompt engineering.

---

## 🏗 Architecture Overview


**Components:**
- **Streamlit UI** – User-facing interface
- **Amazon Bedrock Agent** – Core reasoning and orchestration
- **Action Groups (OpenAPI)** – Structured API definitions guiding agent decisions
- **AWS Lambda** – Business logic execution
- **Knowledge Base** – Embedding-based retrieval for insurance FAQs and documents
- **Amazon S3** – Stores OpenAPI schemas and knowledge base documents

---

## 🤖 Agent Flow

1. User submits a request via Streamlit UI
2. Bedrock Agent classifies the request and determines if it is actionable
3. Agent either:
   - Invokes an **Action Group (Lambda)** for transactional tasks, or
   - Queries the **Knowledge Base** for informational responses
4. Agent processes tool outputs and generates a final response
5. **Agent Traces** are used to debug reasoning, tool selection, and execution

---

## 🔧 Key Features

- Amazon Bedrock Agents with structured **Action Groups**
- **OpenAPI schemas** to guide API selection and parameter extraction
- **AWS Lambda** functions for insurance business logic
- **Knowledge Base integration** using embeddings
- **Agent response tracing** for debugging decision-making
- End-to-end UI built with **Streamlit**

---

## 🧪 Debugging & Tracing

The project uses **Amazon Bedrock Agent Traces** to inspect:
- Model invocation inputs
- Tool selection decisions
- Lambda execution payloads
- Knowledge base retrieval steps

Example trace outputs are shown below.

---

## 📸 Screenshots

### Streamlit UI
![UI Demo](https://github.com/ibrahim-02/insurance-bedrock-agent/blob/854716c8d9bd39948e672a58065942189afb6437/Screenshoots/Streamlit%20UI.png)

### Action Group Invocation Trace
![Agent Trace - Action Group](https://github.com/ibrahim-02/insurance-bedrock-agent/blob/0587d8d029c18f416ed9cabd0705c2b9b6affe72/Screenshoots/agent-trace-action-group.png)

### Knowledge Base Retrieval Trace
![Agent Trace - KB](https://github.com/ibrahim-02/insurance-bedrock-agent/blob/main/Screenshoots/kb-console-testing.png)

---


