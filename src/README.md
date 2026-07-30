# 🛠️ Disassembly Wizard — Desktop GUI (`app.py`)

An intuitive, modern desktop GUI built with **CustomTkinter**. It serves as the main integration bridge for the **Disassembly Wizard** project, connecting input JSON models with Rubin's core loader and driving exporters (Word, HTML+JS, PowerPoint, Markdown, PDF).

---

## ⚡ Quick Start (TL;DR)

Run these commands directly in your terminal from the root/src directory:

```bash
# 1. Go to src directory
cd src

# 2. Install dependencies
pip install customtkinter pillow python-docx python-pptx opencv-python numpy

# 3. Run the application
python3 app.py 
📋 Prerequisites 
Python Version: Python 3.10 or higher recommended.

Linux/Ubuntu Users Note: Tkinter is not bundled by default on some Linux distributions. Run this once before launching:

Bash
sudo apt update && sudo apt install -y python3-tk
💻 Step-by-Step Setup Guide
Step 1: Navigate to the Source Folder
Open your terminal or command prompt and switch to the project's src folder:

Bash
cd path/to/s26-std-03/src
Step 2: Set Up a Virtual Environment (Recommended)
To prevent dependency conflicts with system packages, create and activate a clean environment:

Linux / macOS:

Bash
python3 -m venv venv
source venv/bin/activate
Windows:

Bash
python -m venv venv
.\venv\Scripts\activate
Step 3: Install Required Libraries
Install the core GUI library and output module requirements:

Bash
pip install --upgrade pip
pip install customtkinter pillow python-docx python-pptx opencv-python numpy
Step 4: Launch the GUI
Run the main script:

Bash
python3 app.py
✨ Key Features & Capabilities
Automatic Path Resolution (sys.path): Dynamically scans src/, src/main/, and subdirectories so teammate exporter modules are discovered regardless of execution directory.

Dynamic Graph Inspection: Automatically scans target JSON files to detect disassembly tree depth levels.

Multi-Format Export Support: One-click integration for:

📄 Word Documents (.docx)

🌐 Interactive HTML + JS

📊 PowerPoint Presentations (.pptx)

📝 Markdown Files (.md)

Real-Time Telemetry Log: Integrated execution log window that surfaces structural warnings, path diagnostics, and error reporting live.  

🛠️ Troubleshooting 
Issue,                     Cause,                                     Quick Fix
ModuleNotFoundError: | No module named '_tkinter',Missing Tkinter on Linux,Run sudo apt install python3-tk
Exporter module missing in logs |,Exporter file not in path,Ensure files are inside src/ or src/main/
customtkinter rendering issues |,Outdated pip or missing Pillow,Run pip install --upgrade customtkinter pillow
