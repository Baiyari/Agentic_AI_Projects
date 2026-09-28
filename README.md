# Agentic AI Projects

A collection of hands-on projects exploring **Agentic AI, LLM-powered applications, Retrieval-Augmented Generation (RAG), workflow automation, and intelligent chatbots**. The repository brings together practical assignments and prototypes built with tools such as Langflow, n8n, and language-model integrations.

> **Repository:** `Agent_AI_Projects`  
> **Author:** Baiyari Debbarma  
> **Focus areas:** Agentic AI · Generative AI · LLM Applications · RAG · Workflow Automation

---

## Table of Contents

- [About the Repository](#about-the-repository)
- [Projects](#projects)
  - [1. AI Agent for Automated Emails and Reminders](#1-ai-agent-for-automated-emails-and-reminders)
  - [2. RAG Chatbot in n8n](#2-rag-chatbot-in-n8n)
  - [3. Multi-Agent System](#3-multi-agent-system)
  - [4. TravelMate AI — Travel Agent Smart Chatbot](#4-travelmate-ai--travel-agent-smart-chatbot)
- [Technology Stack](#technology-stack)
- [Key Concepts Explored](#key-concepts-explored)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Security and Configuration](#security-and-configuration)
- [Disclaimer](#disclaimer)
- [Contact](#contact)

---

## About the Repository

This repository documents practical explorations of AI agents and automation-driven applications. Each project focuses on a different use case—from automating routine tasks and retrieving information from documents to coordinating multiple agents and supporting travel planning.

The goal is to understand how LLM-based systems can be connected to tools, data sources, and workflows to build applications that go beyond simple prompt-and-response interactions.

Projects are maintained as individual assignments and prototypes. Their implementation details, integrations, and configuration requirements may vary.

## Projects

### 1. AI Agent for Automated Emails and Reminders

**File:** `AI Agent for Auto mail and reminder system`

An AI-powered workflow concept designed to support email-related tasks and payment reminders through automation.

**Objective**
- Reduce repetitive manual work associated with reminders.
- Organize reminder-related tasks into an automated workflow.
- Explore how AI agents and workflow automation can support routine productivity use cases.

**Core capabilities / areas explored**
- Email and reminder workflow automation.
- AI-assisted task handling.
- Trigger-based workflow design and process automation.

**Use case:** A productivity assistant for organizing and automating routine email and reminder tasks.

> The exact email provider, trigger conditions, scheduling logic, and integrations depend on the workflow configuration exported with the project.

---

### 2. RAG Chatbot in n8n

**File:** `Agent_RAG_Chatbot.json`

A Retrieval-Augmented Generation (RAG) chatbot workflow built in n8n. The project explores how a conversational AI application can use retrieved information as context when responding to user questions.

**Objective**

Build a chatbot workflow that combines retrieval with LLM-based response generation, with the aim of grounding responses in relevant source information rather than relying only on the model's pre-trained knowledge.

**Conceptual workflow**

1. **Ingest source content** — provide the documents or information that will form the chatbot's knowledge base.
2. **Prepare the content** — extract and split text into manageable chunks.
3. **Create searchable representations** — generate embeddings and store them in a compatible vector store, where configured.
4. **Retrieve relevant context** — find content related to the user's question.
5. **Generate a response** — pass the question and retrieved context to the language model.
6. **Return the answer** — deliver the response through the configured chat workflow.

**Key concepts**
- Retrieval-Augmented Generation (RAG).
- Document processing and chunking.
- Semantic retrieval and vector embeddings.
- LLM orchestration using n8n.
- Conversational question answering.

> The specific embedding model, vector database, document source, and LLM are determined by the nodes and credentials configured in the n8n workflow.

---

### 3. Multi-Agent System

**File:** `MAS_AgenticAI.json`

A multi-agent AI workflow exploring how multiple AI agents or specialized components can contribute to a larger task.

**Objective**

Explore the design of AI systems in which responsibilities can be separated across agents, rather than handled by a single general-purpose agent.

**Concepts explored**
- Multi-agent workflow design.
- Task decomposition and role specialization.
- Agent coordination and information flow.
- LLM-based reasoning and orchestration.

**Why multi-agent systems?**

A complex task can often be separated into smaller subtasks. A multi-agent design makes it possible to assign distinct responsibilities to specialized agents and coordinate their outputs through a workflow.

> Agent roles, handoff logic, tools, and execution sequence should be reviewed in the exported JSON workflow for the exact implementation.

---

### 4. TravelMate AI — Travel Agent Smart Chatbot

**File:** `Travel Agent Smart Chatbot (Agentic AI Assignment).json`  
**Built with:** Langflow

TravelMate AI is a conversational travel-planning assistant designed to help users explore destinations and organize travel plans through natural-language interaction.

**Objective**

Create an AI travel assistant that can understand travel-related requests and support trip planning, destination discovery, and practical travel recommendations. The Langflow design connects a chat input to an AI agent, with web search configured as an agent tool.

**Planned / configured assistance**
- Suggest destinations based on travel interests and preferences.
- Help draft day-by-day itineraries.
- Provide travel-planning suggestions for accommodation areas and local transportation.
- Estimate trip budgets based on user-provided details.
- Offer practical travel tips and packing suggestions.
- Use web search to look for relevant online information when the tool is configured and available.

**High-level workflow**

`User message → Chat Input → AI Agent (language model + configured tools) → Chat Output`

The Web Search component is connected to the agent's tool input so that the agent can invoke search when relevant. Search results and response quality depend on the provider, credentials, model availability, and workflow configuration.

**Example prompts**
- “Plan a three-day trip to Jaipur for a moderate budget.”
- “Suggest destinations for a nature-focused trip in October.”
- “Create a weekend itinerary for Goa.”
- “What should I consider when planning a family trip to Kerala?”

**Technology**
- Langflow for visual LLM workflow development.
- A configurable language model.
- Web Search tool integration, subject to valid authentication and provider availability.

> TravelMate AI is a planning assistant, not a booking platform. Verify current prices, opening hours, visa rules, safety advisories, and availability with official or trusted sources before making travel decisions.

---

## Technology Stack

The repository explores the following tools and concepts across its projects. Not every technology is used in every workflow.

| Technology / Concept | Role |
|---|---|
| Langflow | Visual development and orchestration of LLM applications and agents |
| n8n | Workflow automation and integration of AI with other services |
| Large Language Models (LLMs) | Natural-language understanding and response generation |
| Retrieval-Augmented Generation (RAG) | Grounding responses using retrieved source content |
| Web Search tools | Retrieving online information for supported agent tasks |
| Multi-agent architecture | Separating and coordinating specialized agent responsibilities |
| APIs and credentials | Connecting workflows to model providers and external services |

## Key Concepts Explored

- **AI Agents:** LLM-powered systems that can select and use configured tools to work toward a task.
- **Tool Calling:** Connecting an agent to external functions or services it can invoke when needed.
- **RAG:** Retrieving relevant information from a knowledge source and supplying it to an LLM as context.
- **Workflow Automation:** Connecting triggers, processing steps, AI components, and outputs into repeatable flows.
- **Multi-Agent Orchestration:** Coordinating multiple specialized agents or workflow components to complete a broader task.
- **Human-in-the-Loop Verification:** Reviewing important outputs and checking external facts before acting on them.

## Repository Structure

The repository currently contains individual workflow exports for the projects below:

```text
Agent_AI_Projects/
├── AI Agent for Auto mail and reminder system
├── Agent_RAG_Chatbot.json
├── MAS_AgenticAI.json
├── Travel Agent Smart Chatbot (AgentAI Assignment).json
└── README.md
```

GitHub may display filenames differently depending on the exact names and extensions of uploaded files. The JSON files are workflow exports; they are not necessarily standalone applications that can run without importing them into the corresponding platform and configuring credentials.

## Getting Started

### Langflow project

1. Open your Langflow instance.
2. Import the TravelMate AI JSON workflow using the import option available in your Langflow version.
3. Configure valid credentials for the selected language model.
4. Configure the Web Search integration and provide any required authentication.
5. Check that the chat input, agent, and chat output are connected.
6. Run the flow in the Playground and test it with travel-related prompts.

### n8n projects

1. Open your n8n instance.
2. Import the relevant workflow JSON using n8n's workflow import feature.
3. Review each node and its connections.
4. Configure the required credentials, environment variables, and external services.
5. Confirm that any required data sources, document stores, or triggers are configured.
6. Execute the workflow with test data before using it in a live environment.

### Multi-agent workflow

Import `MAS_AgenticAI.json` into the platform it was exported from, then review the agent roles, model configuration, tools, and handoff connections. Configure credentials before execution.

**Note:** Platform versions and node integrations may differ. Some workflows may require adjustments before they run in another environment.

## Security and Configuration

- Never commit API keys, access tokens, passwords, or private credentials to GitHub.
- Use the platform's credential manager or environment variables for secrets.
- Review workflow exports before publishing to ensure that they do not contain sensitive data.
- Use test accounts and sample data while developing.
- Treat AI-generated outputs and web-search results as suggestions that require verification, especially for financial, travel, or other consequential decisions.

If a credential was accidentally committed, remove it from the repository and revoke or rotate it with the provider. Deleting it from the latest file alone may not remove it from Git history.

## Disclaimer

These projects are educational prototypes and demonstrations of AI, agentic workflows, and automation concepts. They are not presented as production-ready services. Features and integrations depend on the exported workflow, external providers, model availability, and user configuration.

## Contact

**Baiyari Debbarma**  
MBA — Data Science & Data Analytics  
Symbiosis Centre for Information Technology (SCIT), Pune

- LinkedIn: [Baiyari Debbarma](https://www.linkedin.com/)

---

*Built as part of Agentic AI Class assignments and Projects*
