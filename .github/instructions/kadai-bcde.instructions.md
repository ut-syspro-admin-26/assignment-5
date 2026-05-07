---
applyTo: "kadai-bcde/**"
---

# kadai-b (optional)

**Problem statement:** Add foreground job control to `ish`.

**Requirements:**

- Assign a new process group ID to each job.
- Make the currently running job the foreground process group of the terminal (use `tcsetpgrp(3)`).
- SIGINT must not terminate `ish` itself.

# kadai-c (optional)

**Problem statement:** Add background execution (`&`) to `ish`.

**Requirements:**

- Commands ending with `&` must run in the background, returning the prompt immediately.
- Background processes must not become zombies (reap them appropriately).
- Background processes must not receive signals from the keyboard.

# kadai-d (optional)

**Problem statement:** Add Ctrl-Z (suspend) and the built-in command `bg` to `ish`.

**Requirements:**

- Ctrl-Z must suspend the foreground job and return `ish` to the foreground; `ish` itself must
  not be suspended by Ctrl-Z.
- `bg` resumes one suspended background job.

**Optional requirements:**

- `bg` accepts a job ID as an argument to resume a specific job.

# kadai-e (optional)

**Problem statement:** Add the built-in command `fg` to `ish`.

**Requirements:**

- `fg` brings one background job to the foreground

**Optional requirements:**

- `fg` accepts a job ID as an argument to bring a specific job to the foreground.
