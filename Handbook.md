# ╔══════════════════════════════════════════════════════════════════════╗
# ║                                                                    ║
# ║          🚀 LINUX DEVELOPER HANDBOOK                               ║
# ║                                                                    ║
# ║          Ubuntu • Linux Terminal • Developer Reference             ║
# ║                                                                    ║
# ║                 👨‍💻 Author: Samiur Rabbi Alex                      ║
# ║                                                                    ║
# ╚══════════════════════════════════════════════════════════════════════╝

> **"The terminal isn't just a tool; it's a developer's superpower."**

---

# 📚 Table of Contents

1. Terminal Basics
2. Navigation
3. File & Directory Management
4. File Permissions
5. Package Management
6. Process Management
7. Searching Files & Text
8. Networking
9. SSH
10. Git Essentials
11. Docker Essentials
12. Python & Node.js
13. Useful One-Liners
14. Common Mistakes
15. Daily Developer Workflow

---

# 🚀 1. Terminal Basics

The Linux terminal (Shell) allows you to communicate directly with the operating system. Every command follows the general structure:

```bash
command [options] [arguments]
```

Example:

```bash
ls -la
```

- **ls** → command
- **-la** → options (`-l` long format, `-a` show hidden files)

---

# 📂 2. Navigation

## pwd — Print Working Directory

Shows your current location.

```bash
pwd
```

Output:

```text
/home/alex/Documents
```

---

## ls — List Files

```bash
ls
```

Lists files in the current directory.

### Common Options

```bash
ls -l
```

Long view.

```bash
ls -a
```

Show hidden files.

```bash
ls -lh
```

Human-readable sizes.

```bash
ls -lah
```

Developer favorite.

---

## cd — Change Directory

Go into a folder.

```bash
cd Documents
```

Go back.

```bash
cd ..
```

Go Home.

```bash
cd ~
```

Return to previous folder.

```bash
cd -
```

---

## clear

Clear the terminal.

```bash
clear
```

Shortcut:

```
Ctrl + L
```

---

# 📁 3. File & Directory Management

## Create Files

```bash
touch notes.txt
```

Creates an empty file.

---

## Create Directories

```bash
mkdir project
```

Nested folders.

```bash
mkdir -p app/src/main/java
```

---

## Copy

```bash
cp file.txt backup.txt
```

Copy directories.

```bash
cp -r project backup
```

---

## Move / Rename

```bash
mv old.txt new.txt
```

Move file.

```bash
mv file.txt Documents/
```

---

## Delete

Delete file.

```bash
rm file.txt
```

Delete folder.

```bash
rm -r folder
```

Force delete.

```bash
rm -rf folder
```

⚠ Never use:

```bash
sudo rm -rf /
```

---

## View File

```bash
cat file.txt
```

Large file.

```bash
less file.txt
```

First lines.

```bash
head file.txt
```

Last lines.

```bash
tail file.txt
```

Live log monitoring.

```bash
tail -f app.log
```

---

# 🔐 4. File Permissions

View permissions.

```bash
ls -l
```

Example

```text
-rwxr-xr-x
```

Meaning

| Symbol | Meaning |
|---------|----------|
| r | Read |
| w | Write |
| x | Execute |

Permission Numbers

| Number | Permission |
|---------|------------|
|7|rwx|
|6|rw-|
|5|r-x|
|4|r--|

Make executable.

```bash
chmod +x script.sh
```

Numeric mode.

```bash
chmod 755 script.sh
```

Owner only.

```bash
chmod 700 private.sh
```

Change owner.

```bash
sudo chown alex:developers project
```

---

# 📦 5. Package Management

Update package list.

```bash
sudo apt update
```

Upgrade system.

```bash
sudo apt upgrade
```

Install package.

```bash
sudo apt install git
```

Remove package.

```bash
sudo apt remove firefox
```

Clean packages.

```bash
sudo apt autoremove
```

Search package.

```bash
apt search docker
```

Package information.

```bash
apt show curl
```

---

# ⚙ 6. Process Management

Running processes.

```bash
ps
```

Detailed view.

```bash
ps aux
```

Interactive monitor.

```bash
top
```

Better monitor.

```bash
htop
```

Kill process.

```bash
kill PID
```

Force kill.

```bash
kill -9 PID
```

Kill by name.

```bash
pkill chrome
```

Background execution.

```bash
command &
```

---

# 🔍 7. Searching Files & Text

Find files.

```bash
find . -name "*.java"
```

Directories only.

```bash
find . -type d
```

Files larger than 100MB.

```bash
find . -size +100M
```

Search text.

```bash
grep "error" log.txt
```

Recursive.

```bash
grep -rn "TODO" .
```

