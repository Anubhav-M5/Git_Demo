# Git & VS Code Command Cheat Sheet

A beginner-friendly guide covering essential Git commands, flags, and VS Code integration workflows.

---

## 1. Deconstructing Flag Options & Abbreviations

Flags modify how a command behaves. Here is what the flags used in our commands mean:

| Flag / Option | Full Name | What It Does | Example Command |
| :--- | :--- | :--- | :--- |
| **`-m`** | `--message` | Attaches an inline commit message directly in the terminal (avoids opening Vim/Nano editor). | `git commit -m "Initial commit"` |
| **`-b`** | `--branch` | Tells `checkout` or `switch` to **create a new branch** before switching to it. | `git checkout -b feature-test` |
| **`-a`** | `--all` | Automatically stages all modified and deleted files (does **not** stage newly created untracked files). | `git commit -a -m "Quick save"` |
| **`-am`** | Combined `-a` and `-m` | Stages all modified files **AND** commits them with a message in one single step. | `git commit -am "Update docs"` |
| **`-u`** | `--set-upstream` | Links your local branch to the remote branch on GitHub so future `git push` or `git pull` commands don't need parameters. | `git push -u origin feature-branch` |

---

## 2. All Commands Covered

### Terminal & File Navigation
| Command | Description |
| :--- | :--- |
| `touch filename.txt` | Creates a new empty file in the current directory *(Mac/Linux/Git Bash)*. |
| `echo "text" > file.txt` | Creates a file with `"text"` inside it (or overwrites if it already exists). |
| `echo "text" >> file.txt` | Appends `"text"` as a new line to an existing file without overwriting. |
| `code filename.txt` | Opens the target file directly in the VS Code editor panel. |
| `ls` / `dir` | Lists all files and folders in your current directory (`ls` for Git Bash/Mac, `dir` for PowerShell). |
| `cd folder-name` | Navigates into a specific directory. |

---

### Core Git Workflow (Edit → Stage → Commit → Push)
| Command | Description |
| :--- | :--- |
| `git status` | Displays modified, untracked, and staged files in your repository. |
| `git add filename` | Moves a specific file from the working directory to the Staging Area. |
| `git add .` | Stages **all** modified, deleted, and newly created files in the repository. |
| `git commit -m "msg"` | Saves staged changes as a historical snapshot with a descriptive message. |
| `git push origin main` | Uploads local commits from your `main` branch to GitHub. |
| `git pull` | Downloads and merges the latest changes from GitHub into your local folder. |

---

### Branching & Merging
| Command | Description |
| :--- | :--- |
| `git checkout -b <name>` | Creates a new branch named `<name>` and immediately switches to it. |
| `git checkout <name>` | Switches to an existing branch named `<name>`. |
| `git merge <branch>` | Combines changes from `<branch>` into your currently active branch. |

---

### Undoing, Moving & Inspection
| Command | Description |
| :--- | :--- |
| `git log --oneline` | Displays a compact list of past commit IDs and commit messages. |
| `git restore filename` | Discards uncommitted changes in a file (resets it back to the last commit). |
| `git restore --staged file` | Unstages a file (moves it from Staged back to regular Changes). |
| `git stash` | Temporarily stashes modified tracked files so you have a clean working directory. |
| `git stash pop` | Restores your most recently stashed changes back into your working folder. |
| `git mv old.txt new.txt` | Renames a file while automatically keeping track of the change in Git. |
| `git rm filename.txt` | Deletes a file from both disk and Git tracking. |

---

## 3. Essential VS Code Visual Shortcuts

* **Toggle Terminal:** `` Ctrl + ` ``
* **Open Source Control Panel:** `Ctrl + Shift + G` *(Mac: `Cmd + Shift + G`)*
* **Open File Explorer:** `Ctrl + Shift + E` *(Mac: `Cmd + Shift + E`)*
* **Switch Active Branch:** Click the branch name in the bottom-left corner of the status bar.
* **Stage File via GUI:** Click the `+` icon next to the file inside the Source Control panel.
* **Resolve Merge Conflicts:** Click `Accept Current` or `Accept Incoming` options hovering above highlighted conflict lines in the editor.
