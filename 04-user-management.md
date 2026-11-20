# User & Group Management — Lesson 4

## Root & sudo
- **root:** the all-powerful admin account (UID 0).
- **sudo:** run a single command with root privileges ("please, as admin").
- Stay a normal user; use `sudo` only when needed (safer).

## User Commands
| Command | What it does |
|---------|--------------|
| `sudo adduser <name>` | Add a user (interactive; sets home + bash). Preferred. |
| `sudo useradd <name>` | Add a user (minimal; no home/password by default). |
| `sudo passwd <name>` | Set or change a user's password. |
| `sudo usermod ...` | Modify a user (shell, name, groups). |
| `sudo userdel <name>` | Delete a user. |

## Where Users Live
| File | Purpose |
|------|---------|
| `/etc/passwd` | List of all users (readable by everyone). |
| `/etc/shadow` | Hashed passwords (root only). |

`/etc/passwd` format: `user:x:UID:GID:name:home:shell`
- `x` → password is stored in `/etc/shadow`
- root's UID is always `0`

## Groups
| Command | What it does |
|---------|--------------|
| `groups` | Show my current groups. |
| `sudo groupadd <name>` | Create a group. |
| `sudo groupdel <name>` | Delete a group. |
| `sudo usermod -aG <group> <user>` | Add user to a group (keep existing groups). |

- Use `-aG` (append), not `-G` alone (which removes other groups).
- Adding a user to the `sudo` group grants them sudo access.

## Switching Users
| Command | What it does |
|---------|--------------|
| `su - <user>` | Switch to another user (needs their password). |
| `sudo su -` | Switch to root (uses your sudo rights). |
| `exit` / `Ctrl+D` | Return to your own user. |

## The sudoers File
- `/etc/sudoers` defines who can use sudo.
- **Always** edit it with `sudo visudo` (it checks for errors before saving).
- Never edit it directly — a mistake can break sudo entirely.
