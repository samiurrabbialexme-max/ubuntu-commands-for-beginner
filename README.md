# 🌌══════════════════════════════════════════════════════════════════════🌌
#          🚀 UBUNTU / LINUX TERMINAL COMMANDS FOR DEVELOPERS 🚀
#                  The Ultimate Cyberpunk Developer Cheat Sheet
# 🌌══════════════════════════════════════════════════════════════════════🌌

> "The terminal isn't just a tool.
> It's where developers become wizards."

---

# 📑 Table of Contents

1. Navigation
2. File Operations
3. Permissions
4. Package Management
5. Searching
6. Process Management
7. Networking
8. SSH
9. Disk Management
10. Compression
11. System Information
12. Logs
13. Git
14. Docker
15. Bash Tricks
16. Environment Variables
17. Development
18. Curl & Wget
19. Monitoring
20. Productivity
21. Dangerous Commands
22. Useful One-liners

---

# 🌍 Navigation

| Command | Description |
|---------|-------------|
| pwd | Current directory |
| ls | List files |
| ls -la | Detailed list |
| ls -lh | Human readable |
| tree | Directory tree |
| cd folder | Change folder |
| cd .. | Go back |
| cd ~ | Home directory |
| cd - | Previous directory |
| clear | Clear terminal |
| history | Command history |
| !! | Repeat last command |
| exit | Exit terminal |

---

# 📂 File Operations

```bash
touch file.txt
mkdir project
mkdir -p app/src/main
cp file1 file2
cp -r folder backup
mv old new
rm file
rm -r folder
rm -rf folder
cat file.txt
less file.txt
head file.txt
tail file.txt
tail -f logfile.log
nano file
vim file
code .
```

---

# 🔍 Find Files

```bash
find . -name "*.java"
find . -type d
find . -type f
locate chrome
which python3
whereis node
```

---

# 🔎 Search Text

```bash
grep hello file.txt
grep -r TODO .
grep -n main app.py
grep -i error log.txt
```

---

# 🔐 Permissions

```bash
chmod 755 script.sh
chmod +x script.sh
chmod -R 777 folder
chown user file
chgrp developers file
sudo !!
sudo su
whoami
id
groups
```

Permission Numbers

```
7 = rwx
6 = rw-
5 = r-x
4 = r--
```

---

# 📦 Package Management (Ubuntu)

```bash
sudo apt update
sudo apt upgrade
sudo apt install git
sudo apt remove firefox
sudo apt autoremove
sudo apt clean
apt search docker
apt show curl
dpkg -i package.deb
```

Snap

```bash
snap list
snap install code --classic
snap remove firefox
```

Flatpak

```bash
flatpak install
flatpak update
flatpak list
```

---

# ⚙ Process Management

```bash
ps
ps aux
top
htop
kill PID
kill -9 PID
pkill chrome
jobs
bg
fg
nohup command &
```

---

# 🌐 Networking

```bash
ip a
ip r
hostname
hostname -I
ping google.com
curl ifconfig.me
wget URL
netstat -tulpn
ss -tulpn
dig google.com
nslookup google.com
traceroute google.com
```

---

# 🔥 SSH

```bash
ssh user@host
ssh-keygen
ssh-copy-id user@host
scp file user@host:/home
scp -r folder server:/var/www
```

---

# 💾 Disk

```bash
df -h
du -sh folder
du -h
lsblk
mount
umount
fdisk -l
```

---

# 📦 Compression

```bash
zip file.zip folder
unzip file.zip
tar -cvf archive.tar folder
tar -xvf archive.tar
tar -czvf archive.tar.gz folder
tar -xzvf archive.tar.gz
```

---

# 🖥 System Information

```bash
uname -a
hostnamectl
lscpu
free -h
uptime
neofetch
screenfetch
```

---

# 📜 Logs

```bash
journalctl
journalctl -xe
journalctl -u nginx
dmesg
```

---

# 🌳 Git

```bash
git init
git clone URL
git status
git add .
git commit -m "message"
git push
git pull
git fetch
git branch
git checkout branch
git switch branch
git merge
git rebase
git stash
git stash pop
git log
git diff
git remote -v
```

---

# 🐳 Docker

```bash
docker ps
docker ps -a
docker images
docker pull ubuntu
docker run ubuntu
docker exec -it container bash
docker stop container
docker rm container
docker compose up
docker compose down
```

---

# 🐍 Python

```bash
python3
python3 file.py
pip install package
pip list
python -m venv venv
source venv/bin/activate
deactivate
```

