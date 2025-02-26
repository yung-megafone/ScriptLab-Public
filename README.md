# ScriptLab

## Overview
ScriptLab is a collection of automation scripts designed to streamline workflows related to **file management, renaming, metadata handling, and system organization**. These scripts aim to enhance efficiency by automating repetitive tasks, handling metadata, and improving file organization.

## 📂 Project Structure
```
📂 ScriptLab/
├── 📂 Filesystem_Tools/
│   ├── 📂 Directory-Structure/
│   │   ├── 📂 pseudocode/
│   │   │   ├── 📄 T1_HighLevel_PC.md 
│   │   │   └── 📄 T2_Structured_PC.md 
│   │   ├── 📄 README.md 
│   │   └── 📄 dir-structure.py
│   ├── 📂 Metadata-Tools/
│   │   ├── 📂 Icon-Changer/
│   │   │   ├── 📂 pseudocode/
│   │   │   │   ├── 📄 T1_HighLevel_PC.md 
│   │   │   │   └── 📄 T2_Structured_PC.md 
│   │   │   ├── 📄 README.md 
│   │   │   └── 📄 icon-changer.py 
│   │   ├── 📂 Meta-Write/
│   │   │   ├── 📂 pseudocode/
│   │   │   │   ├── 📄 T1_HighLevel_PC.md 
│   │   │   │   └── 📄 T2_Structured_PC.md 
│   │   │   ├── 📄 README.md 
│   │   │   └── 📄 meta-write.py 
│   │   └── 📄 README.md 
│   ├── 📂 Renamers/
│   │   ├── 📂 checksum-file-renamer/
│   │   │   ├── 📂 pseudocode/
│   │   │   │   ├── 📄 T1_HighLevel_PC.md 
│   │   │   │   └── 📄 T2_Structured_PC.md 
│   │   │   ├── 📄 README.md 
│   │   │   └── 📄 checksum-rename.py 
│   │   └── 📂 music-renamer/
│   │       ├── 📂 pseudocode/
│   │       │   ├── 📄 T1_HighLevel_PC.md 
│   │       │   └── 📄 T2_Structured_PC.md 
│   │       ├── 📄 README.md 
│   │       └── 📄 music-renamer.py
│   └── 📄 README.md 
├── 📂 MediaDownload_Tools/
│   ├── 📂 yt-dlp-automation/
│   │   ├── 📂 pseudocode/
│   │   │   ├── 📄 T1_HighLevel_PC.md
│   │   │   └── 📄 T2_Structured_PC.md
│   │   ├── 📄 channels.txt
│   │   ├── 📄 README.md
│   │   ├── 📄 todo.txt
│   │   └── 📄 ytfetch.py
│   └── 📄 README.md
├── 📄 LICENSE 
├── 📄 README.md 
└── 📄 requirements.txt

```

## 🔹 Included Scripts
### **1️⃣ Directory Structure Generator**
📌 **Generates an ASCII directory tree of a folder and its subdirectories.**
- Supports file size display and JSON output.
- Allows excluding specific folders or file types.
- Includes progress tracking for large structures.

📍 **Usage:**
```bash
python dir-structure.py /path/to/folder --json
```

### **2️⃣ Icon Changer**
📌 **Assigns a custom folder icon to all subdirectories.**
- Supports Windows (`.ico` files).
- Includes recursive mode to process all subfolders.

📍 **Usage:**
```bash
python icon-changer.py /path/to/folders /path/to/icon.ico --recursive
```

### **3️⃣ Checksum File Renamer**
📌 **Renames files using their SHAKE-128 checksum.**
- Prevents duplicate files by ensuring unique names.
- Uses multithreading for fast processing.
- Includes a progress bar for better tracking.

📍 **Usage:**
```bash
python checksum-rename.py /path/to/files
```

### **4️⃣ Music File Renamer**
📌 **Renames music files based on metadata (ID3, FLAC, WAV tags).**
- Formats filenames as `01 - Artist - Song Title.mp3`.
- Supports recursive processing of subdirectories.
- Prevents overwriting and allows moving renamed files.

📍 **Usage:**
```bash
python music-renamer.py /path/to/music --copy
```

### **5️⃣ Metadata Writer (Filename to Metadata)**
📌 **Extracts structured information from filenames and writes it as embedded metadata.**
- Supports **MP3, FLAC, and WAV** formats.
- Parses filenames for **Track Number, Artist, Title, and Featured Artists**.
- Handles **inconsistent file naming conventions**.
- Uses **Mutagen** to modify metadata tags.
- Includes a **progress bar** for large collections.

📍 **Usage:**
```bash
python meta-write.py /path/to/music
```

### **6️⃣ ytfetch - YouTube Auto Downloader**
📌 **Automates YouTube video downloads, ensuring only new content is fetched.**
- Fetches new videos without redownloading old ones.
- Uses a text-based configuration file (`channels.txt`) for batch processing.
- Saves videos in user-specified folders based on creator names.
- Tracks downloaded content using `downloaded_videos.txt`.
- Supports scheduled execution via cron jobs or Task Scheduler.

## 🛠 Installation
To install dependencies, run:
```bash
pip install -r requirements.txt
```

## 📜 License
This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

## 🚀 Future Improvements
🔹 Add GUI support for script execution.  
🔹 Enhance error handling across all tools.  
🔹 Expand file format support for renaming and metadata extraction.  

For feature requests or contributions, feel free to open an **issue** or **pull request**! 🚀