---
name: auto-pull
description: Automatically pull before editing tracked project files and before every git push in this project.
---

# Pull before edits and pushes

The user authorizes automatic synchronization in this project without asking again.

- At the start of every task that creates, modifies, or deletes code or other version-controlled files, inspect Git status and the current branch's upstream, then run `git pull --no-rebase --no-edit` before the first edit. One initial pull per task is sufficient; do not pull on every save.
- Before every `git push`, including retries, run `git pull --no-rebase --no-edit` again, even if the initial pull succeeded. Complete task checks and commit first, then perform this pull.
- Use the current branch and existing upstream. If no upstream exists but origin has a same-named branch, use `git pull --no-rebase --no-edit origin <current-branch>`. If there is no identifiable remote branch, stop and report the missing synchronization target rather than guessing.
- Integrate remote changes through merges, without rebasing, rewriting history, or force pushing. If pull fails, conflicts, or is blocked by local changes, preserve the state and stop dependent editing or pushing. Do not automatically stash, reset, discard changes, or repeatedly retry.
- If the pre-push pull brings new changes, inspect the integration and rerun affected checks before pushing.
- This skill authorizes synchronization only. Follow the project's auto-commit-push skill and the user's current instructions for committing and pushing.
