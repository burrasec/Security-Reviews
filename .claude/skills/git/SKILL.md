---
name: git
description: Commit and push changes in this repo. Stages everything, commits with a short message, rebases onto origin/main, then pushes.
argument-hint: "[optional short commit message]"
---

When the user asks to commit and push, run:

`git add -A && git commit -m "<short message>" && git pull --rebase origin main && git push origin main`

The `pull --rebase` step integrates any remote-only changes before pushing.

If the user supplied a message as the argument, use it verbatim. Otherwise, derive a concise message from the staged changes.
