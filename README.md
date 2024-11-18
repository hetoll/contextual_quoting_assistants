# Dynamic Quoting System for Complex Products Using Multi-Agent AI Architecture

## Overview
This project implements a sophisticated multi-agent system for generating personalized, context-aware quotes for complex products and services. It leverages LangChain/LangGraph to create an intelligent quoting workflow that incorporates:

- **Retrieval-Augmented Generation (RAG)** for context-sensitive data retrieval
- **Multi-Agent Architecture** with specialized roles
- **Intelligent Classification** using sentiment analysis
- **Dynamic Workflow Management** through a state graph system
- **Database Integration** for storing category rates

## Prerequisites

### Required Python Packages

pip install langgraph
pip install langchain-core
pip install langchain-openai
pip install langchain-groq
pip install langchain-community
pip install python-dotenv
pip install pydantic
pip install typing-extensions
pip install chromadb
pip install langchain-text-splitters

### Environment Variables
Create a `.env` file with the following:

OPENAI_API_KEY=your_openai_key
LANGCHAIN_API_KEY=your_langchain_key
GROQ_API_KEY=your_groq_key
LANGCHAIN_TRACING_V2=optional
LANGCHAIN_PROJECT=optional


## Project Structure

### Core Components

1. **Database Setup**
   - SQLite database for category rates
   - Predefined categories with associated rates
   - Automated table creation and data population

2. **Assistants**
   - **Main Assistant**: Guides users through information gathering
   - **Underwriting Assistant**: Evaluates risk and validates categories
   - **Quote Assistant**: Calculates and presents final premiums

3. **Agents**
   - **Retriever Agent**: Extracts and summarizes business operations
   - **Reasoning Agent**: Determines relevant insurance categories
   - **Classification Grading Agent**: Evaluates category assignments
   - **Quote Generation Agent**: Calculates final premiums

4. **State Management**
   - MainState: Core workflow state
   - RAGState: Retrieval state
   - ExtraState: Additional workflow data

5. **Routing Nodes**
   - `route_main_assistant`: Manages main assistant flow
   - `route_underwriting_assistant`: Handles underwriting transitions
   - `route_quote_assistant`: Controls quote generation flow
   - `route_to_workflow`: Determines assistant routing
   - Additional utility nodes for state updates and message handling

## Usage

### Running the System
1. Open the Jupyter notebook (`contextual_quoting_agentic_system.ipynb`)
2. Run all cells in sequence
3. The system will prompt you for input when ready
4. Type your questions/responses when prompted
5. Type '/exit' to end the session

## Key Features

### 1. Dynamic Category Classification
- Intelligent matching of business descriptions to categories
- Grade-based evaluation of category relevance
- Contextual understanding of business operations

### 2. Automated Quote Generation
- Revenue-based premium calculation
- Multi-category rate application
- Dynamic rate adjustment based on business complexity

### 3. Workflow Management
- State-based conversation flow
- Error handling and fallback mechanisms
- Conditional routing between assistants

## Contact
Hector -> hector@hetoll.com
