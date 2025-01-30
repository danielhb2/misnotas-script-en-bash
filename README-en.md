# bash Note Manager
### Author: Daniel Horacio Braga - AI
## Description
This script is a simple but powerful notes that allows you to create, edit and organize daily notes from the command line. The notes are automatically organized in directories per year and are appointed according to the creation date.  
Base created by IA, adjustments and modifications made by DHB

## Characteristics
- Interactive interface with navigation using keyboard arrows
- Automatic notes organization per year
- Two types of notes per day:
  - Main note (.txt)
  - Annexes (.anexo)
- Text search in all notes
- Content preview
- Content edition and aggregate
- Interactive confirmation for critical operations

# Dependencies
The script requires the following tools:

### required
- `Bash`: Shell in which the script runs
- `fzf`: For interactive interface and file selection
- `nano`: Default text editor
- `cat`: to visualize content (if BAT is not installed)
- `grep`: For text search
- `find`: To list files
- `date`: To handle dates

### Optional
- `bat`: Improved alternative to cat (provides Syntax Highlighting)

## Installation

1. Install the necessary units:

In Ubuntu/Debian:
```bash
Sudo apt install fzf nano bat
```

In Fedora:
```bash
sudo dnf install fzf nano bat
```

In Arch Linux:
```bash
sudo pacman -S fzf nano bat
```

2. Do the executable script:
```bash
chmod +x misnotas
```

## Usage

### Start the program
```bash
misnotas
```

### Director Structure
The script creates and maintains the following structure:
```
~/mis_notas/
├── 2024/
│   ├── 28-01-2024.txt
│   └── 28-01-2024.anexo
├── 2025/
└── ...
```

### Operations available
1. **New note**: Create a main note for the current day
2. **NEW ANNEXA Note**: Create an attached note for the current day
3. **Edit note**: Select and edit an existing note
4. **Preview notes**: See the content of a note
5. **Add content**: Add text to an existing note
6. **Remove note**: Delete a selected note
7. **Search text**: Search text in all notes

### Navigation
- Use arrows ↑/↓ to move between options
- Enter to select
- ESC to cancel/return
- / To search in file lists

## Personalization

The script uses the following default applications:
- Editor: Nano
- Viewer: Bat (or Cat if Bat is not installed)

You can modify the main directory editing the variable NOTES_DIR
```bash
NOTAS_DIR="your_directory"
```
To change the editor, modify the EDITOR variable at the beginning of the script:
```bash
EDITOR="nano"  # Change to vim, emacs, etc.
```

## Notes and considerations
- The notes are saved in flat text
- A directory is automatically created for each year
- Only a main note and an annexed per day are allowed
-The files are automatically named with the DD-MM-YYYY format (Maybe you must adjust the date format, according to your locale settings)



