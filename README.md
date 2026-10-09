# MSc Fintech · Tech Skills Workshop (Sessions 3 & 4)

Hands-on material for two sessions:

- **Session 3: Introduction to Software Development.** Set up your laptop, version control with Git and GitHub, how software gets built, and debugging.
- **Session 4: Handling Big Data.** Data types, loading and cleaning messy files, and what to do when data is too big for Excel.

The setup you do here (**Python + VS Code + Git + GitHub**) is the same one you can use for the rest of your programme. It isn't just for today.

---

## Files

| File | What it is |
|---|---|
| `SETUP.md` | Step-by-step setup for Windows, Mac and the browser fallback |
| `00_setup_check.ipynb` | Run this to check your setup. Green = ready |
| `S3_bug_hunt.ipynb` | Session 3 debugging exercises (pairs) |
| `S4_1_data_types_and_dataframes.ipynb` | Session 4 code-along: types, loading and cleaning a messy file |
| `S4_2_too_big_for_excel.ipynb` | Session 4: making and handling a 2-million-row file |
| `S4_3_pair_challenge.ipynb` | Session 4 pair challenge on real salary data |
| `S4_4_optional_api_stock_data.ipynb` | Optional: getting stock prices from an API |
| `TEAM.md` | Used in the Session 3 pair exercise |
| `data/` | All data files (the big one is generated on your laptop and never uploaded) |

---

## Session 3 · Git exercise (solo)

1. **Get your own copy.** On the workshop repository page on GitHub, click **Use this template → Create a new repository**. Name it `fintech-workshop-yourname` and click **Create repository**.
2. **Clone it.** In VS Code press `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`), type **Git: Clone**, choose **Clone from GitHub**, sign in when the browser opens, and pick your new repository. Save it somewhere you'll find again (e.g. *Documents*), then click **Open**.
3. **Tell Git who you are** (only once per laptop). Open the terminal in VS Code (**View → Terminal**) and run:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "the-email-you-used-for-GitHub"
   git config --global pull.rebase false
   ```
4. **Check your setup.** Open `00_setup_check.ipynb`, choose your Python (see SETUP.md), and run it. If VS Code says the Python *requires the ipykernel package* and installing doesn't work, see *Common problems* in SETUP.md.
5. **Make a change.** Fill in the *About me* section at the bottom of this README and save.
6. **Stage, commit, push**, in the VS Code terminal:
   ```bash
   git status
   git add README.md
   git commit -m "Add my introduction"
   git push
   ```
7. **Check.** Refresh your repository page on GitHub. Your change is there. Click **Commits** to see the history.

## Session 3 · Pair exercise: create and fix a merge conflict

Person **A** and Person **B**:

1. **A:** on your repository page, go to **Settings → Collaborators → Add people** and add B's GitHub username.
2. **B:** accept the invite (check your email, or go to github.com/notifications), then clone **A's** repository (Git: Clone, paste the URL).
3. **Both:** open `TEAM.md` and write a *different* team motto on the motto line. Save.
4. **B:** `git add TEAM.md` → `git commit -m "B's motto"` → `git push`. This one works.
5. **A:** `git add TEAM.md` → `git commit -m "A's motto"` → `git push`. **Rejected**: GitHub has a change you don't have yet.
6. **A:** `git pull`. Git reports a **CONFLICT** in `TEAM.md`. VS Code highlights both versions. Choose *Accept Current*, *Accept Incoming* or *Accept Both*, or edit by hand, then save.
7. **A:** `git add TEAM.md` → `git commit -m "Merge mottos"` → `git push`.
8. **B:** `git pull` to see the merged result. Then swap roles and try again on B's repository.

This is what happens on every real team: two people change the same line, Git spots it, and a person decides what's right.

## Session 4

Open the notebooks in order (`S4_1`, `S4_2`, `S4_3`). At the end, commit and push your work as in Session 3.

---

## After the workshop

- Keep this repository. It's a working example of everything above.
- Apply for the free **GitHub Student Developer Pack** with your university email: https://education.github.com/pack
- Further reading:
  - *Pro Git* (free online): https://git-scm.com/book
  - *The Missing Semester of Your CS Education* (MIT): https://missing.csail.mit.edu/
  - *Python for Data Analysis*, 3rd ed., Wes McKinney (free online): https://wesmckinney.com/book/
  - Robert C. Martin, *Clean Code*

---

## About me

- **Name:**
- **What I did before this MSc:**
- **One thing I want to be able to do with code by the end of the programme:**
