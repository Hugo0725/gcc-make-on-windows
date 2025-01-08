# Setting Up GCC and Make on Windows: A Step-by-Step Guide

This repository provides a step-by-step guide on how to install GCC and Make on a Windows system, create a basic `main.c` program, and use Makefiles to compile and manage the build process. It is designed for beginners who want to learn the fundamentals of using GCC and Make on Windows.

---

## Install GCC Compiler

1. Visit the [MinGW website](https://www.mingw-w64.org/downloads/) or directly download from the [MinGW GitHub repository](https://github.com/niXman/mingw-builds-binaries/releases).
2. Download the file `x86_64-14.2.0-release-posix-seh-ucrt-rt_v12-rev0.7z` (recommended).
3. Extract the `.7z` file to a directory on your disk.
4. Add the path to `gcc.exe` to your environment variables:
   - Example: Add `C:\mingw64\bin` to the `PATH` environment variable.

> **Recommendation Summary**
> - **Architecture**: Use `x86_64` for 64-bit systems.
> - **Thread Model**: Choose `POSIX` for cross-platform support.
> - **Exception Handling**: Prefer `SEH` for modern Windows development.
> - **C Standard Library**: Opt for `UCRT` for the latest features.

---

## Install Make

1. Download `Complete package, except sources` from the [Make for Windows](https://gnuwin32.sourceforge.net/packages/make.htm).
2. Add the path to `make.exe` to your environment variables:
   - Example: Add `C:\Program Files (x86)\GnuWin32\bin` to the `PATH` environment variable.

---

## Verify Toolchain Installation

1. Open `cmd.exe`.
2. Verify `gcc` version:
    ```bash
    gcc --version
    ```
    Expected output:
    ```
    gcc (x86_64-posix-seh-rev0, Built by MinGW-Builds project) 14.2.0
    Copyright (C) 2024 Free Software Foundation, Inc.
    ```
3. Verify `make` version:
    ```bash
    make --version
    ```
    Expected output:
    ```
    GNU Make 3.81
    Copyright (C) 2006 Free Software Foundation, Inc.
    This program built for i386-pc-mingw32
    ```

---

## Build and Run Example

1. Ensure your project directory contains the following files:
    ```
    /project-directory
    ├── main.c
    └── Makefile
    ```
2. Open `cmd.exe` and navigate to your project directory:
    ```bash
    cd path\to\your\repository
    ```
3. Run the `make` command:
    ```bash
    make
    ```
4. Confirm that `main.exe` is successfully built in the project directory.
5. Execute the program:
    ```bash
    main.exe
    ```

---

This guide should help you quickly set up GCC and Make on Windows and start building projects. If you encounter any issues, feel free to reach out or consult the official documentation!
