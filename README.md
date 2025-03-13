<div align="center">

# DataLens: The Intelligent Chart Generator 📊
<div align="center" style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center">
  <a href="https://github.com/langgraph" target="_blank">
    <img src="https://img.shields.io/badge/LangGraph-0072B8?style=for-the-badge&logo=github&logoColor=white" alt="LangGraph" height="30">
  </a>
  <a href="https://github.com/langchain" target="_blank">
    <img src="https://img.shields.io/badge/LangChain-3D9970?style=for-the-badge&logo=github&logoColor=white" alt="LangChain" height="30">
  </a>
  <a href="https://www.python.org/" target="_blank">
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" height="30">
  </a>
  <a href="https://openai.com/api/" target="_blank">
    <img src="https://img.shields.io/badge/OpenAI%20API-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI" height="30">
  </a>
  <a href="https://www.crummy.com/software/BeautifulSoup/" target="_blank">
    <img src="https://img.shields.io/badge/BeautifulSoup-FF7F50?style=for-the-badge&logo=python&logoColor=white" alt="BeautifulSoup" height="30">
  </a>
  <a href="https://replit.com/languages/python3" target="_blank">
    <img src="https://img.shields.io/badge/PythonREPL-F7DF1E?style=for-the-badge&logo=python&logoColor=black" alt="PythonREPL" height="30">
  </a>
  <a href="https://tavily.com/" target="_blank">
    <img src="https://img.shields.io/badge/Tavily-9B59B6?style=for-the-badge&logo=github&logoColor=white" alt="Tavily" height="30">
  </a>
  <a href="https://langsmith.com/" target="_blank">
    <img src="https://img.shields.io/badge/LangSmith-E74C3C?style=for-the-badge&logo=github&logoColor=white" alt="LangSmith" height="30">
  </a>
  <a href="https://matplotlib.org/" target="_blank">
    <img src="https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white" alt="Matplotlib" height="30">
  </a>
  <a href="https://seaborn.pydata.org/" target="_blank">
    <img src="https://img.shields.io/badge/Seaborn-5c7da2?style=for-the-badge&logo=python&logoColor=white" alt="Seaborn" height="30">
  </a>
  <a href="https://pandas.pydata.org/" target="_blank">
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" height="30">
  </a>
</div>

## Turn your words into stunning data visuals, effortlessly! ✨

  <p align="center">
    <b>Intelligent extraction | Custom visualizations | Advanced analysis</b>
  </p>
</div>

# Overview

DataLens is an advanced agentic framework built on LangGraph that transforms natural language queries into data-driven visualizations. The system autonomously navigates the web using Tavily search and BeautifulSoup scraping to gather relevant information, then intelligently processes and visualizes this data through customized charts—all orchestrated by a sophisticated AI agent powered by OpenAI's models.

## Core Capabilities

- Smart workflow management using LangGraph and LangChain to coordinate different AI tasks
- Powered by OpenAI's GPT models to understand your requests and generate helpful responses
- Intelligent web scraping that can collect and organize data from websites
- Beautiful charts created with matplotlib and seaborn that you can customize
- Natural conversation interface to create and modify charts through simple text commands
- Comprehensive monitoring with LangSmith to track performance and troubleshoot issues

## Setup

1. Clone this repository
   ```bash
   git clone https://github.com/yourusername/DataLens.git
   cd DataLens
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up environment variables in a `.env` file:
   ```
   OPENAI_API_KEY=your_openai_api_key
   TAVILY_API_KEY=your_tavily_api_key
   LANGSMITH_TRACING=true
   LANGSMITH_ENDPOINT=https://api.smith.langchain.com
   LANGSMITH_API_KEY=your_langsmith_api_key
   LANGSMITH_PROJECT="chart-agent"
   ```
4. Run the main script: `test.ipynb`

## Usage

The main functionality is demonstrated in `test.ipynb`. The notebook illustrates how to:

1. Load and preprocess data
2. Generate charts based on the data
3. Ask questions about the charts and data
4. Use the agent to perform complex data analysis tasks

### Agents Overview

- **Supervisor Agent**: Supervises the research agent to ensure the output is relevant and sufficient for generating a chart. It evaluates the summary and reasoning from the research agent and decides whether to proceed with chart generation or request further information.

- **Research Agent**: Researches the web for information relevant to the user query. It utilizes web search and web scraping tools to gather data and passes the summary to the supervisor agent.

- **Chart Agent**: Generates charts based on the summary provided by the research agent. It uses a code generation tool to create the necessary code for chart creation, executes the code, and generates a chart description.

## Components

- **Data Processing**: Tools for loading, cleaning, and analyzing data
- **Chart Generation**: Functions to create various types of charts based on data
- **Agent**: LangGraph-based agent that can understand requests and utilize appropriate tools
- **Tools**: Custom tools for data manipulation, chart creation, and analysis

