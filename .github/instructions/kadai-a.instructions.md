---
applyTo: "kadai-a/**"
---

**Problem statement:** Create a C program named `count` that counts how many times SIGINT
(Ctrl+C) has been received and exits when the count reaches 10.

**Requirements:**

- The command `make count` produces the executable.
- Use `sigaction(2)` to register the SIGINT handler.
- Increment a global variable `count` inside the signal handler.
- Monitor `count` outside the signal handler (not inside it), and print "exit" to stdout and
  terminate the program when `count` reaches 10 or more.
- Do not call async-signal-unsafe functions inside the signal handler.
- Declare `count` with the `volatile` modifier so the program works correctly even when compiled
  with optimization flags such as `-O3`.
