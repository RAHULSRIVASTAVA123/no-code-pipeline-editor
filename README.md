# no-code-pipeline-editor
A no-code pipeline builder inspired by VectorShift, featuring dynamic nodes, template-based Text nodes, DAG validation, and undo/redo support.



A no-code, DAG-based pipeline editor inspired by VectorShift.  
Built with **React Flow**, **Zustand**, and **FastAPI**, this project allows users to visually construct pipelines, define dynamic text templates, and validate graph correctness.

---

##  Features

###  Visual Pipeline Builder
- Drag-and-drop node-based editor
- Connect nodes using directed edges
- Snap-to-grid canvas with diagram-style background

###  Node Types
- **Input** – Entry point for data
- **LLM** – Represents a language model step
- **Output** – Final pipeline output
- **Text** – Template-based text node with variables
- **Number, Delay, Merge, Logger, Condition** – Additional nodes demonstrating scalability

###  Text Node Logic (Part 3)
- Auto-resizing text area (node grows with content)
- Supports template variables using `{{variable}}` syntax
- Each variable dynamically creates an input handle
- Prevents duplicate handles for the same variable

###  Graph Validation
- Pipeline submitted to backend for analysis
- Backend checks:
  - Number of nodes
  - Number of edges
  - Whether the graph is a valid **DAG (Directed Acyclic Graph)**

###  Productivity Features
- **Delete nodes / edges** using `Delete` or `Backspace`
- **Undo / Redo**
  - `Ctrl + Z` → Undo
  - `Ctrl + Shift + Z` / `Ctrl + Y` → Redo

###  UI & UX Polish
- Clean, neutral UI inspired by professional diagram tools
- Dotted canvas background for spatial clarity
- Rounded buttons and modal-based pipeline summary

---

##  Tech Stack

### Frontend
- **React**
- **React Flow**
- **Zustand** (state management)

### Backend
- **FastAPI**
- Python



