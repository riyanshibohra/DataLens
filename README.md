<div align="center">

# VisualizeAI: The Intelligent Chart Generator

This project implements an AI agent that can generate and analyze charts based on data. The agent utilizes OpenAI's model APIs, LangGraph, and various tools to process data, create visualizations, and answer questions about the data.

</div>

<div align="center" style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center">
  <img src="https://img.shields.io/badge/-LangGraph-blue" alt="LangGraph" height="25">
  <img src="https://img.shields.io/badge/-LangChain-green" alt="LangChain" height="25">
  <img src="https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white" alt="Python" height="25">
  <img src="https://img.shields.io/badge/-OpenAI%20API-412991?logo=openai&logoColor=white" alt="OpenAI" height="25">
  <img src="https://img.shields.io/badge/-BeautifulSoup-orange" alt="BeautifulSoup" height="25">
  <img src="https://img.shields.io/badge/-PythonREPL-yellow" alt="PythonREPL" height="25">
  <img src="https://img.shields.io/badge/-Matplotlib-11557c" alt="Matplotlib" height="25">
  <img src="https://img.shields.io/badge/-Seaborn-5c7da2" alt="Seaborn" height="25">
  <img src="https://img.shields.io/badge/-Pandas-150458?logo=pandas&logoColor=white" alt="Pandas" height="25">
  <img src="https://img.shields.io/badge/-Tavily-purple" alt="Tavily" height="25">
  <img src="https://img.shields.io/badge/-LangSmith-red" alt="LangSmith" height="25">
</div>

## Core Capabilities

- Smart workflow management using LangGraph and LangChain to coordinate different AI tasks
- Powered by OpenAI's GPT models to understand your requests and generate helpful responses
- Intelligent web scraping that can collect and organize data from websites
- Beautiful charts created with matplotlib and seaborn that you can customize
- Natural conversation interface to create and modify charts through simple text commands
- Comprehensive monitoring with LangSmith to track performance and troubleshoot issues

## Setup

1. Clone this repository
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

