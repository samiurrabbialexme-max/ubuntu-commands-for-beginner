# 🐧 Ubuntu Terminal Cheat Sheet for MERN Developers

> Beginner-friendly • Ubuntu + VS Code + Chrome + Git + Node.js

------------------------------------------------------------------------

## 🚀 Open Applications

  Action                          Command
  ------------------------------- --------------------
  Open Chrome                     `google-chrome`
  Open VS Code (current folder)   `code .`
  Open Home                       `cd ~`
  Open File Manager               `nautilus .`
  New Terminal                    **Ctrl + Alt + T**

## 📁 Navigation

``` bash
pwd        # Current directory
ls -la     # List all files
cd folder  # Enter folder
cd ..      # Go back
cd -       # Previous folder
```

## 📂 File Operations

``` bash
mkdir project
touch app.js
cp file.txt backup.txt
mv old.txt new.txt
rm file.txt
rm -rf folder
```

## 🌿 Git

``` bash
git clone URL
git status
git add .
git commit -m "message"
git push
git pull
```

## 🟢 Node & npm

``` bash
node -v
npm -v
npm install
npm run dev
npm start
```

## ⌨️ Terminal Shortcuts

  Shortcut         Action
  ---------------- ----------------
  Tab              Auto-complete
  Ctrl+C           Stop process
  Ctrl+L           Clear screen
  Ctrl+R           Search history
  Ctrl+Shift+C/V   Copy / Paste

## ⭐ Useful Aliases

Add to `~/.bashrc`

``` bash
alias c='clear'
alias ll='ls -lah'
alias gs='git status'
alias ..='cd ..'
alias proj='cd ~/Projects'
source ~/.bashrc
```

## 💻 Daily MERN Workflow

``` bash
cd ~/Projects/my-app
code .
npm install
npm run dev
```

## 🛠️ Must-have Apps

-   VS Code
-   Google Chrome
-   Git
-   Node.js LTS
-   Postman
-   MongoDB Compass
