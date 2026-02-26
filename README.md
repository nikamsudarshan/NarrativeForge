# NarrativeForge: Automated Creative Synthesis via Multi-Agent Orchestration

**A sophisticated n8n-based generative pipeline that leverages Large Language Models (LLMs) and external knowledge tools to transform structured creative briefs into factually-grounded, high-fidelity long-form narratives.**

---

## 🚀 Core Features

* **Structured Brief Ingestion:** Utilizes a multi-field form trigger to capture granular creative constraints, including genre, pacing, mood, and technical keywords.
* **Fact-Grounded Generation:** Features a mandatory tool-usage protocol that invokes Wikipedia APIs to integrate authentic real-world details into fictional narratives for enhanced realism.
* **Dynamic Agentic Orchestration:** Employs a LangChain-powered AI agent to synthesize complex user visions while adhering to strict operational parameters.
* **Automated Document Synthesis:** Seamlessly converts generated text into downloadable file formats for immediate distribution or archival.
* **Customizable Narrative Heuristics:** Allows for precision control over narrative style, point of view, and target audience alignment.

## 🛠 Technical Stack

The architecture is built upon a modern automation and AI orchestration stack:

* **Workflow Orchestration:** [n8n](https://n8n.io/) (Visual Automation Platform).
* **LLM Framework:** [LangChain](https://www.langchain.com/) (Agentic and Tool-calling modules).
* **Large Language Model:** [Google Gemini](https://ai.google.dev/).
* **External Intelligence:** Wikipedia Tool (via LangChain).
* **Frontend Trigger:** n8n Form Builder.

## 🏗 System Architecture (Logic Flow)

The system operates as a linear, state-aware pipeline:

1. **Form Submission:** The user inputs 13 distinct creative parameters (e.g., central conflict, plot twist, word count) via the `n8n-nodes-base.formTrigger`.
2. **Agent Initialization:** The `Story Gen AI Agent` receives the brief and initializes its system instructions as a "Narrative Generation Engine".
3. **Research & Synthesis (Branching Logic):** If real-world elements are detected, the agent queries the **Wikipedia Tool** to retrieve factual data points.
4. **Content Generation:** The **Google Gemini Chat Model** processes the combined brief and research data to generate a pure narrative output.
5. **Serialization:** The final text is passed to the `Convert to File` node, transforming the raw string into a structured file output.

---

## 🔬 Scientific & Research Relevance

In a research-intensive environment like **IISc Bangalore**, this agentic architecture provides a blueprint for several advanced applications:

* **Synthetic Data Generation:** Creating diverse, factually-grounded scenarios for training and testing NLP models or safety protocols.
* **Automated Research Summarization:** Adapting the pipeline to ingest scientific abstracts and generate lay-audience summaries or pedagogical narratives.
* **Knowledge Graph Enrichment:** Demonstrating how LLMs can be constrained to verify information against trusted external databases (Wikipedia) before outputting results—a critical requirement for reducing hallucinations in scientific AI.

---

## 💻 Installation & Usage

### Prerequisites

* An active [n8n](https://n8n.io/) instance (Desktop or Cloud).
* A Google Gemini (PaLM/Generative AI) API Key.

### Setup

1. **Import Workflow:**
* Download the `AIstoryGen.json` file.
* In your n8n canvas, click **Import from File** and select the JSON.


2. **Configure Credentials:**
* Open the **Google Gemini Chat Model** node and add your API credentials.


3. **Activate Webhook:**
* Save the workflow and toggle it to **Active**.


4. **Generate:**
* Open the Form URL provided by the **On form submission** node, fill in your brief, and submit.



---

## 👨‍🔬 About the Author

I am a **Mechatronics Engineering student** at **New Horizon Institute of Technology** (affiliated with the **University of Mumbai**) with a **Minor in Information Technology**. My work focuses on the intersection of automated systems and software intelligence.

As the founding member of the **ARMORY Robotics Club**, I have led projects ranging from hexapod kinematics to advanced n8n automation workflows. I am dedicated to exploring how agentic AI can streamline complex R&D processes and am currently seeking opportunities to apply these skills in a high-impact research environment.
