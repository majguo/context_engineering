# Context Engineering

This repository explores context engineering techniques for AI agents, based on the 4 categories outlined in the [LangChain blog post](https://blog.langchain.com/context-engineering-for-agents/).

## Categories

### 1. Write Context
**Description**: Saving information outside the context window to help an agent perform a task.

**Examples**:
- **Scratchpads**: Saving information outside context window for future use
- **Memories**: Storing reflections and synthesized memories across multiple sessions

### 2. Select Context
**Description**: Pulling information into the context window to help an agent perform a task.

**Examples**:
- Selecting memories relevant to current task
- Retrieving specific tool descriptions using semantic search
- Using RAG techniques to fetch relevant knowledge

### 3. Compress Context
**Description**: Retaining only the tokens required to perform a task.

**Examples**:
- Context summarization across agent interactions
- Trimming older messages from context
- Using trained models to prune unnecessary context

### 4. Isolate Context
**Description**: Splitting up context to help an agent perform a task.

**Examples**:
- Multi-agent approaches with separate context windows
- Using sandboxed environments to separate context
- Designing state objects with isolated context fields

## Organization

This repository is organized by the four context engineering categories:

```
context_engineering/
├── write_context.md/.ipynb      # Examples of saving context externally
├── select_context.md/.ipynb     # Examples of retrieving relevant context
├── compress_context.md/.ipynb   # Examples of context compression techniques
└── isolate_context.md/.ipynb    # Examples of context isolation methods
```

Each category contains implementations and examples demonstrating the respective context engineering techniques, available in both markdown and Jupyter notebook formats.

## Setup

### Prerequisites
- Python 3.8 or higher
- [uv](https://docs.astral.sh/uv/) package manager

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd context_engineering
```

2. Create and activate a virtual environment using uv:
```bash
uv venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. Install dependencies:
```bash
uv pip install -r requirements.txt
```

4. Set up environment variables:
```bash
export OPENAI_API_KEY="your-openai-api-key"
```

### Running the Examples

#### Jupyter Notebooks
```bash
jupyter lab
# Navigate to context_engineering/ folder and open any .ipynb file
```

#### Python Scripts
All examples from the notebooks can be run directly as Python scripts by copying the code blocks from the markdown files.

## Learn More

To learn more, see:
- [Context Engineering for Agents Blog Post](https://blog.langchain.com/context-engineering-for-agents/) - Original blog post outlining the 4 categories