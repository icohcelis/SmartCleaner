# SmartCleaner

SmartCleaner is an advanced junk file analyzer and cleaner for Windows, built with Python and Tkinter. It detects and removes outdated cache folders, broken shortcuts, and system junk files while offering a clean, modern UI with dark mode support.

## Features

- 🧹 Scans app-specific caches (Local/AppData)
- 🗑 Cleans Windows temp folders and Recycle Bin
- 🔗 Detects and deletes broken shortcuts
- 📁 Visual treeview with checkboxes and path/size info
- 🌘 Light/Dark theme toggle (with `sv-ttk`)
- ⚙️ Admin privilege elevation on launch
- 🧵 Multithreaded scanning for speed
- 🧠 Smart cache system to avoid redundant scans
- ❌ Graceful handling of locked files and in-use processes

## Installation

1. Install dependencies:

```bash
pip install winshell pywin32 psutil sv-ttk humanize
```
Run the script with Python 3.10+ on Windows: (Prefably 10+)

```python cac4.py```
🚨 Note: The app will re-launch itself with administrator rights automatically.
