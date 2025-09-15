🧠 AI Research Agent

An AI-powered research assistant built using LangChain
, Anthropic Claude
, and OpenAI
.
The agent can search the web, query Wikipedia, and save research results into structured text files for later use.

✨ Features

🌐 Web Search – Powered by DuckDuckGo

📚 Wikipedia Lookup – Fetch concise summaries from Wikipedia

💾 Save to File – Automatically saves research results with timestamps

🧾 Structured Responses – Returns results in a well-defined JSON format

🔧 Tool-Calling Agent – Dynamically selects and invokes the right tools

📂 Project Structure
.
├── tools.py              # Defines search, Wikipedia, and save-to-file tools
├── main.py              # Core AI Agent logic
├── research_output.txt   # Stores saved research results
├── key.env                  # Environment variables (API keys)
└── README.md             # Project documentation

⚙️ Installation
1. Clone the repository
git clone (https://github.com/23f2002469/Ai_Agent.git)
cd Ai_Agent

2. Create and activate virtual environment
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

3. Install dependencies
pip install -r requirements.txt

🔑 Environment Variables

Create a .env file in the project root and add your API keys:

OPENAI_API_KEY=your_openai_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key

🚀 Usage

Run the agent:

python main.py


You’ll be prompted:

What can i help you research? 


Example:

What can i help you research? The impact of AI on healthcare


The agent will:

Search the web / Wikipedia for relevant data

Generate a structured summary

Save results to research_output.txt

🛠 Tools Overview

search → Web search via DuckDuckGo

wiki_tool → Wikipedia summaries

save_tool → Append structured research output into research_output.txt

📊 Example Output
{
  "topic": "The impact of AI on healthcare",
  "summary": "AI is transforming healthcare by enabling predictive analytics, improving diagnostics, and enhancing personalized medicine...",
  "sources": [
    "https://en.wikipedia.org/wiki/Artificial_intelligence_in_healthcare",
    "https://www.healthit.gov/"
  ],
  "tools_used": ["search", "wiki_tool", "save_tool"]
}

🧩 Tech Stack

LangChain
 – Agent framework

Anthropic Claude
 – LLM backend

DuckDuckGo Search API
 – Web search

Wikipedia API
 – Wiki data

Python 3.9+

🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.
