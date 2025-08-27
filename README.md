# LLM Smart Assistant

This project implements a **multi-level smart assistant** using Python and Large Language Models (LLMs).  
It progressively builds from a simple chatbot to a fully agentic AI with tool usage and memory.  



## Project Structure

LLM_Smart_Assistant/
├── README.md # Overall project documentation 
├── .env # API keys
├── Level1/
│ ├── chatbot.py 
│ ├── README.md # Level 1 instructions
│ └── interactions.log
├── Level2/
│ ├── chatbot_with_tool.py 
│ ├── calculator_tool.py # Basic arithmetic tool
│ ├── README.md # Level 2 instructions
│ └── interactions_level2.log
├── Level3/
│ ├── full_agent.py 
│ ├── calculator_tool.py 
│ ├── translator_tool.py 
│ ├── README.md # Level 3 instructions
│ └── interactions_level3.log




## Levels Overview

### Level 1 — Basic Chatbot
- Uses an LLM (OpenAI/Gemini) to answer user queries.
- Input: Free text query.  
- Output: LLM-generated response.  
- **File:** `Level1/chatbot.py`  

### Level 2 — Tool-Augmented Chatbot
- Extends Level 1 by integrating a **calculator tool**.  
- Detects arithmetic tasks (e.g., “add 10 and 20”).  
- Routes such tasks to `calculator_tool.py`, else defaults to LLM.  
- **File:** `Level2/chatbot_with_tool.py`  

### Level 3 — Full Agent
- Fully agentic AI with **multi-step reasoning**.  
- Breaks complex queries into sub-tasks.  
- Can call multiple tools (`calculator_tool.py`, `translator_tool.py`).  
- Maintains simple memory across steps.  
- Example:  
  > “Translate 'Good Morning' into German and then multiply 5 and 6.”  
  - Step 1 → Translation (`Good Morning → Guten Morgen`)  
  - Step 2 → Multiplication (`5 × 6 = 30`)  
- **File:** `Level3/full_agent.py`  



## Setup & Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/preethi-2005/LLM_Agentic_Thinking.git
   cd LLM_Agentic_Thinking



# LLM Smart Assistant

## Setup

### 1. Create virtual environment
```bash
python -m venv .venv
source .venv/bin/activate   # Mac/Linux
.venv\Scripts\activate      # Windows
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add your API keys to `.env`

OPENAI_API_KEY=your_api_key_here

GEMINI_API_KEY=your_gemini_key_here (If you are using Gemini Api and modify the code accordingly)


## 🚀 Running the Project

### Run Level 1
```bash
python Level1/chatbot.py "What is the capital of France?"
```

### Run Level 2
```bash
python Level2/chatbot_with_tool.py "Add 12 and 30"
```

### Run Level 3
```bash
python Level3/full_agent.py "Translate 'Good Morning' into German and then multiply 5 and 6."
```



## 📝 Logs
Each level stores logs of all interactions inside interactions.log files.  

**Example:**  
```
Level1/interactions.log
```


## 👩‍💻 Contributor
**Gayathri**  
mail: 245122733098@mvsrec.edu.in 

---

