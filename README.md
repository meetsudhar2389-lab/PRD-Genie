\# PRD Genie 🧞‍♂️



> \*\*AI-Powered Product Documentation Assistant\*\*  

> \*Transforming unstructured meeting transcripts into engineering-ready PRDs, Epics, and User Stories using Multi-Agent Workflows and Continuous Observability.\*



\---



\## 📌 Project Overview



\*\*PRD Genie\*\* is an enterprise-grade agentic AI assistant designed to eliminate friction in product management workflows. In high-growth engineering and product organizations, Product Managers (PMs) and Technical Product Managers (TPMs) spend substantial time extracting context, scope, and technical constraints from lengthy meeting discussions. Manual conversion of these unstructured discussions into structured Product Requirements Documents (PRDs) often leads to inconsistent formatting, lost institutional context, and delayed time-to-market.



PRD Genie automates and standardizes this end-to-end process:

1\. \*\*Ingests\*\* raw meeting transcripts, discussion notes, and stakeholder recordings.

2\. \*\*Extracts\*\* functional requirements, dependencies, and technical constraints while flagging ambiguities.

3\. \*\*Incorporate Human-in-the-Loop (HITL)\*\* validation gates to ensure accuracy and domain alignment.

4\. \*\*Generates\*\* standardized PRDs using customizable markdown templates (`prd\_template.md`).

5\. \*\*Decomposes\*\* requirements into hierarchical Epics, Jira-ready User Stories with acceptance criteria, gap analysis, and delivery effort estimations.



Driven by a visual \*\*Langflow\*\* orchestration pipeline, \*\*OpenAI `gpt-4o-mini`\*\*, and tracked via \*\*Langfuse\*\* for LLM-as-a-Judge groundedness evaluations, PRD Genie bridges the gap between chaotic product discovery and structured engineering execution.



\---



\## 📁 Repository Structure



```text

├── 📄 README.md                        # Project documentation and setup guide

├── 📂 01\_Ideation\_Document/            # Initial problem framing, user research, and pain point analysis

├── 📂 02\_Program\_Charter/              # Executive charter, OKRs, project scope, and milestones

├── 📂 03\_Product\_Document/             # Functional specifications, HLD, LLD, and Agent Architecture

├── 📂 04\_Sample\_Output\_Files/          # Generated PRDs, Epics, User Stories, Gap Analyses, and Estimates

└── 📂 05\_Test\_Cases\_Executed/          # Evaluation test suites, Langfuse traces, and benchmark results





🚀 Key Features \& Capabilities

Automated Requirements Extraction: Processes unstructured text into JSON schema payloads isolating stakeholders, functional scope, and edge cases.



Human-in-the-Loop (HITL) Routing: Pauses execution when ambiguities are detected, allowing PMs to review and approve/reject extracted inputs before full PRD synthesis.



Standardized PRD Generation: Enforces company-wide template compliance to ensure consistency for engineering estimations.



Parallel Execution Agents:



Story Breakdown Agent: Generates structured Epics and User Stories complete with acceptance criteria.



Gap Analyzer Agent: Scans draft PRDs against historical architectural patterns to identify missing non-functional requirements (NFRs).



Scope Estimator Agent: Assesses delivery complexity and relative sizing metrics.



Observability \& Evaluation: Full trace tracking, token usage analytics, and LLM-as-a-Judge groundedness scoring via Langfuse.



🏗️ Architecture \& Agent Flow

PRD Genie operates as an orchestrated multi-agent network built on Langflow:



Plaintext

\[Chat Input / Meeting Transcript]

&#x20;              │

&#x20;              ▼

&#x20;  \[Requirement Extractor Agent] ──► \[PRD Genie Router (JSON Schema Validation)]

&#x20;                                               │

&#x20;                       ┌───────────────────────┴───────────────────────┐

&#x20;                       ▼                                               ▼

&#x20;                \[Approved Path]                                \[Ambiguities Found]

&#x20;                       │                                               │

&#x20;                       ▼                                               ▼

&#x20;              \[Human-in-the-Loop]                     \[Clarification Routing]

&#x20;                       │

&#x20;                       ▼

&#x20;        \[PRD Generator + Template Loader]

&#x20;                       │

&#x20;        ┌──────────────┼──────────────┐

&#x20;        ▼              ▼              ▼

\[Story Breakdown]  \[Gap Analysis]  \[Scope Estimation]

&#x20;        │              │              │

&#x20;        ▼              ▼              ▼

&#x20; \[Saved File Artifacts \& Chat UI Outputs]



🛠️ Getting Started

Prerequisites

* Python 3.10+
* Langflow
* OpenAI API Key (OPENAI\_API\_KEY)
* Langfuse Account \& API Keys (LANGFUSE\_PUBLIC\_KEY, LANGFUSE\_SECRET\_KEY)

