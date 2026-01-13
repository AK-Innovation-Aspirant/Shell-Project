# Unix-like Command Interpreter (Interactive Shell)

## High-level description

This project implements a small **Unix-like interactive shell**: it reads a user’s command line input, parses it into a structured form (commands, arguments, operators), and then executes programs using standard Unix process and file-descriptor mechanisms. The shell behaves like a lightweight subset of common shells (e.g., `bash`) with support for pipelines, redirection, background jobs, and typical interactive usability features.

## Capabilities (High Level)
- **Program execution:** runs external commands with arguments in a standard Unix process model.
- **Composability:** supports connecting programs together and directing input/output through common shell mechanisms.
- **Interactive usability:** provides a prompt-oriented workflow and handles user interrupts in a way that matches typical terminal expectations.
- **Job handling:** supports running tasks asynchronously and managing their lifecycle without leaking system resources.
- **Convenience features:** includes common command-line quality-of-life behaviors (e.g., interpreting quoted strings and expanding user-friendly shortcuts).

## What I Learned
- **Processes & file descriptors:** how process creation, waiting, and descriptor wiring enable shells to compose programs.
- **Parsing & ambiguity:** why shell syntax is deceptively complex and how parsing choices affect semantics.
- **Signals & terminal control:** how interactive programs respond to interrupts and how shells coordinate foreground/background behavior.
- **Robustness:** handling malformed input, failed execs, and cleanup paths without leaving zombies or broken terminal state.

## Notes
This repository intentionally omits implementation details that would function as a step-by-step solution. It is meant to document scope and learning outcomes rather than provide a reference implementation.

