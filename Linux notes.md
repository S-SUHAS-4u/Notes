# Linux Command Line Course Notes

---

## Introduction

Linux is a powerful, open-source operating system widely used in servers, development, and DevOps. The command line (CLI) is essential for interacting with Linux efficiently.

**Benefits of Using the Command Line:**
- Greater control than GUI
- Automation with scripts
- Consistent across distributions

---

## 1. Setting Up Your Environment

### Creating a Linux Virtual Machine
- Use **VirtualBox**, **VMware**, or **WSL (Windows Subsystem for Linux)**
- Install a distribution (e.g., **Ubuntu**, **CentOS**)
- Allocate resources (RAM, CPU, Disk)
- Use snapshot feature for safe experimentation

### Alternatives to a VM
- **MacOS/Linux host OS:** Direct terminal use
- **Windows:** Git Bash, WSL
- **Online terminals:** Katacoda, Replit

### Using GitHub Codespaces
- Provides a **cloud-based Linux environment**
- No local setup required
- Useful for quick command trials and saving work

---

## 2. Command-Line Basics

### What is the Command Line?
- A **text-based interface** to interact with the OS
- Common shells: **bash**, **zsh**, **fish**
- Command prompt format:  
  `username@hostname:~$`

### Command Structure
- Syntax:  
  `command [options] [arguments]`
- Example:  
  `ls -l /home`

### Running Commands
- Execute line by line
- Press `Enter` to run
- Use `Ctrl+C` to stop a running process

### Getting Help
- `man <command>` — manual page
- `<command> --help` — quick help
- `info <command>` — detailed docs

### Useful Keyboard Shortcuts
- `Ctrl+C` — cancel process
- `Ctrl+Z` — suspend process
- `Ctrl+R` — reverse search history
- `↑/↓` — cycle through command history
- `Tab` — autocomplete

---

## 3. Files, Directories, and Permissions

### Linux File System Structure
- **Root directory `/`** is the top
- Standard folders:
  - `/home` — user files
  - `/etc` — configuration
  - `/bin` — essential commands
  - `/var` — logs, variable data

### File Paths
- **Absolute path:** starts from `/` (e.g., `/home/user/docs`)
- **Relative path:** relative to current dir (e.g., `./docs`)

### Navigation Commands
- `pwd` — print working directory
- `cd <dir>` — change directory
- `ls` — list files

### Listing Files
- `ls -l` — long format
- `ls -a` — includes hidden files
- `ls -lh` — human-readable sizes

### Directory Management
- `mkdir newdir` — create directory
- `rmdir emptydir` — remove empty directory

### File Operations
- `cp file1 file2` — copy
- `mv file1 file2` — move/rename
- `rm file` — remove file
- `rm -r dir` — remove directory recursively

### Finding Files
- `find /path -name "filename"`
- `locate filename` (uses index, faster)

### User Roles and `sudo`
- **root (superuser)** and regular users
- `sudo` — run command as root  
  Example: `sudo apt update`

### File Permissions
- Types: **read (r), write (w), execute (x)**
- Example: `-rw-r--r--`  
  (First char = file type: `-`, `d`, `l`)

### Modifying Permissions and Ownership
- `chmod` — change permissions (e.g., `chmod 755 file`)
- `chown` — change ownership

### Links
- Hard link: `ln file linkname`
- Symbolic (soft) link: `ln -s file symlink`

---

## 4. Common Command-Line Tasks and Tools

### Unix Philosophy
- Small programs that do one thing well
- Combine with pipes for powerful workflows

### Pipes
- `|` passes output of one command to another  
  Example: `ls -l | grep ".txt"`

### Viewing Text Files
- `cat file` — view whole file
- `head -n 10 file` — first 10 lines
- `tail -n 10 file` — last 10 lines
- `less file` — scrollable view

### Searching Text
- `grep "pattern" file`
- `grep -i` — ignore case
- `grep -r` — recursive search

### Text Manipulation
- `awk '{print $1}' file` — print first column
- `sed 's/old/new/g' file` — replace text
- `sort file` — sort lines

### Editing Text
- **Vim:** `vim file` (Insert mode: `i`, Command: `:`, Save & quit: `:wq`)
- **Nano:** `nano file` (Shortcuts at bottom, e.g., `Ctrl+O`, `Ctrl+X`)

### Archives
- `tar -cvf archive.tar files/` — create tar
- `tar -xvf archive.tar` — extract tar
- `zip file.zip file1 file2`
- `unzip file.zip`

### Output Redirection
- `>` — redirect output to file (overwrite)
- `>>` — append to file
- `<` — take input from file
- `2>` — redirect errors

### Environment Variables and PATH
- View all: `printenv`
- Echo variable: `echo $PATH`
- Add path:  
  `export PATH=$PATH:/new/dir`

---

## 5. Advanced Topics (A Peek)

### System Information
- Distribution: `cat /etc/os-release`
- Kernel: `uname -a`

### Hardware and Disk Info
- CPU: `lscpu`
- Block devices: `lsblk`
- Disk space: `df -h`
- Memory: `free -h`

### Package Management

**Debian/Ubuntu:**
```bash
sudo apt update
sudo apt install <package>
```

**RedHat/CentOS:**
```bash
sudo yum install <package>
```

- List installed: `dpkg -l` or `rpm -qa`

---


