# 🧠 Multi-Agent Debate DAG using LangGraph

This project is a technical assignment for ATG's Machine Learning Internship. It simulates a structured 8-round debate between two AI agents — a Scientist and a Philosopher — over a user-supplied topic.

---

## ⚙️ Features

- Two alternating agents using LangGraph nodes
- Memory accumulation using Annotated List
- Judge node decides the winner based on transcript
- Clean CLI input and Jupyter Notebook integration

---

## 📂 Project Structure
```
multi-agent-debate-dag/
│
├── debate.ipynb # Run this to simulate the full debate
├── README.md
│
├── setup/
│ └── setup_import.py
│
├── nodes/
│ ├── user_input.py
│ ├── agent_a.py
│ ├── agent_b.py
│ ├── memory.py
│ └── judge.py



# 🚀 How to Run

### Option 1: Jupyter Notebook
1. Open `debate.ipynb`
2. Run all cells
3. Enter a debate topic when prompted

### Option 2: Python Script
You can refactor the notebook into a single `.py` script if needed.

---

## 🧠 Sample Output

Enter the debate topic: Should AI be regulated like medicine?

[Round 1] Scientist: AI must be regulated for safety.
[Round 2] Philosopher: Overregulation limits innovation.
...
[Judge] Winner: Scientist
Reason: Scientist highlighted risks and public safety.

---

## 🛠️ Requirements

Install dependencies:

```bash
pip install langgraph langchain openai graphviz


```
## 📬 Author
Shaivik Shende
Machine Learning Intern Candidate – ATG


---

### ✅ Next Step: Upload to GitHub

1. Unzip the [📦 ZIP file](sandbox:/mnt/data/multi_agent_debate_dag_fixed_final.zip)
2. Run these commands in terminal:


```bash
cd multi-agent-debate-dag
git init
git remote add origin https://github.com/your-username/multi-agent-debate-dag.git
git add .
git commit -m "Initial commit: Multi-Agent Debate DAG"
git push -u origin master

```
## 🐍 Optional Python Version of the Notebook (main.py)
If you prefer to run it as a CLI script instead of Jupyter:
```bash
# main.py

from setup.setup_import import initialize_graph

# Build and compile graph
graph = initialize_graph()
app = graph.compile()

# Run the graph
final_state = app.invoke({
    "topic": input("Enter the debate topic: ") or "Should AI be regulated like medicine?",
    "round": 1,
    "memory": [],
    "last_speaker": ""
})

# Show results
print("\n🧠 Final Debate Transcript:\n")
for line in final_state["memory"]:
    print(line)
```


## ✅ .gitignore file (to exclude junk when uploading)

# Jupyter Notebook checkpoints
.ipynb_checkpoints/

# Python cache
__pycache__/
*.pyc

# VSCode settings
.vscode/

# OS files
.DS_Store
Thumbs.db

# Environment files
.env
*.env


## 📦 Final Folder Layout (after adding these):
```
multi-agent-debate-dag/
├── debate.ipynb
├── main.py
├── README.md
├── .gitignore
│
├── setup/
│   └── setup_import.py
│
├── nodes/
│   ├── user_input.py
│   ├── agent_a.py
│   ├── agent_b.py
│   ├── memory.py
│   └── judge.py
```