Ignore case.

```bash
grep -i warning app.log
```

Locate installed file.

```bash
which python3
```

---

# 🌐 8. Networking

IP Address.

```bash
ip a
```

Routing.

```bash
ip r
```

Hostname.

```bash
hostname
```

Internet test.

```bash
ping google.com
```

Download.

```bash
wget URL
```

API request.

```bash
curl https://example.com
```

Open ports.

```bash
ss -tulpn
```

DNS.

```bash
nslookup google.com
```

---

# 🔑 9. SSH

Connect server.

```bash
ssh user@server
```

Generate key.

```bash
ssh-keygen
```

Copy key.

```bash
ssh-copy-id user@server
```

Upload file.

```bash
scp file.txt user@server:/home/user
```

Download folder.

```bash
scp -r user@server:/var/www .
```

---

# 🌳 10. Git Essentials

Initialize.

```bash
git init
```

Clone.

```bash
git clone URL
```

Status.

```bash
git status
```

Add files.

```bash
git add .
```

Commit.

```bash
git commit -m "Initial commit"
```

Push.

```bash
git push origin main
```

Pull.

```bash
git pull
```

Branch.

```bash
git branch
```

Switch.

```bash
git switch feature
```

Log.

```bash
git log --oneline
```

---

# 🐳 11. Docker

Images.

```bash
docker images
```

Containers.

```bash
docker ps
```

Run Ubuntu.

```bash
docker run -it ubuntu bash
```

Stop.

```bash
docker stop container
```

Remove.

```bash
docker rm container
```

Compose.

```bash
docker compose up
```

Shutdown.

```bash
docker compose down
```

---

# 🐍 12. Python & Node.js

Python

```bash
python3 app.py
```

Virtual environment.

```bash
python3 -m venv venv
```

Activate.

```bash
source venv/bin/activate
```

Install package.

```bash
pip install requests
```

Node

```bash
npm install
```

Development server.

```bash
npm run dev
```

Production.

```bash
npm run build
```

---

# ⚡ 13. Useful One-Liners

Largest folders.

```bash
du -h . | sort -hr | head
```

Count files.

```bash
find . -type f | wc -l
```

Find empty files.

```bash
find . -empty
```

Random password.

```bash
openssl rand -base64 20
```

Open current folder.

```bash
xdg-open .
```

Current public IP.

```bash
curl ifconfig.me
```

---

# ⚠ 14. Common Mistakes

❌ Wrong

```bash
rm *
```

May delete everything.

---

❌ Wrong

```bash
chmod 777 -R /
```

Huge security risk.

---

❌ Wrong

```bash
sudo
```

Without understanding what you're doing.

---

✅ Always verify commands before pressing Enter.

---

# 💻 15. Daily Developer Workflow

```text
┌────────────┐
│ Open Shell │
└─────┬──────┘
      │
      ▼
 git pull
      │
      ▼
 code .
      │
      ▼
 Build Project
      │
      ▼
 Test
      │
      ▼
 Commit
      │
      ▼
 Push
      │
      ▼
 Deploy
      │
      ▼
 SSH Server
      │
      ▼
 Monitor Logs
```

---

# 🎯 Developer Tips

✅ Learn keyboard shortcuts.

✅ Use aliases.

```bash
alias ll="ls -lah"
```

✅ Keep your system updated.

```bash
sudo apt update && sudo apt upgrade
```

✅ Read documentation.

```bash
man ls
```

or

```bash
ls --help
```

---

# 📖 Recommended Commands to Master

- ls
- cd
- pwd
- cp
- mv
- rm
- chmod
- chown
- grep
- find
- curl
- wget
- ssh
- git
- docker
- top
- htop
- ps
- kill
- tar
- zip
- unzip
- apt
- nano
- vim
- cat
- less
- tail
- journalctl
- systemctl

Master these commands, and you'll be productive on nearly any Ubuntu or Linux system.

---

# 🌌 Closing Message

```
███████╗ █████╗ ███╗   ███╗██╗██╗   ██╗██████╗
██╔════╝██╔══██╗████╗ ████║██║██║   ██║██╔══██╗
███████╗███████║██╔████╔██║██║██║   ██║██████╔╝
╚════██║██╔══██║██║╚██╔╝██║██║██║   ██║██╔══██╗
███████║██║  ██║██║ ╚═╝ ██║██║╚██████╔╝██║  ██║
╚══════╝╚═╝  ╚═╝╚═╝     ╚═╝╚═╝ ╚═════╝ ╚═╝  ╚═╝

          ✨  S A M I U R   R A B B I   A L E X  ✨
```

> **Code. Learn. Build. Share. Repeat. 🚀**
