# Python Mini AI Agent

**🚀 Live Demo:** [Try the Mini AI Agent](https://python-mini-ai-agent-rwkwdd7fjvalx56cnohbgq.streamlit.app/)

A beginner-friendly Python project that demonstrates simple tool routing: read a user request, identify the intended tool, and execute the matching Python function.

## Features

- Calculator tool for basic addition.
- DuckDuckGo web search integration.
- Email tool demonstration (simulation only; it does not send email).
- Keyword/condition-based tool routing.

## Technology

Python · Regular Expressions · DuckDuckGo Search · Streamlit

## How it works

1. The user enters a request.
2. The program checks the request against supported keywords and conditions.
3. The matching tool function runs.
4. The tool output is displayed.

## Run locally

```bash
git clone https://github.com/sai-manikanta-kadali/mini-ai-agent.git
cd mini-ai-agent
pip install -r requirements.txt
streamlit run app.py
```

Check the repository for the current application entry point and dependency file. If the project is run from a notebook, open the notebook in Google Colab instead.

## Limitations

- Tool routing is keyword-based; it is not an LLM planner.
- The email tool is a simulation and does not send real messages.
- The calculator currently demonstrates addition only.
- This is a beginner learning project, not a production autonomous agent.

---

A first hands-on step toward understanding Python tools and agent-style workflows.