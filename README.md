![oreilly-logo](images/oreilly.png)

# Designing and Deploying LLM Pipelines

This repository contains code for the [O'Reilly Live Online Training for Designing and Deploying LLM Pipelines](https://learning.oreilly.com/live-events/designing-and-deploying-llm-pipelines/0642572014796)

In this comprehensive course, machine learning engineers and software developers learn how to transition large language model (LLM) prototypes into fully deployed production systems. Through detailed instruction and real-world case studies, you explore the best practices for integrating LLMs into diverse workflows, ensuring that your models perform effectively in practical applications.

## Setup Instructions

### Using Python 3.11 Virtual Environment

At the time of writing, we need a Python virtual environment with Python 3.11.

#### Option 1: Python 3.11 is Already Installed

##### Step 1: Verify Python 3.11 Installation

```bash
python3.11 --version
```

##### Step 2: Create a Virtual Environment

```bash
python3.11 -m venv .venv
```

This creates a `.venv` folder in your current directory.

##### Step 3: Activate the Virtual Environment

- **macOS/Linux:**
  
  ```bash
  source .venv/bin/activate
  ```

- **Windows:**
  
  ```cmd
  .venv\Scripts\activate
  ```

You should see `(.venv)` in your terminal prompt.

##### Step 4: Verify the Python Version

```bash
python --version
```

##### Step 5: Install Packages

```bash
pip install -r requirements.txt
```

##### Step 6: Deactivate the Virtual Environment

```bash
deactivate
```

---

#### Option 2: Install Python 3.11

If you don’t have Python 3.11, follow the steps below for your OS.

##### **macOS (Using Homebrew)**

```bash
brew install python@3.11
```

##### **Ubuntu/Debian**

```bash
sudo apt update
sudo apt install python3.11 python3.11-venv
```

##### **Windows (Using Windows Installer)**

1. Go to [Python Downloads](https://www.python.org/downloads/release/python-3110/).
2. Download the installer for Python 3.11.
3. Run the installer and ensure **"Add Python 3.11 to PATH"** is checked.

### Verify Installation

```bash
python3.11 --version
```

You might need to run this command to make the venv findable in jupyter

```bash
python -m ipykernel install --user --name=oreilly-ai-pipelines --display-name "Python (oreilly-ai-pipelines)"
```


## Notebooks



#### Agents and Workflows

- **[Introduction to LangGraph](notebooks/LangGraph_Hello_World.ipynb)** - Building workflows and agents with LangGraph
	- **[Reflection to LangGraph](notebooks/LangGraph_Reflect.ipynb)** - Reflection with LangGraph
	- **[Planning/Executing with LangGraph](notebooks/LangGraph_Plan_Execute.ipynb)** - Planning/Executing with LangGraph
	- **[ReAct with LangGraph](notebooks/LangGraph_React.ipynb)** - ReAct Agents with LangGraph
		- **[Using Local LLMs](notebooks/LangGraph_React_Local_LLMs.ipynb)** - ReAct Agents with LangGraph with local llms
	- **[Evaluating LangGraph](notebooks/LangGraph_Workfow_Eval.ipynb)** - Evaluating LangGraph
- **[Introduction to CrewAI](notebooks/CrewAI_Hello_World.ipynb)** - CrewAI 101
- **[Introduction to OpenAI Agents](notebooks/OpenAI%20Agents.ipynb)** - OpenAI Agents 101
- **[Introduction to SmolAgents](notebooks/SmolAgents.ipynb)** - HuggingFace's SmolAgents 101

#### Deployment + Production
	
- **[Model Training/Serving with BERT](notebooks/model_serving.ipynb)** - Fine-tuning and running batch data loads with BERT
- **[Deploying models with FastAPI](deploy/)** - using FastAPI to deploy a model
- **[Third party model inference](notebooks/third_party_inference.ipynb)** - Using different types of LLM providers
- **[Using Evaluation to combat AI drift](https://colab.research.google.com/drive/14E6DMP_RGctUPqjI6VMa8EFlggXR7fat?usp=sharing)** - See how drift affects ML models

#### Distillation + Quantization

- **[Quantizing Llama-3 dynamically](https://colab.research.google.com/drive/12RTnrcaXCeAqyGQNbWsrvcqKyOdr0NSm?usp=sharing)** - Using bitsandbytes to quantize a model in real-time on load. We will investigate the differences before and after quantization

	- **[Working with llama.cpp and GGUF (no GPU)](https://colab.research.google.com/drive/15IC5cI-aFbpND5GrvKjAMas1Hmc7M6Rg?usp=sharing)** - See how to load a pre-quantized version of Llama to compare speed and memory usage
	- **[Working with llama.cpp and GGUF (with a GPU)](https://colab.research.google.com/drive/1D6k-BeuF8YRTR8BGi2YYJrSOAZ6cYX8Y?usp=sharing)**

## Instructor

**Sinan Ozdemir** Sinan is a former lecturer of Data Science at Johns Hopkins University and the author of multiple textbooks on data science and machine learning. Additionally, he is the founder of the recently acquired Kylie.ai, an enterprise-grade conversational AI platform with RPA capabilities. He holds a master’s degree in Pure Mathematics from Johns Hopkins University and is based in San Francisco, CA.