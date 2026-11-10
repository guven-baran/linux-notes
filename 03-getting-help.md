# Getting Help & Knowing the System — Lesson 3

## Terminal vs Shell vs Bash
- **Terminal (emulator):** the window where you type commands.
- **Shell:** the program inside the terminal that reads and runs your commands.
- **Bash:** the most common type of shell (others: zsh, fish).
- **PowerShell:** Windows' own shell (can also run on Linux).

## Reading the Prompt — `kali@kali:~$`
- `kali` → current **user**
- `@kali` → **hostname** (the machine)
- `:~` → current location (`~` = home directory)
- `$` → logged in as a normal **user**
- `#` → logged in as **root** (full admin power — be careful)

## Getting Help
| Command | What it does |
|---------|--------------|
| `man <cmd>` | Full manual for a command (press `q` to quit) |
| `<cmd> --help` / `-h` | Short usage summary |
| `apropos <keyword>` | Search for a command by keyword |

## Knowing the System
| Command | What it does |
|---------|--------------|
| `whoami` | Show current user |
| `id` | Show user and group IDs |
| `hostname` | Show the machine's name |
| `uname -a` | Show system/kernel info |
| `ps` | List running processes |
| `who` | Show who is logged in |
| `ip a` | Show network interfaces / IP addresses |
| `lsblk` | List block devices (disks) |
| `lsusb` | List connected USB devices |
