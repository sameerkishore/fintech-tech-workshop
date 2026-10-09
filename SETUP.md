# Setup guide

You need four things: **Python** (with Jupyter), **VS Code**, **Git**, and a **GitHub account**.
Most of you already have Python from Anaconda for your modules, so **don't install a second Python**. Just add what's missing.

---

## Step 0 · Quick test (2 minutes)

Open a notebook however you normally do (Anaconda Navigator → Jupyter, VS Code, anything) and run:

```python
import sys, pandas
print(sys.version, pandas.__version__)
```

| Result | Go to |
|---|---|
| It printed two version numbers | **Route A**: you already have Python |
| An error, or you don't know how to open a notebook | Try **Route A** with your buddy for up to 10 minutes. If it's still broken, use **Route C** for today and fix your laptop later |
| You have no Python / Anaconda at all | **Route B** |

**Everyone:** create a free GitHub account now if you don't have one: https://github.com/signup

---

## Route A · You already have Anaconda (or another Python)

**1. Install Git** (start this first, because it can take a few minutes)
- **Windows:** download from https://git-scm.com/download/win and run it. Click **Next** through every screen; the defaults are fine.
- **Mac:** open the **Terminal** app and run `git --version`. If it prints a version, you already have it. If a window pops up offering to install the *command line developer tools*, click **Install** and wait (5–15 minutes). You can also trigger it with `xcode-select --install`.

**2. Install VS Code** from https://code.visualstudio.com
- **Mac:** after downloading, **drag Visual Studio Code into your Applications folder**. Running it straight from Downloads causes problems later.

**3. Add the Python and Jupyter extensions.** In VS Code, click the Extensions icon (four squares) on the left, search **Python**, install the one by Microsoft, then do the same for **Jupyter**.

**4. Restart VS Code** (fully quit and reopen) so it finds Git.

→ Now go to [Get the workshop files](#get-the-workshop-files).

## Route B · No Python yet

Install **Anaconda**, the same thing your modules use:
1. Go to https://www.anaconda.com/download. You can click **Skip registration**.
2. Download the installer for your system.
   - Mac: open the Apple menu → *About This Mac*. "Apple M1/M2/M3/M4" = **Apple silicon**; "Intel" = **Intel**.
3. Run it with the default options (on Windows, choose *Just Me*). It's a large download, so while it runs, sit with your buddy or use **Route C**.
4. Then do **Route A** (Git, VS Code, extensions).

> **Windows shortcut:** open **PowerShell** and paste this one line to install all three:
> ```powershell
> winget install -e --id Git.Git; winget install -e --id Microsoft.VisualStudioCode; winget install -e --id Anaconda.Anaconda3
> ```
> If it says `winget` is not recognised, use the download links instead.

## Route C · Your laptop won't cooperate today: GitHub Codespaces

Codespaces is VS Code running in your browser, with everything already installed. It's the **same VS Code and the same GitHub account**, so nothing you learn is wasted.

1. Make your own copy of the workshop repository first (**Use this template → Create a new repository**).
2. On *your* repository page: green **Code** button → **Codespaces** tab → **Create codespace on main**.
3. Wait about 2 minutes while it sets up. Then open `00_setup_check.ipynb`, choose the suggested Python, and run it.

Free accounts get a monthly allowance of hours, more with the Student Developer Pack. Codespaces stop by themselves when idle. Use this for today, then fix your laptop with Route A or B at home.

---

## Get the workshop files

Follow **"Session 3 · Git exercise"** in `README.md`: Use this template → clone in VS Code → set your Git name and email.

## Open a notebook and pick the right Python

1. In VS Code, open `00_setup_check.ipynb`.
2. Top-right, click **Select Kernel** → **Python Environments**.
3. Choose the one that mentions **anaconda3** or **base (conda)** (Route A/B), or the suggested one (Route C).
4. If VS Code asks to install `ipykernel`, click **Install**.
5. Run the cell. Fix any ❌ it reports.

---

## Common problems

| Problem | Fix |
|---|---|
| `git` is not recognised (Windows) | Fully quit and reopen VS Code after installing Git. Still failing? Re-run the Git installer with defaults. |
| `xcrun: error: invalid active developer path` (Mac) | Run `xcode-select --install` in Terminal. |
| VS Code doesn't list Anaconda in *Select Kernel* | `Ctrl/Cmd+Shift+P` → **Python: Select Interpreter** → **Enter interpreter path**. Usually `C:\Users\<you>\anaconda3\python.exe` (Windows) or `/opt/anaconda3/bin/python` or `~/anaconda3/bin/python` (Mac). Then reload the window. |
| `ModuleNotFoundError: No module named ...` | In a notebook cell: `%pip install <name>`, then **Restart** the kernel. |
| `git push` asks for a password | Use the terminal **inside VS Code**, which signs in through your browser. GitHub doesn't accept your account password for Git. You can also sign in via the Accounts icon (bottom-left of VS Code). |
| `Updates were rejected because the remote contains work...` | Someone pushed first. Run `git pull`, sort out any conflict, then push. |
| `Need to specify how to reconcile divergent branches` | Run `git config --global pull.rebase false`, then `git pull` again. |
| A cell runs forever | Press **Interrupt** (■) at the top of the notebook. |
| Only have Google Colab | It works for the notebooks: in a Colab cell run `!git clone <your repository URL>` then `%cd <repository name>`. But set up your own laptop soon. |
