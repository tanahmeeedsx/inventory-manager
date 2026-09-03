# inventory-manager

A small e-commerce inventory system used as a self-practice Git and GitHub assignment — Round 2 of Git mastery training, covering the same 10 core skills as the original bongoDev assignment, applied to a different scenario.

---

## What I practiced here

**Identity and Setup**
Initialized the repository and configured Git identity so every commit is traceable.

**Secret Protection**
Created a `.env` file with a fake API key and added it to `.gitignore`. Also had to fix a real mistake here — the `.env` was accidentally committed before `.gitignore` was in place, which needed `git rm --cached .env` to stop tracking it without deleting the file itself.

**Branching**
Created `feature/payment-integration` to isolate payment gateway work from `main`.

**Staging Discipline**
Kept two unrelated config changes (`shipping.conf`, `tax.conf`) in two separate, focused commits.

**Remote Setup**
Connected to GitHub over SSH from the start this time, avoiding the HTTPS authentication issue from the first assignment.

**History Investigation**
Deliberately broke a `discount.txt` value, then used `git log -p` and `git blame` to trace exactly which commit and author caused it.

**Safety Net (Stash)**
Used `git stash -u` to shelve in-progress, untracked work (`checkout_flow.py`) while fixing an urgent bug in `tax.conf`, then restored it.

**Clean Merge (Squash)**
Combined three small "tweak" commits on `feature/payment-integration` into one clean commit on `main` using `git merge --squash`.

**Conflict Resolution**
Deliberately created a real merge conflict (making sure both branches actually diverged, to avoid a fast-forward) and resolved it manually in `discount.txt`.

**Disaster Recovery**
Recovered a commit after an accidental `git reset --hard` using `git reflog`.

---

## Issues Faced

A few real problems came up while working through this:

- `.env` got committed before `.gitignore` was set up, which needed `git rm --cached .env` to fix — deleting from Git tracking without deleting the actual file.
- (add any other issues you hit while completing the remaining tasks)

---

## Tools Used

Git, GitHub, SSH for authentication, and the Linux terminal.

---

## Status

- [ ] Task 01 — Setup & Identity
- [ ] Task 02 — Secret Protection
- [ ] Task 03 — Branching
- [ ] Task 04 — Staging Discipline
- [ ] Task 05 — Remote Setup
- [ ] Task 06 — History Investigation
- [ ] Task 07 — Safety Net (Stash)
- [ ] Task 08 — Clean Merge (Squash)
- [ ] Task 09 — Conflict Resolution
- [ ] Task 10 — Disaster Recovery
