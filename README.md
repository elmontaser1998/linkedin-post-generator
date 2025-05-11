# 🤖 CrewAI LinkedIn Post Generator

![image](https://github.com/user-attachments/assets/0fd29963-56f7-42bc-b94c-e34d91a568eb)


This project leverages CrewAI to automate the creation of engaging LinkedIn posts using intelligent agents. It uses LLMs (via Groq's LLaMA 3) and tools such as Tavily Search to research a topic, find relevant videos, and generate a professional LinkedIn post ready for publishing.
 
### Features
- Topic research via Tavily
- YouTube video recommendations
- LinkedIn post generation with formatting, emojis, and hashtags
- Multi-agent collaboration (Researcher, Video Finder, Writer)
- Powered by CrewAI, LangChain, and Groq
  
  <p align="center"> 
   <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" /> 
   <img src="https://img.shields.io/badge/CrewAI-4C1C1C?style=for-the-badge&logo=crewAI;base64,&logoColor=white" /> 
   <img src="https://img.shields.io/badge/LangChain-000000?style=for-the-badge&logo=LangChain&logoColor=white" /> 
   <img src="https://img.shields.io/badge/Groq-blueviolet?style=for-the-badge&logo=groq&logoColor=white" /> 
   <img src="https://img.shields.io/badge/HuggingFace-FFBF00?style=for-the-badge&logo=huggingface&logoColor=black" /> 
   <img src="https://img.shields.io/badge/Tavily-3F3F3F?style=for-the-badge&logo=google&logoColor=white" /> </p>

###  Quick Start
1. Install dependencies
```bash
pip install crewai crewai-tools
pip install langchain-groq
```
2. Set up API Keys (Environment Variables)
Before running the script, set your API keys:

```bash

export TAVILY_API_KEY="your_tavily_api_key"
export HUGGINGFACE_API_KEY="your_huggingface_key"
export GROQ_API_KEY="your_groq_api_key"
```
Or add them directly in the script for testing (not recommended for production):

```python
os.environ["TAVILY_API_KEY"] = "..."
os.environ["HUGGINGFACE_API_KEY"] = "..."
os.environ["GROQ_API_KEY"] = "..."
```
### How It Works
The application follows a multi-agent pipeline:

1. Researcher Agent: Uses Tavily API to research a topic.

2. Video Agent: Finds relevant YouTube videos using Tavily.

3. Content Writer Agent: Writes a polished LinkedIn post from research findings and videos.

Agents communicate and share data using CrewAI’s Task and Crew architecture.

### Future Enhancements
- Web interface via Streamlit 
- Support for automatic LinkedIn posting via API
- Add a Validation Agent to review and approve the generated LinkedIn post before publishing
- Add an Image Generation Agent to create contextual visuals for the post (e.g. via DALL·E, SDXL, etc.)
- Run the application locally with Ollama, using lightweight LLMs (e.g. llama3) for privacy and offline compatibility
