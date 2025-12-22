# 1. Terminal Basics Guide

## 🔰 BEGINNER LEVEL

### Understanding the Terminal Basics

- [ ] Use `-h` or `--help` when unsure about a command

---

## Essential Navigation Commands

#### 1. `pwd` - Print Working Directory (Where am I?)
```
pwd                               # Shows full path of current folder
```
**Output example**: `/Users/yourname/Documents/my-project`
**When to use**: When lost, to see your current location
**What it shows**: Your absolute path from the root of your computer

---

#### 2. `ls` - List files and folders (What's here?)
```
ls                                # List all files and folders
ls -l                             # Long format (detailed info)
ls -a                             # Show hidden files (start with .)
ls -la                            # Show all files in detail
ls -lh                            # Long format with human-readable sizes
ls <folder-path>                  # List contents of specific folder
ls /Users/yourname/Documents      # List a specific folder's contents
ls -h                             # View all options
```
**Output example**:
```
Desktop    Documents    Downloads    Pictures    .bashrc
```
**When to use**: To see what files/folders are in current location
**Color coding**: Folders are blue, files are white, executable files are green

---

#### 3. `cd` - Change Directory (Move to folder)
```
cd <folder-name>                  # Go into a folder
cd Documents                      # Enter Documents folder
cd Desktop/my-project             # Enter nested folders
cd ..                             # Go up one level (parent folder)
cd ../..                          # Go up two levels
cd ~                              # Go to home folder (shortcut)
cd /                              # Go to root (top of computer)
cd -                              # Go back to previous folder
cd /absolute/path/to/folder       # Use full path
cd -h                             # View help
```
**When to use**: To navigate into different folders
**Examples**:
- `cd Documents` - Enter Documents
- `cd ..` - Go back to parent folder
- `cd ~/Projects` - Go to Projects folder in home directory

---

#### 4. `mkdir` - Make Directory (Create folder)
```
mkdir <folder-name>               # Create a new folder
mkdir my-project                  # Create folder named "my-project"
mkdir folder1 folder2             # Create multiple folders at once
mkdir -p path/to/nested/folder    # Create nested folders (parent folders too)
mkdir -v <folder-name>            # Verbose (shows what it's doing)
mkdir -h                          # View help
```
**When to use**: When you need to create a new folder
**Examples**:
- `mkdir my-project` - Creates folder "my-project"
- `mkdir -p src/components` - Creates "src" then "components" inside it

---

#### 5. `touch` - Create empty file
```
touch <filename>                  # Create empty file
touch index.html                  # Create file named "index.html"
touch file1.txt file2.txt         # Create multiple files
touch -h                          # View help
```
**When to use**: Creating blank files quickly
**Examples**:
- `touch README.md` - Create blank README.md
- `touch index.html style.css` - Create two files at once

---

#### 6. `cat` - View file contents (Read file)
```
cat <filename>                    # Display file contents
cat index.html                    # Show what's in index.html
cat file1.txt file2.txt           # Display multiple files
cat -n <filename>                 # Show line numbers
cat -h                            # View help
```
**When to use**: To quickly read a file in terminal
**Note**: Best for small files (large files will flood your screen)

---

#### 7. `clear` - Clear terminal screen
```
clear                             # Clear all text on screen
clear -h                          # View help
```
**When to use**: When terminal gets cluttered
**Shortcut**: Ctrl + L (works on most terminals)

---

## Advanced Navigation Tips

#### Navigating with Absolute vs Relative Paths
```
# Absolute path (starts from root /)
cd /Users/yourname/Documents/my-project

# Relative path (starts from current location)
cd Documents/my-project
cd ../sibling-folder
cd ./current-folder
```

#### Using Tab Completion
```
cd Doc[TAB]                       # Press Tab to auto-complete
# Becomes: cd Documents
```
**Pro tip**: Tab saves typing and prevents spelling errors!

#### Using Up/Down Arrows
```
[UP ARROW]                        # Cycle through previous commands
[DOWN ARROW]                      # Cycle forward through commands
```

#### Home Directory Shortcuts
```
~                                 # Home folder (/Users/yourname)
cd ~                              # Go to home
cd ~/Documents                    # Documents in home
```

---

## Common Terminal Workflows

### Create a New Project Folder
```
mkdir my-new-project              # Create folder
cd my-new-project                 # Enter folder
pwd                               # Confirm location
ls                                # See contents (empty)
```

### Create Files for a Project
```
mkdir my-website
cd my-website
touch index.html
touch style.css
touch script.js
ls                                # See all files created
```

---

## 🎯 Important Symbols & Shortcuts

| Symbol | Meaning |
|--------|---------|
| `.` | Current folder |
| `..` | Parent folder (one level up) |

---

## Command Anatomy

Every command follows this pattern:

```
command -flag argument

Examples:
ls -la Documents
├─ command: ls
├─ flag: -la (options that modify behavior)
└─ argument: Documents (what the command acts on)
```

**Types of flags**:
- Short flags: `-l` (single dash, one letter)
- Long flags: `--long` (double dash, full word)
- Combined: `-la` (multiple short flags together)

---

## ⚠️ Safety Tips

- [ ] Always use `ls` before `rm` (double-check before deleting)
- [ ] Use `rm -i` for confirmation before deleting
- [ ] Use `cp` to backup files before editing
- [ ] Use `pwd` when lost to confirm location
- [ ] Don't delete system files (nothing in `/System` or `/Windows`)
- [ ] Create backups of important folders

---

## Cheat Sheet: Quick Reference

```
pwd                    # Current location
ls                     # List files
ls -la                 # List all detailed
cd folder              # Enter folder
cd ..                  # Go up one level
cd ~                   # Go home
mkdir folder           # Create folder
touch file.txt         # Create file
cp file copy.txt       # Copy file
mv old.txt new.txt     # Rename file
rm file.txt            # Delete file
rm -i file.txt         # Safe delete (ask first)
cat file.txt           # View file contents
tree                   # Show structure
clear                  # Clear screen
```
