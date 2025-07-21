# 🚀 Quick-Start Guide — Deep Research Agent

### 1. What It Is  
An AI-powered assistant (Gemini API) that runs multi-layer research and outputs a fully cited `final_report.md`.

### 2. One-Minute Run  
```bash
# prerequisites: Python 3.9+, a Gemini API key
export GEMINI_KEY=your_api_key_here
pip install -r requirements.txt
python main.py "your research question"
```

#### Optional flags  
* `--mode` `fast|balanced|comprehensive` (default `balanced`)  
* `--num-queries` `<int>` number of search queries (default 3)  
* `--learnings` `"<previous finding 1>" "<finding 2>" …`  

#### Research Modes & Their Purpose  

| Mode | Represents | Best For |
|------|------------|----------|
| **fast** | Quick, surface-level scan (minimal depth & breadth) | Rapid fact-finding, time-sensitive checks, initial exploration |
| **balanced** *(default)* | Moderate depth and breadth without recursion | General research tasks where you need solid coverage but not an exhaustive dive |
| **comprehensive** | Exhaustive, multi-layer exploration with recursive sub-queries | Academic papers, detailed analyses, or any topic requiring full 360-degree coverage |

Example:  
```bash
python main.py "Impact of AI on healthcare" --mode comprehensive --num-queries 5
```

### 3. What You Get  
* Interactive follow-up questions for clarity  
* Concurrent web searches with breadth & depth control  
* A richly formatted, ~3 000-word report saved as `final_report.md`  
* All sources tracked & deduplicated  
* Progress logged; research tree saved to `research_tree.json`

### 4. Project At-a-Glance
```
open-gemini-deep-research/
├─ main.py               # CLI entry point
├─ src/deep_research.py  # core research engine
└─ requirements.txt
```

That’s everything you need to install, run, and understand the Deep Research Agent—concise, complete, and ready to explore.
