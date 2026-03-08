# Do portfolio work locally in Cursor

This folder is your **portfolio repo**. To use Cursor’s Source Control (commit, push) here, you need Git working on your Mac **once**, then you can do everything from Cursor.

---

## 1. One-time: Install Git (Command Line Tools)

In **Terminal** (not Cursor), run:

```bash
xcode-select --install
```

A dialog will ask to install the “Command Line Developer Tools.” Click **Install** and wait for it to finish.

---

## 2. One-time: Turn this folder into a Git repo

In **Terminal**, run:

```bash
cd "/Users/jacquelinekoerner/Downloads/jacquelinekoerner.github.io"
git init
git branch -M main
git remote add origin https://github.com/jacquelinekoerner/jacquelinekoerner.github.io.git
```

If the repo **already exists** on GitHub and you want to match it (instead of starting fresh), use this instead of the above:

```bash
cd "/Users/jacquelinekoerner/Downloads/jacquelinekoerner.github.io"
# Backup your files, then replace folder with a clone:
cd ..
mv jacquelinekoerner.github.io jacquelinekoerner.github.io-backup
git clone https://github.com/jacquelinekoerner/jacquelinekoerner.github.io.git
# Copy your updated files from the backup into the new folder, then delete the backup.
```

---

## 3. Open this folder in Cursor

- **File → Open Folder…**
- Choose: **Downloads → jacquelinekoerner.github.io**

Cursor’s workspace is now the repo. You can edit `index.html` and `README.md` here.

---

## 4. Commit and push from Cursor

- **Source Control** (branch icon in the left sidebar, or `Cmd+Shift+G`)
- Stage: check **index.html** and **README.md** (or “Stage All Changes”)
- Message: e.g. `Update portfolio — March 2026`
- Click **Commit**
- Click **Sync Changes** (or **Push**) to send to GitHub

Or use **Cursor’s integrated Terminal** (`Ctrl+`` ` or View → Terminal) from this folder:

```bash
git add index.html README.md
git commit -m "Update portfolio — March 2026"
git push -u origin main
```

---

## Summary

| Step | Where |
|------|--------|
| Install Command Line Tools | Terminal (once) |
| `git init` + `remote add` (or clone) | Terminal (once) |
| Edit portfolio | Cursor |
| Commit & push | Cursor (Source Control or integrated Terminal) |

After the one-time setup, you only need Cursor and this folder.
