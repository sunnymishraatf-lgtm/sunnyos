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


# Day 2 — What an Operating System Does

## What I Learned

An operating system manages computer hardware and provides
services that applications use.

The five major responsibilities of an operating system are:

1. Process Management
2. Memory Management
3. File Management
4. Device Management
5. Security and Protection

## Kernel vs User Space

User space is where normal applications run, such as
Chrome, VS Code, and terminal programs.

Kernel space is where the operating system's core runs.
The kernel has privileged access to hardware and system resources.

The separation exists to protect the system from buggy or
malicious applications.

Applications request privileged OS services through system calls.

## What an OS Does Not Do

An operating system is not the same thing as an application.

Applications such as Chrome, VS Code, and games run on top
of the operating system and use OS-provided services.

## OS Stack

User
↓
Applications
↓
System Calls
↓
Kernel
↓
Hardware

## Five Pillars and SunnyOS Roadmap

| Pillar | SunnyOS Area |
|---|---|
| Processes | Process management and CPU scheduling |
| Memory | Memory management and virtual memory |
| Files | File systems |
| Devices | Device drivers and I/O |
| Security | Protection and isolation |

## Practical Work

Created a simple program/diagram showing the operating
system stack and its major responsibilities.

## Testing

- Compilation with `-Wall -Wextra -Werror`: PASS
- Program execution: PASS
- Edge-case testing: PASS

## Commands Used

```bash
gcc -Wall -Wextra -Werror main.c -o main
./main



# Day 3 — From Bits to Bytes

## What I learned

Today I learned how computers represent numbers and text using bits and bytes.

### Binary

Binary is base 2 and uses only `0` and `1`.

8 bits make 1 byte. An unsigned byte can represent values from 0 to 255.

### Hexadecimal

Hexadecimal is base 16 and uses:

`0-9` and `A-F`

One hexadecimal digit represents 4 bits, so two hexadecimal digits represent one byte.

Examples:

* `65` decimal = `0x41` hexadecimal
* `255` decimal = `0xFF` hexadecimal
* `0x41` = binary `01000001`

### Two's complement

Two's complement is used to represent signed integers.

For an 8-bit signed integer, the range is:

`-128` to `127`

For example:

`11111111` represents `-1`.

Adding 1 to the maximum signed 8-bit value:

`01111111 + 1 = 10000000`

causes overflow and produces `-128` when interpreted as a signed 8-bit value.

### ASCII and UTF-8

ASCII maps characters to numeric values.

For example:

`A = 65 = 0x41`

UTF-8 is a variable-length encoding used for Unicode characters. A character can occupy between 1 and 4 bytes, so the number of characters is not always equal to the number of bytes.

## What I built

I created a C program that prints decimal and hexadecimal representations of byte values.

I also created `TEST.BIN` containing `ABC` and inspected its bytes using `od`.

The file produced:

`41 42 43`

which represents:

* `A` → `0x41`
* `B` → `0x42`
* `C` → `0x43`

## Commands used

```bash
gcc -Wall -Wextra -Werror day3.c -o bits
./bits
printf 'ABC' > TEST.BIN
od -An -tx1 TEST.BIN
```

## Verification

* Strict compilation: PASS
* Program execution: PASS
* Decimal/hex conversion tests: PASS
* Byte inspection with `od`: PASS
* Edge cases tested: `0`, `1`, `15`, `16`, `65`, `127`, `255`

## Design decisions

I used `unsigned char` for byte-sized values because an unsigned 8-bit value can represent `0` through `255`.

I used strict compiler flags to catch warnings and keep the code clean.

## Result

I can now convert small values between decimal, hexadecimal, and binary and understand how numbers and basic text are represented as bytes in memory.
