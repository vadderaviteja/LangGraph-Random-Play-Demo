# 🎮 LangGraph Random Play Demo

A simple **LangGraph** project demonstrating how to build a state-based graph with conditional routing using Python. The flow starts from an initial node, randomly chooses between two game nodes (**Kabaddi** or **Kho-Kho**), and then ends execution.

This project is designed as a **beginner-friendly example** to understand:

* LangGraph basics
* State management using `TypedDict`
* Conditional edges with randomness
* Graph visualization using Mermaid

---

## 🧠 Project Overview

The graph flow works as follows:

1. **START** → `start_play`
2. `start_play` updates the state and decides the next node randomly
3. Based on randomness:

   * Goes to `kabbadi` **OR**
   * Goes to `kho_kho`
4. The selected node updates the state
5. **END**

Each node appends information to a shared state variable called `graph_info`.

---

## 🗂️ Project Structure

```
langgraph-random-play/
│
├── main.py              # Main LangGraph implementation
├── README.md            # Project documentation
├── requirements.txt     # Required dependencies
```

---

## 🧪 Example Output

Input:

```python
entire_graph.invoke({"graph_info": "My name is Raviteja"})
```

Possible Outputs:

* `My name is Raviteja, I am planning to play kabbadi`
* `My name is Raviteja, I am planning to play kho_kho`

(The result changes because the path is chosen randomly.)

---

## 📦 Requirements

Create a `requirements.txt` file with the following content:

```
langgraph
ipython
typing-extensions
```

> ⚠️ **Note:**
>
> * Python version **3.9+** is recommended
> * `random` and `typing` are part of Python's standard library

---

## 🚀 Installation & Setup

1. **Clone the repository**

```bash
git clone https://github.com/vadderaviteja/LangGraph-Random-Play-Demo
cd langgraph-random-play
```

2. **Create and activate a virtual environment (optional but recommended)**

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run

```bash
python main.py
```

Or invoke the graph inside a Python shell or notebook:

```python
entire_graph.invoke({'graph_info': 'My name is Raviteja'})
```

---

## 📊 Graph Visualization

The project uses **Mermaid diagrams** to visualize the graph structure:

```python
display(Image(entire_graph.get_graph().draw_mermaid_png()))
```

This helps in understanding node connections and execution flow clearly.

---

## 🛠️ Technologies Used

* **Python**
* **LangGraph**
* **TypedDict** for state definition
* **Mermaid** for graph visualization

---

## 🎯 Learning Objectives

* Understand state-driven workflows
* Learn conditional routing in LangGraph
* Visualize execution graphs
* Build foundations for **Agentic AI / GenAI workflows**

---

