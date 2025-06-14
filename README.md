# SmartCleaner

[![License: MIT]()](https://opensource.org/licenses/MIT)
[![Python: 3.9+]()](https://www.python.org/downloads/)
[![Platform: Windows]()](https://www.microsoft.com/windows)

Smart Cleaner Ultimate is a powerful and safe disk cleanup tool designed to find and remove gigabytes of junk files from your Windows system. It features an intelligent scanning engine, a modern and responsive user interface, and a strong focus on performance and safety.

## ✨ Key Features

*   🚀 **Blazing Fast Scans:** Utilizes a multi-threaded architecture to scan multiple locations in parallel, making full use of modern CPUs and SSDs.
*   🧠 **Intelligent Application Cache Scanner:** Safely finds junk files *inside* application directories (e.g., Discord, Chrome, Spotify) without incorrectly flagging the entire program folder as junk.
*   🎨 **Modern Themed GUI:** A clean and responsive interface built with `sv-ttk`, featuring a toggleable Windows 11-style dark mode. Your theme choice is saved automatically.
*   🎯 **Comprehensive Cleaning:** Targets a wide range of junk:
    *   Application Caches (for hundreds of programs)
    *   Windows System Temp & Prefetch
    *   Recycle Bin
    *   Broken Shortcuts on the Desktop and in the Start Menu
*   🔒 **"Kill & Delete" for Locked Files:** If a file is in use, the application identifies the locking process and asks for permission to terminate it, allowing for a more thorough cleaning.
*   🖱️ **Advanced UI Controls:** Includes full support for **Shift + Click** to select a range of items and an enhanced right-click context menu for quick actions.
*   🕒 **Time-Based Filtering:** Focus your cleaning on files that haven't been touched in over 30 days, 90 days, or a year.

## 🛠️ Getting Started

Follow these steps to get the application running on your local machine.

### Prerequisites

*   Python 3.9 or newer
*   Windows 10 or 11

### Installation & Running

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Luc6i/SmartCleaner.git
    cd smartCleaner
    ```

2.  **Install the required libraries:**
    ```bash
    pip install humanize winshell pywin32 psutil sv-ttk
    ```

3.  **Run the application:**
    The script will automatically request administrator privileges to perform a deep system scan.
    ```bash
    python cac4.py
    ```

## ⚙️ How It Works

The power of Smart Cleaner Ultimate comes from its intelligent and safe scanning logic:

*   **Parallel Processing:** The main scan manager uses a `ThreadPoolExecutor` to launch multiple scan tasks at once (Application Caches, System Files, Shortcuts). This drastically reduces the total analysis time.
*   **Safe Application Scanning:** Instead of using a flawed "leftover" detection model, the `scan_application_data` function iterates through top-level application folders in `%APPDATA%` and `%LOCALAPPDATA%`. It then performs a targeted, recursive search *within* these folders for common cache and log directory names. This ensures that only true junk folders are flagged, leaving the core application files untouched.
*   **Safety Blacklist:** A hardcoded blacklist prevents the scanner from ever analyzing critical system folders like `Microsoft` or `Programs`, adding an extra layer of protection against false positives.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/Luc6i/SmartCleaner/issues).

1.  **Fork** the project.
2.  Create your **Feature Branch** (`git checkout -b feature/AmazingFeature`).
3.  **Commit** your changes (`git commit -m 'Add some AmazingFeature'`).
4.  **Push** to the branch (`git push origin feature/AmazingFeature`).
5.  Open a **Pull Request**.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
