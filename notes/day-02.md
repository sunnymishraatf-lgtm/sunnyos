Sketch for os

┌─────────────────────────────┐
│          USER               │
└──────────────┬──────────────┘
               │
┌──────────────▼──────────────┐
│       APPLICATIONS          │
│ Chrome / VS Code / Games    │
└──────────────┬──────────────┘
               │
          System Calls
               │
┌──────────────▼──────────────┐
│        KERNEL               │
│                            │
│ Process Management         │
│ Memory Management          │
│ File Systems               │
│ Device Drivers             │
│ Security                   │
└──────────────┬──────────────┘
               │
┌──────────────▼──────────────┐
│          HARDWARE           │
│ CPU / RAM / SSD / Devices  │
└─────────────────────────────┘



kernal vs user space


┌──────────────────────────┐
│       USER SPACE         │
│                          │
│ Chrome                   │
│ VS Code                  │
│ Terminal                 │
│ Your programs            │
│                          │
├──────────────────────────┤
│       KERNEL SPACE       │
│                          │
│ Process management       │
│ Memory management        │
│ File systems             │
│ Drivers                  │
│ Networking               │
│ Hardware control         │
└──────────────────────────┘
             │
             ▼
          Hardware



Keyboard
   ↓
Hardware signal
   ↓
Keyboard controller
   ↓
Driver
   ↓
Kernel
   ↓
Application





five pillar of os 
*-processes
*-Memory
*-Files
*-Devices
*-security


future  area--  

| OS Pillar | Future SunnyOS Area                 |
| --------- | ----------------------------------- |
| Processes | Process management & CPU scheduling |
| Memory    | Virtual memory & memory management  |
| Files     | File systems                        |
| Devices   | Drivers & I/O                       |
| Security  | Protection & isolation              |



-Wall -Wextra -Werror

-Wall

Enables many common compiler warnings.

-Wextra

Enables additional warnings.

-Werror

Turns warnings into errors.



ex--
gcc -Wall -Wextra -Werror main.c -o main




Compilation tells you:

"The compiler accepted the code."

Execution tells you:

"The program actually behaves correctly."

Those are different things.



                    USER
                     │
                     ▼
              APPLICATIONS
       ┌─────────┬─────────┬─────────┐
       │ Chrome  │ VS Code │ Your App│
       └─────────┴─────────┴─────────┘
                     │
                     │ System Calls
                     ▼
              ┌─────────────┐
              │   KERNEL    │
              │             │
              │ Processes   │
              │ Memory      │
              │ Files       │
              │ Devices     │
              │ Security    │
              └──────┬──────┘
                     │
                     ▼
                 HARDWARE
       ┌────────┬────────┬────────┐
       │  CPU   │  RAM   │  SSD   │
       └────────┴────────┴────────┘




Questions---
Question 1

What is an operating system?

Expected idea:

Software that manages hardware resources and provides services/interfaces for applications.

Question 2

What is a process?

A running instance of a program.

Question 3

Why does the OS manage memory?

To allocate memory to programs, manage virtual/physical memory, and prevent programs from interfering with each other.

Question 4

What does a file system do?

It organizes and manages persistent data as files/directories and provides applications with a usable storage interface.

Question 5

What is a device driver?

Software that allows the OS to communicate with a particular hardware device.

Question 6

Why separate user space and kernel space?

To protect the system and isolate applications from critical OS and hardware operations.

Question 7

How does an application request privileged OS services?

Through system calls.

Question 8

Is Chrome part of the operating system?

No. Chrome is an application that uses OS services.