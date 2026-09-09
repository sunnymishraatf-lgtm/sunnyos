# SunnyOS Foundation

## Purpose

Day 1 establishes the basic development environment, project structure, and development workflow for SunnyOS.

## Project Structure

```text
SunnyOS/
├── src/
├── tests/
├── docs/
├── scripts/
├── notes/
└── README.md
```

### Directory Responsibilities

* `src/` — source code
* `tests/` — test code
* `docs/` — technical documentation
* `scripts/` — development/helper scripts
* `notes/` — daily learning notes

## Development Environment

The project is being developed on Linux Mint using:

* VS Code
* GCC
* Git
* Make
* GDB

## Day 1 Program

Created:

```text
src/main.c
```

The program prints the SunnyOS Day 1 message and demonstrates the basic C development workflow.

## Compilation

The program was compiled using:

```bash
gcc -Wall -Wextra -Werror src/main.c -o sunnyos
```

The compilation completed successfully without warnings or errors.

## Execution

The program was executed using:

```bash
./sunnyos
```

Expected output:

```text
Sunnyos Day 1
Learn -> Build -> Test -> Document -> Commit
```

The program produced the expected output.

## Testing

### Strict Compilation

**PASS**

The program compiled successfully using `-Wall -Wextra -Werror`.

### Program Execution

**PASS**

The program produced the expected output.

### Edge Cases

**PASS**

The program does not accept user input, command-line arguments, files, or external data. It was executed repeatedly and produced consistent output.

## Design Decisions

The project uses separate directories for source code, tests, documentation, scripts, and learning notes. This keeps the project organized and makes it easier to expand as SunnyOS becomes more complex.

The Day 1 program is intentionally small because its purpose is to verify the development environment rather than implement OS functionality.

## Conclusion

The SunnyOS development environment is ready for future work. The basic compile, run, test, documentation, and Git workflow has been established.