---

# 🟩 Node.js

```bash
node app.js
npm install
npm install express
npm run dev
npm run build
npm start
npx create-react-app
```

---

# ☕ Java

```bash
javac Main.java
java Main
gradle build
./gradlew assembleDebug
```

---

# 🌐 Curl

```bash
curl google.com
curl -O URL
curl -I URL
curl -X POST URL
curl -H "Authorization: token"
```

---

# 📥 Wget

```bash
wget URL
wget -c URL
wget -r website
```

---

# 📈 Monitoring

```bash
top
htop
iotop
vmstat
watch free -h
watch df -h
```

---

# 🌍 Environment Variables

```bash
echo $HOME
echo $PATH
export JAVA_HOME=/usr/lib/jvm
env
printenv
```

---

# ⚡ Bash Tricks

```bash
alias ll="ls -la"

history | grep git

CTRL + C
CTRL + D
CTRL + L
CTRL + A
CTRL + E
CTRL + R
TAB
```

---

# 🚀 Productivity

```bash
time command

watch -n 2 command

xargs

tee

yes

seq 1 100

sort

uniq

wc

cut

awk

sed
```

Examples

```bash
cat log.txt | grep ERROR

ps aux | grep chrome

ls | wc -l

cat file | sort | uniq

awk '{print $1}' file

sed 's/old/new/g' file
```

---

# 🧠 Useful One-Liners

Largest folders

```bash
du -h . | sort -hr | head
```

Open current folder

```bash
xdg-open .
```

Find large files

```bash
find . -type f -size +100M
```

Find empty files

```bash
find . -empty
```

Delete *.log

```bash
find . -name "*.log" -delete
```

Count files

```bash
find . -type f | wc -l
```

Random password

```bash
openssl rand -base64 20
```

Current IP

```bash
curl ifconfig.me
```

CPU Information

```bash
lscpu
```

Memory

```bash
free -h
```

---

# ☠ Dangerous Commands

Never run these unless you know exactly what they do.

```bash
rm -rf /

chmod -R 777 /

dd if=/dev/zero of=/dev/sda

mkfs.ext4 /dev/sda

:(){ :|:& };:
```

---

# 🛰 Developer Workflow

```text
Git
 ↓
Code
 ↓
Build
 ↓
Test
 ↓
Docker
 ↓
Deploy
 ↓
SSH
 ↓
Monitor
```

---

# 🎯 Recommended Developer Tools

✅ git

✅ curl

✅ wget

✅ htop

✅ tree

✅ neofetch

✅ docker

✅ docker compose

✅ tmux

✅ vim

✅ nano

✅ jq

✅ ripgrep (rg)

✅ bat

✅ fzf

✅ fd

✅ ncdu

---

# 🌌 Terminal Philosophy

```
GUI makes things easier.

Terminal makes impossible things possible.
```

---

# 🚀 Happy Coding!

```
██████╗ ███████╗██╗   ██╗
██╔══██╗██╔════╝██║   ██║
██║  ██║█████╗  ██║   ██║
██║  ██║██╔══╝  ╚██╗ ██╔╝
██████╔╝███████╗ ╚████╔╝
╚═════╝ ╚══════╝  ╚═══╝

Code.
Build.
Hack.
Repeat.

# 🚀 Happy Coding!

```
███████╗ █████╗ ███╗   ███╗██╗██╗   ██╗██████╗
██╔════╝██╔══██╗████╗ ████║██║██║   ██║██╔══██╗
███████╗███████║██╔████╔██║██║██║   ██║██████╔╝
╚════██║██╔══██║██║╚██╔╝██║██║██║   ██║██╔══██╗
███████║██║  ██║██║ ╚═╝ ██║██║╚██████╔╝██║  ██║
╚══════╝╚═╝  ╚═╝╚═╝     ╚═╝╚═╝ ╚═════╝ ╚═╝  ╚═╝

               ██████╗  █████╗ ██████╗ ██████╗ ██╗
               ██╔══██╗██╔══██╗██╔══██╗██╔══██╗██║
               ██████╔╝███████║██████╔╝██████╔╝██║
               ██╔══██╗██╔══██║██╔══██╗██╔══██╗██║
               ██║  ██║██║  ██║██████╔╝██████╔╝██║
               ╚═╝  ╚═╝╚═╝  ╚═╝╚═════╝ ╚═════╝ ╚═╝

                     ✨  S A M I U R   R A B B I   A L E X  ✨
```

> *"Code. Create. Innovate. Repeat."* 🚀
```
