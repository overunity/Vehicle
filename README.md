# Unreal Engine Project Git + LFS Setup Guide

This repository is a **template** for creating new Unreal Engine projects with proper Git and Git LFS configuration.  
It includes:
- `.gitignore` — keeps Unreal’s temporary, build, and cache files out of Git.
- `.gitattributes` — ensures all large binary asset types are stored efficiently with Git LFS.

---

## ✅ How to Use This Template for a New Unreal Project

### 1. Create Your Unreal Project
- Open **Unreal Engine**.
- Choose a template (e.g. First Person, Third Person).
- Name your project (e.g. `MyAwesomeGame`).
- Choose a location **outside of OneDrive/Dropbox** (e.g. `D:\UnrealProjects\MyAwesomeGame`).
- Uncheck "Include Starter Content" if you want a lightweight start.
- Click **Create**.

---

### 2. Start from This Template
1. On GitHub, open this repository and click **Use this template**.
2. Name your new repository (e.g. `MyAwesomeGame`).
3. Clone your new repository to your computer.
4. Move or create your Unreal project files inside the cloned folder.

---

### 3. Initialize Git LFS (once per machine)
Open a terminal (Git Bash or PowerShell) in your project folder and run:
```
git lfs install
```

---

### 4. Commit the Rules First
If your `.gitattributes` and `.gitignore` are not yet committed (only for a brand-new repo):
```
git add .gitattributes .gitignore
git commit -m "Add Git + LFS rules for Unreal Engine"
```

---

### 5. Add and Commit Your Project
```
git add .
git commit -m "Initial commit - Unreal project files"
git push -u origin main
```

---

## ✅ What This Setup Does
- **`.gitignore`** blocks:
  - `Binaries/`, `Build/`, `DerivedDataCache/`, `Intermediate/`, `Saved/`  
  - Temporary, log, and backup files
  - IDE/editor-specific settings that don’t belong in version control
- **`.gitattributes`** automatically stores in LFS:
  - Unreal assets (`.uasset`, `.umap`)
  - Models, textures, audio, video, and other large binary files

---

## 📌 Notes for Collaborators
- After cloning the repo for the first time, run:
```
git lfs install
```
- All large files will be handled by LFS automatically — no manual tracking needed.

---

Happy developing! 🚀
