# Rules

These are the rules that should be applied in every scenario.

- When making technical decisions, do not give much weight to development cost.
  Instead, prefer quality, simplicity, robustness, scalability, and long term maintainability.
- Apply that same high standard to engineering excellence: lint, test failures, and test flakiness.
  If you see one, even if it is not caused by what you are working on right now, still get it fixed.
- Never manually modify files that are marked as auto-generated (e.g. generated Supabase types).
  Regenerate them from their source instead.
- When end-to-end testing a product, be picky about the UI you see and be obsessed with pixel perfection.
  If something clearly looks off, even if it is not directly related to what you are doing, try to get it fixed along the way.
- When working on something, don't just patch locally.
  Step back and ask whether a broader change, or even a full migration, would result in higher quality code.
  Don't be afraid to criticize what already exists in the codebase and propose reworking it.
- Never take the surrounding file or codebase as the standard to match.
  If what is already there is below the bar, rewrite it instead of imitating it.
  Turning dirty code into clean code is always appreciated.
- Always think in terms of best practices, and always critique what you are doing while you do it.
  Keep asking what could be done better.
  It is fine to start down one path and switch to a better approach once reading the files or writing the code reveals it; act like a real developer, not someone blindly executing instructions.
- Proactively invoke a matching skill whenever a task fits its description, without waiting to be told.
  If a skill clearly applies, run it on your own; only ask first when more than one skill could reasonably apply and the choice matters.
- Always ask before committing or pushing.
  Unless the most recent instruction explicitly asked to commit or push, confirm with me first instead of doing it on your own.
- Never create a merge commit: no `git merge`, no merging `git pull`.
  Integrate upstream changes with `git pull --rebase` (or `git rebase`), so history stays linear.
  If a rebase would rewrite a commit already pushed to another branch, ask me before force-pushing instead of merging.
- Write commit messages as a single line stating what the change does.
  No body, no why, no when.
- Never add yourself as a co-author of a commit.
  No `Co-Authored-By` trailer, no generated-with footer.
- In markdown and comments, break the line after every sentence.
  Stay brief and leave out the thought process.
  Every extra line is one more thing to keep accurate over time.
- Comments are banned: never use them.
  Fix the naming or the structure instead, so the logic, function, or data is clear on its own.
  If a decision or a precision needs to be recorded, put it in documentation instead.
- Never use the em dash character ("—") anywhere: not in prose, code, comments, commit messages, or documentation.
  Overusing it is a tell-tale sign of AI writing.
  Use a comma, colon, parentheses, or two separate sentences instead.
  The same applies to the en dash ("–") in prose; reserve the plain hyphen ("-") for ranges and compound words.
