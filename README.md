# Embedded C Programming Design Patterns

This repository contains PDF documents, reference materials, and design templates from Martin Schröder's **"Embedded C Programming Design Patterns"** course. 

It covers architectural approaches tailored for the Embedded Systems world, utilizing the C programming language not just for low-level hardware manipulation, but to build **scalable, testable, and modern (SOLID) software architectures**.

## Repository Objective
To apply Object-Oriented Programming (OOP) principles in C; minimizing hardware coupling, enabling robust Unit Testing (via Mocking), and establishing software architectures that fully comply with **MISRA C** and **ISO 26262 Functional Safety** standards.

## Core Design Patterns Covered

* **Encapsulation & Opaque Pointer:** Creating secure and abstracted APIs by hiding the internal structure of `struct` data types from the application layer (Information Hiding).
* **Virtual API (Polymorphism) & Factory Pattern:** Achieving polymorphism in C via Function Pointers and designing a clean, decoupled Hardware Abstraction Layer (HAL).
* **Inheritance via Composition (`CONTAINER_OF`):** Building secure inheritance hierarchies in C using the `CONTAINER_OF` macro, which forms the foundation of the Linux Kernel and Zephyr RTOS.
* **State Machine Pattern:** Moving away from complex and unmaintainable `switch-case` blocks to design modular and deterministic State Machines managed via function pointers.
* **Concurrency & Synchronization:** Mutex and Spinlock architectures to prevent Race Conditions in multi-core microcontrollers and Interrupt Service Routines (ISRs).
* **Subsystem & Service Architectures:** Layered and independent service-based system design to prevent spaghetti code and circular dependencies.

## ⚙️ Why These Patterns? (Engineering Principles)
1. **Zero Dynamic Memory:** All architectures are designed with completely static memory allocation, strictly avoiding `malloc` and `free`. This completely eliminates the risks of memory leaks and memory fragmentation.
2. **Hardware Isolation:** By removing the software's direct dependency on the target hardware (ECU), the codebase can be easily subjected to MiL/SiL tests on a Host PC using mocked hardware interfaces.
3. **Safety-Critical Compliance:** Provides a highly reliable coding standard for fault-intolerant and safety-critical projects in the automotive, aerospace, and medical industries.

---
* **Note:** The educational materials, reference documents, and core concepts in this repository are based on Martin Schröder's course content. This repository serves as a reference guide (cheatsheet) for engineers focusing on robust embedded software architecture.*
