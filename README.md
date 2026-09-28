# Web Development Setup Guide

> A step-by-step environment setup guide for first-year students — Windows edition.

---

## Table of Contents

1. [Install Visual Studio Code](#1-install-visual-studio-code)
2. [Install the Live Server Extension](#2-install-the-live-server-extension)
3. [Create a GitHub Account](#3-create-a-github-account)
4. [Install Git on Windows](#4-install-git-on-windows)
5. [Configure Git with Your GitHub Account](#5-configure-git-with-your-github-account)
6. [Clone the Repository](#6-clone-the-repository)
7. [Set Up Your Working Folder](#7-set-up-your-working-folder)
8. [Open the Project in VS Code](#8-open-the-project-in-vs-code)


---

## 1. Install Visual Studio Code

VS Code is a free, lightweight code editor made by Microsoft. It supports syntax highlighting, smart auto-complete, a built-in terminal, and built-in Git — everything you need for web development.

1. Go to **[https://code.visualstudio.com](https://code.visualstudio.com)** (always download from the official site).
2. Click **Download for Windows** and save the `.exe` file.
3. Open your **Downloads** folder and double-click the installer.
4. Select **"I accept the agreement"** → click **Next**.
5. Keep the default install location and Start Menu folder → click **Next** through both screens.
6. On the **Select Additional Tasks** screen, make sure these are checked:
   - ✅ Create a desktop icon
   - ✅ "Open with Code" in file/folder right-click menus
   - ✅ **Add to PATH** ← important, leave this checked
7. Click **Next** → **Install** → **Finish** (keep "Launch VS Code" checked).

---

## 2. Install the Live Server Extension

Live Server runs a local web server that auto-refreshes your browser every time you save a file — essential for HTML/CSS/JS development.

1. In VS Code, click the **Extensions** icon in the left sidebar (or press `Ctrl+Shift+X`).
2. Search for **Live Server**.
3. Select the one by **Ritwick Dey** and click **Install**.
4. To use it: open any `.html` file, right-click → **"Open with Live Server"**, or click **Go Live** in the bottom status bar.

---

## 3. Create a GitHub Account

> Use your **college email address** (ending with `@thesiu.in`) when registering.

1. Go to **[https://github.com](https://github.com)** and click **Sign up**.
2. Enter your **college email** (`yourname@thesiu.in`), choose a username and password.
3. Complete the verification steps and confirm your email via the link sent to your inbox.
4. Once signed in, your GitHub account is ready.

---

## 4. Install Git on Windows

1. Go to **[https://git-scm.com](https://git-scm.com)** and click **Download for Windows**.
2. Double-click the downloaded `.exe` and click **Yes** on the permission prompt.
3. Click **Next** through the license, install location, components, and Start Menu screens — **defaults are fine**.
4. On the **"Choose Git's default editor"** screen → select **"Use Visual Studio Code as Git's default editor"** → **Next**.
5. On the **"Override the default branch name"** screen → type `main` → **Next**.
6. For all remaining screens (PATH, SSH, HTTPS backend, line endings, terminal, git pull behaviour, credential helper) — keep the **recommended defaults** and click **Next** each time.
7. Click **Install** → **Finish**.

---

## 5. Configure Git with Your GitHub Account

Open the integrated terminal in VS Code (`Ctrl+```) and run these two commands — replace the values with your own name and college email:

```bash
git config --global user.name "Your Full Name"
git config --global user.email "yourname@thesiu.in"
```

> This is a one-time setup. It links your commits to your GitHub identity across all repositories.

---

## 6. Clone the Repository

Clone the repository into your **D drive** using the terminal.

1. Open **Command Prompt** or the **VS Code integrated terminal** (`Ctrl+``\``).
2. Navigate to the D drive:

   ```bash
   D:
   ```

3. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

   > Since the repository is private, a browser window will open — **sign in to GitHub** and grant access when prompted (one-time only).

4. After cloning, a new folder with the repository name will appear in `D:\`.

---

## 7. Set Up Your Working Folder

After cloning, create a separate working folder on your D drive and copy the cloned files into it. This keeps your working copy separate from the cloned source.

1. Open **File Explorer** and navigate to your **D drive**.
2. Create a new folder, for example:

   ```
   D:\WebDev
   ```

3. Copy the entire contents of the cloned repository folder (from `D:\<repo-name>`) and paste them into `D:\WebDev\`.

> You will do your day-to-day work inside `D:\WebDev\`.

---

## 8. Open the Project in VS Code

1. In VS Code, go to **File → Open Folder** (or press `Ctrl+K Ctrl+O`).
2. Navigate to `D:\WebDev\` and click **Select Folder**.
3. The project files will appear in the **Explorer** panel on the left.
4. Open any `.html` file and click **Go Live** in the status bar to preview it in your browser.

---

<div align="center">

Happy Coding 😊

</div>

---
