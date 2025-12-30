# Shell Project Writeup — Unix-like Command Interpreter - NO CODE

## High-level description

This project implements a small **Unix-like interactive shell**: it reads a user’s command line input, parses it into a structured form (commands, arguments, operators), and then executes programs using standard Unix process and file-descriptor mechanisms. The shell behaves like a lightweight subset of common shells (e.g., `bash`) with support for pipelines, redirection, background jobs, and typical interactive usability features.

## Course / policy note

Completed for **Purdue CS252 (Spring 2025)**. Source code is **not publicly available** in order to respect course and academic integrity policies.

## Implemented functionality

### Core execution
- Runs external programs with arguments
- Foreground execution with correct waiting behavior
- Background execution using `&`

### Pipelines
- Multi-stage pipelines using `|` (e.g., `a | b | c`)
- Correct pipe setup/teardown between processes

### I/O redirection
- Redirects `stdin`, `stdout`, and `stderr`
- Supports overwrite vs. append for output redirection
- Supports combined redirection patterns (where applicable)

### Built-in commands
- Standard shell builtins (e.g., `cd`, `exit`, and common environment-related behavior)

### Interactive behavior & job handling
- Prompt in interactive mode; test-friendly behavior in non-interactive mode
- Signal behavior consistent with interactive shells (e.g., Ctrl-C handling for foreground jobs)
- Background job cleanup and completion reporting (no zombie accumulation)

### Expansions & convenience features
- Quoting and escaping for arguments with spaces/special characters
- Environment variable expansion (including common special expansions)
- Tilde expansion (`~`)
- Wildcard/glob expansion (`*`, `?`)
- Line editing and command history
- Path/command completion
- Startup initialization behavior (e.g., reading a shell rc file), if configured
