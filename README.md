# 🤖 Agents in Action

[![Microsoft Agent Framework](https://img.shields.io/badge/Microsoft-Agent%20Framework-blue?style=for-the-badge&logo=microsoft)](https://learn.microsoft.com/en-us/agent-framework/)
[![Python](https://img.shields.io/badge/Python-3.10+-green?style=for-the-badge&logo=python)](https://python.org)
[![Azure AI](https://img.shields.io/badge/Azure-AI%20Foundry-blue?style=for-the-badge&logo=microsoft-azure)](https://ai.azure.com)

**AI Agent Implementations & Sample Use Cases**

*Master Agents through hands-on agent implementations and workflows*

---

🎯 [Getting Started](#-getting-started) • 🤖 [Agent Samples](#-agent-framework-samples) • 💼 [Sample Use Cases](#-sample-use-cases) • 🛠️ [Setup Guide](#-environment-setup)

---

## 🎯 Mission Statement

This repository showcases AI agent implementations and sample use cases using the **Microsoft Agent Framework**. Through practical samples and comprehensive examples, you'll learn to build sophisticated multi-agent systems, workflows, and autonomous AI applications.

> **🎓 Format**: Hands-on samples and example use cases  
> **🎯 Target Audience**: Developers building AI agent applications  
> **💡 Approach**: Learn by example with practical implementations

---

## 📁 Repository Structure

```
agents-in-action/
├── 🤖 agent-framework/          # Microsoft Agent Framework samples & tutorials
│   ├── agents/                 # Azure AI Agents and MCP integrations
│   ├── workflows/              # Orchestration, checkpointing, human-in-the-loop
│   ├── middleware/             # Request/response interception patterns
│   ├── context_providers/      # Memory and context management
│   ├── threads/                # Conversation management
│   ├── observability/          # Monitoring and evaluation
│   └── devui/                  # Development UI for testing
│
├── 💼 samples/                  # Sample implementations & use cases
│   ├── code_migration/         # Migration Assistant Agent
│   └── book_generator/         # Kids Educational Book Generator
│
├── .env.example                # Environment configuration template
└── requirements.txt            # Python dependencies
```

---

## 🚀 Getting Started

### Step 1: Clone & Setup

```powershell
# Clone the repository
git clone https://github.com/dhangerkapil/agents-in-action.git
cd agents-in-action

# Verify Python version (3.10+ required)
python --version
```

### Step 2: Create Virtual Environment

```powershell
# Create and activate virtual environment
python -m venv .venv
.\.venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Step 3: Configure Environment Variables

1. Copy `.env.example` to `.env`:
   ```powershell
   cp .env.example .env
   ```

2. Update the following variables in `.env`:
   ```properties
   # Azure OpenAI Configuration
   AZURE_OPENAI_API_KEY=your_api_key_here
   AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
   AZURE_OPENAI_CHAT_DEPLOYMENT_NAME=gpt-4o
   AZURE_OPENAI_IMAGE_DEPLOYMENT=gpt-image-1-mini
   
   # Azure AI Foundry (optional, for specific samples)
   AZURE_AI_PROJECT_ENDPOINT=your_project_endpoint
   AZURE_AI_MODEL_DEPLOYMENT_NAME=gpt-4o
   ```

### Step 4: Explore the Samples

Start with the [Agent Framework Samples](#-agent-framework-samples) to learn fundamentals, then explore [Sample Use Cases](#-sample-use-cases) for practical implementations.

---

## 🤖 Agent Framework Samples

The **Microsoft Agent Framework** is an open-source development kit that unifies Semantic Kernel and AutoGen into a next-generation foundation for AI agent development. It provides two primary capabilities:

- **🤖 AI Agents**: Autonomous decision-making with tool integration and conversation management
- **🔄 Workflows**: Orchestrating complex multi-agent processes with type safety and checkpointing

📖 [Official Documentation](https://learn.microsoft.com/en-us/agent-framework/) • 🔗 [GitHub Repository](https://github.com/microsoft/agent-framework)

### 🤖 Azure AI Agents
**Location:** `agent-framework/agents/azure_ai_agents/`

| Sample | Description |
|--------|-------------|
| 🤖 [Basic Agent Usage](agent-framework/agents/azure_ai_agents/azure_ai_basic.ipynb) | Fundamental agent concepts with automatic lifecycle management |
| ⚙️ [Explicit Settings](agent-framework/agents/azure_ai_agents/azure_ai_with_explicit_settings.ipynb) | Agent creation with explicit configuration patterns |
| 🔄 [Existing Agent Management](agent-framework/agents/azure_ai_agents/azure_ai_with_existing_agent.ipynb) | Working with pre-existing agents using agent IDs |
| 💬 [Thread Management](agent-framework/agents/azure_ai_agents/azure_ai_with_existing_thread.ipynb) | Conversation thread continuity and management |
| 🔧 [Function Tools](agent-framework/agents/azure_ai_agents/azure_ai_with_function_tools.ipynb) | Comprehensive function tool integration patterns |
| 💻 [Code Interpreter](agent-framework/agents/azure_ai_agents/azure_ai_with_code_interpreter.ipynb) | Python code execution and mathematical problem solving |
| 📄 [File Search](agent-framework/agents/azure_ai_agents/azure_ai_with_file_search.ipynb) | Document-based question answering with file uploads |
| 🌐 [Bing Grounding](agent-framework/agents/azure_ai_agents/azure_ai_with_bing_grounding.ipynb) | Web search integration using Bing Grounding |

### 🔌 Model Context Protocol (MCP)
**Location:** `agent-framework/agents/mcp/`

| Sample | Description |
|--------|-------------|
| 🔌 [Azure AI with MCP](agent-framework/agents/mcp/azure_ai_with_mcp.ipynb) | Hosted MCP tools with Azure AI Foundry agents |
| 🖥️ [Agent as MCP Server](agent-framework/agents/mcp/agent_as_mcp_server.py) | Expose Agent Framework agents as MCP servers |
| 🔐 [MCP API Key Auth](agent-framework/agents/mcp/mcp_api_key_auth.py) | API key authentication patterns for MCP servers |

### 🔄 Workflows
**Location:** `agent-framework/workflows/`

| Category | Samples |
|----------|---------|
| 📚 **Start Here** | [Executors & Edges](agent-framework/workflows/_start-here/step1_executors_and_edges.ipynb), [Agents in Workflows](agent-framework/workflows/_start-here/step2_agents_in_a_workflow.ipynb), [Streaming](agent-framework/workflows/_start-here/step3_streaming.ipynb) |
| 🎯 **Orchestration** | Sequential and concurrent agent coordination patterns |
| ⚡ **Parallelism** | Fan-out/fan-in, map-reduce, concurrent execution |
| 🎭 **Control Flow** | Conditional routing, loops, dynamic branching |
| 💾 **State Management** | Shared state, context passing, data persistence |
| 🔄 **Checkpointing** | State snapshots, resume from failure, long-running workflows |
| 👤 **Human-in-the-Loop** | Interactive approval, feedback loops, manual intervention |
| 📊 **Observability** | Workflow monitoring, execution tracing, performance metrics |
| 🎨 **Visualization** | Workflow diagrams, execution graphs, flow rendering |

### 🛡️ Middleware
**Location:** `agent-framework/middleware/`

| Sample | Description |
|--------|-------------|
| 🔧 [Agent & Run Level](agent-framework/middleware/1-agent_and_run_level_middleware.ipynb) | Middleware fundamentals and scoping |
| 🔨 [Function-Based](agent-framework/middleware/2-function_based_middleware.ipynb) | Function-based middleware patterns |
| 🏗️ [Class-Based](agent-framework/middleware/3-class_based_middleware.ipynb) | Class-based middleware with inheritance |
| 🎨 [Decorator Middleware](agent-framework/middleware/4-decorator_middleware.ipynb) | @agent_middleware and @function_middleware decorators |
| 💬 [Chat Middleware](agent-framework/middleware/5-chat_middleware.ipynb) | Message interception and modification |
| ⚠️ [Exception Handling](agent-framework/middleware/6-exception_handling_with_middleware.ipynb) | Error handling and recovery patterns |
| 🛑 [Termination](agent-framework/middleware/7-middleware_termination.ipynb) | Early termination and control flow |
| 🔄 [Result Override](agent-framework/middleware/8-override_result_with_middleware.ipynb) | Streaming and non-streaming result modification |
| 📦 [Shared State](agent-framework/middleware/9-shared_state_middleware.ipynb) | State management with middleware containers |

### 🧠 Context Providers
**Location:** `agent-framework/context_providers/`

| Sample | Description |
|--------|-------------|
| 💾 [Azure AI Memory](agent-framework/context_providers/1-azure_ai_memory_context_providers.ipynb) | Agent memory with user fact extraction, tone detection, and persistent context |

### 🧵 Threading & Conversation Management
**Location:** `agent-framework/threads/`

| Sample | Description |
|--------|-------------|
| 💬 [Thread Serialization](agent-framework/threads/1-azure-ai-thread-serialization.ipynb) | Service-managed threads with cloud storage |
| 🔧 [Custom Message Store](agent-framework/threads/2-custom_chat_message_store_thread.ipynb) | Custom ChatMessageStoreProtocol implementation |
| 📦 [Redis Message Store](agent-framework/threads/3-redis_chat_message_store_thread.ipynb) | Distributed conversation storage |
| 🔄 [Suspend/Resume](agent-framework/threads/4-suspend_resume_thread.ipynb) | Thread persistence patterns |

### 📊 Observability
**Location:** `agent-framework/observability/`

| Sample | Description |
|--------|-------------|
| 👁️ [Agent Observability](agent-framework/observability/1-azure_ai_agent_observability.ipynb) | Trace LLM calls, tool executions, token usage |
| 💬 [Chat Client Observability](agent-framework/observability/2-azure_ai_chat_client_with_observability.ipynb) | Monitor Azure AI chat clients |

### 🎨 Development UI
**Location:** `agent-framework/devui/`

| Sample | Description |
|--------|-------------|
| 🌐 [In-Memory Mode](agent-framework/devui/in_memory_mode.py) | Quick-start web interface for testing agents |
| 🤖 [Sample Agents](agent-framework/devui/) | Pre-built examples: Foundry agent, weather agent, spam workflow |

---

## 💼 Sample Use Cases

Sample implementations demonstrating practical applications of Agent Framework.

### 🔄 Migration Assistant Agent
**Location:** `samples/code_migration/agent_framework/`

An intelligent agent that helps developers migrate code from other frameworks (AutoGen, Semantic Kernel, LangChain) to Microsoft Agent Framework.

**Features:**
- 📚 Indexes and searches 200+ official Agent Framework samples
- 🔍 Semantic search across Python and .NET implementations
- 💡 Provides migration guidance with code examples
- 🔗 Links to official GitHub samples and documentation
- 🤖 Interactive DevUI for testing and exploration

**Key Files:**
- `agent.py` - Main migration assistant agent
- `indexer.py` - Sample indexing with LLM-generated metadata
- `index.json` - Pre-indexed sample database

**Run the agent:**
```powershell
cd samples/code_migration/agent_framework
python agent.py
# Opens at http://localhost:8090
```

**Capabilities:**
- Search samples by tags (workflow, middleware, tools, etc.)
- Fetch actual code from GitHub repositories
- Get migration patterns for AutoGen, Semantic Kernel, LangChain
- Interactive chat with context-aware responses

---

### 📚 Kids Educational Book Generator
**Location:** `samples/book_generator/agent_framework/`

A sophisticated multi-agent workflow that generates personalized children's educational books with illustrations, complete with parent discussion guides.

**Features:**
- 📖 Structured book generation with Pydantic models
- ⚡ Fan-out/fan-in parallel processing for chapters
- 🎨 AI-generated illustrations using Azure OpenAI (gpt-image-1-mini)
- 🔄 Quality assurance with feedback loops
- 💾 Shared state management for artifacts
- 🌐 Unsplash fallback for images

**Key Components:**
- Multi-agent collaboration (Structure Planner, Content Generator, QA Reviewer)
- Parallel page generation with image synthesis
- HTML rendering with embedded images
- Iterative refinement with quality feedback

**Run the workflow:**
```powershell
cd samples/book_generator/agent_framework
python workflow.py
# Opens at http://localhost:8090
```

**Example Topics:**
- "How do airplanes fly?"
- "Why is the sky blue?"
- "How do plants grow?"

**Output:**
- Complete HTML book with images
- Age-appropriate content (6-year-olds)
- Parent discussion questions
- Activity suggestions

---

## 🔧 Environment Setup

### 📋 System Requirements

- 🐍 **Python 3.10+** - Required for Agent Framework
- ☁️ **Azure Subscription** - For Azure OpenAI and AI Foundry
- 💻 **VS Code** (Recommended) - Best development experience
- 🛠️ **Azure CLI** (Optional) - For resource management

### 🔑 Azure Resources Needed

1. **Azure OpenAI Resource**
   - Deploy models: `gpt-4o`, `gpt-4o-mini`, `gpt-image-1-mini`
   - Get API key and endpoint from Azure Portal

2. **Azure AI Foundry Project** (Optional)
   - For Azure AI Agents samples
   - Connect to your Azure OpenAI resource

### 📦 Dependencies

All dependencies are in `requirements.txt`:
```
agent-framework --pre
azure-identity
azure-ai-projects
azure-ai-inference
openai
python-dotenv
jupyter
pandas
tabulate
...
```

Install with:
```powershell
pip install -r requirements.txt
```

---

## 🛠️ Troubleshooting

### Common Issues

**Import Errors:**
```powershell
# Ensure you're in the virtual environment
.\.venv\Scripts\activate

# Reinstall dependencies
pip install -r requirements.txt --force-reinstall
```

**Environment Variables Not Loading:**
```powershell
# Verify .env file exists in root directory
ls .env

# Check dotenv is loading correctly
python -c "from dotenv import load_dotenv; load_dotenv(); import os; print(os.getenv('AZURE_OPENAI_API_KEY'))"
```

**Azure OpenAI Authentication:**
```powershell
# Test your credentials
python -c "from openai import AzureOpenAI; client = AzureOpenAI(api_key='your_key', azure_endpoint='your_endpoint', api_version='2024-02-01'); print('Success!')"
```

**Image Generation Not Working:**
- Verify `AZURE_OPENAI_IMAGE_DEPLOYMENT` is set in `.env`
- Ensure you've deployed `gpt-image-1-mini` model in Azure OpenAI
- Check the debug output for response structure

---

## 📚 Additional Resources

- 📖 [Microsoft Agent Framework Documentation](https://learn.microsoft.com/en-us/agent-framework/)
- 🔗 [Agent Framework GitHub](https://github.com/microsoft/agent-framework)
- 🎥 [Azure AI Video Tutorials](https://learn.microsoft.com/en-us/shows/ai-show/)
- 💡 [Azure OpenAI Service](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- 🛡️ [Responsible AI Guidelines](https://learn.microsoft.com/en-us/azure/ai-services/responsible-use-of-ai-overview)

---

## 🤝 Contributing

Contributions are welcome! This repository will continue to grow with more agent samples and use cases.

**Ways to Contribute:**
- 🐛 Report bugs or issues
- 💡 Suggest new sample use cases
- 📝 Improve documentation
- 🔄 Submit pull requests with new sample implementations

---

## 📄 License

**License:** MIT License  
**Repository:** [github.com/dhangerkapil/agents-in-action](https://github.com/dhangerkapil/agents-in-action)

---

## 🔖 Version History

- **v1.0** - Initial release with Agent Framework samples and two sample use cases
  - Migration Assistant Agent
  - Kids Educational Book Generator
  - Complete Agent Framework sample collection

*More agent sample implementations coming soon!*
