# MiniLibC — x86_64 Assembler

> Epitech project — B-ASM-400 (B4, *x86_64 Assembler*)

A reimplementation of a subset of the C standard library, written **entirely in x86-64 assembly** and compiled into a dynamic ELF library (`libasm.so`). The goal is to understand, at the lowest level, how the everyday functions of the C library actually work — and how dynamic libraries can override them at runtime via `LD_PRELOAD` (weak binding).

## Implemented functions

Each function follows the exact behaviour of its `man` page:

`strlen` · `strchr` · `strrchr` · `memset` · `memcpy` · `strcmp` · `memmove` · `strncmp` · `strcasecmp` · `strstr` · `strpbrk` · `strcspn`

## Tech stack

- **Language:** x86-64 Assembly
- **Output:** dynamic ELF library `libasm.so`
- **Build:** `Makefile` (`make`, `re`, `clean`, `fclean`)

## Build

```sh
make
```

## Usage

The produced library can be preloaded to replace the system implementations:

```sh
LD_PRELOAD=./libasm.so your_program
```

## What I learned

- Writing and calling functions following the System V AMD64 calling convention
- Manual register and stack management
- How dynamic linking and symbol resolution (weak binding) work under the hood
