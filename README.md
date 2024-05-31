# Summarization App Using LangChain and OpenAI

This project demonstrates how to build a summarization application using LangChain and OpenAI's GPT-3.5-turbo model. It covers basic prompt-based summarization, prompt templates, and advanced summarization techniques using `map_reduce` and `refine` chains.

## Prerequisites

Before running the code, ensure you have the following installed:

- Python 3.8+
- Required libraries as specified in `requirements.txt`

## Setup

1. Clone this repository or download the project files.

2. Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Create a `.env` file in the project root directory and add your OpenAI API key:
    ```plaintext
    OPENAI_API_KEY=your_openai_api_key
    ```

## Libraries Used

- `os`
- `dotenv`
- `openai`
- `langchain`
- `wikipedia`
- `pdf2image`
- `pdfminer`

## Project Structure

- `project_summarization.ipynb`: Main notebook with code for various summarization techniques using LangChain and OpenAI.
- `requirements.txt`: Lists all the dependencies needed for the project.

## Steps to Run the Project

1. **Basic Prompt**

   Use a basic prompt to summarize a given text.

    ```python
    from langchain_openai import ChatOpenAI
    from langchain.schema import AIMessage, HumanMessage, SystemMessage
    ```

2. **Summarizing Using Prompt Templates**

   Create prompt templates to generate concise summaries and translate them into different languages.

    ```python
    from langchain import PromptTemplate
    from langchain.chains import LLMChain
    ```

3. **Summarizing using SuffDocumentChain**

   Summarize a document using the `SuffDocumentChain`.

    ```python
    from langchain.chains.summarize import load_summarize_chain
    from langchain.docstore.document import Document
    ```

4. **Summarizing Large Documents Using map_reduce**

   Summarize large documents by splitting them into chunks and using the `map_reduce` chain.

    ```python
    from langchain.text_splitter import RecursiveCharacterTextSplitter
    ```

5. **map_reduce with Custom Prompts**

   Customize the prompts used in the `map_reduce` summarization chain.

    ```python
    from langchain import PromptTemplate
    ```

6. **Summarizing Using the refine Chain**

   Use the `refine` chain to progressively refine and improve the summary.

    ```python
    from langchain.chains.summarize import load_summarize_chain
    ```

7. **refine with Custom Prompts**

   Customize the initial and refine prompts in the `refine` chain.

    ```python
    from langchain import PromptTemplate
    ```

8. **Summarizing Using LangChain Agents**

   Use LangChain agents to perform summarization by integrating with external tools like Wikipedia.

    ```python
    from langchain.agents import initialize_agent, Tool
    from langchain.utilities import WikipediaAPIWrapper
    ```

## Running the Code

1. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

2. Create a `.env` file and add your OpenAI API key:
    ```plaintext
    OPENAI_API_KEY=your_openai_api_key
    ```

3. Run the Jupyter notebook `project_summarization.ipynb` to execute the code cells and observe the summarization techniques.

## Author

Sarveshmani Tiwari

