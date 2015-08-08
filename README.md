Quickstart
==========

Requirements:

- A C compiler

- GNU make

- A POSIX compliant OS (Linux or Mac OS)

To built the zeta VM, go to the source directory and run `make`

Tests can then be run using the test command: `./zeta --test`

The Zeta Programming Language
=============================

This is an implementation of a Virtual Machine (VM) for the zeta programming
language I'm working on in my spare time. Zeta draws inspiration from LISP,
Smalltalk, ML, JavaScript and C. The language is currently at the early
prototype stage, meaning the syntax and semantics are likely to change a lot
in the coming months.

Planned features of the language include:

- Dynamic typing

- Garbage collection

- A user-extensible grammar, giving programmers the ability to define new syntactic constructs

- No distinction between statements and expression, everything is an expression, as in LISP

- Functional constructs such as map and foreach

- A module system

- An easy to use canvas library to render simple 2D graphics

The Zeta Virtual Machine
========================

I've chosen to implement the VM core in pure C, for the following reasons:

- To make low-level details explicit (for instance, the layout of hosted objects in memory)

- To avoid hidden sources of overhead

- To avoid dependence on non-portable tools and languages. GCC is available on almost every platform in existence

The zeta implementation will be largely self-hosted. The core VM will
implement an interpreter in C, but the garbage collector and zeta JIT
compiler will be written in the zeta language itself.

