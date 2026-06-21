# 🗺️ Offensive Security Tool Development: C and C++ Roadmap

## ⚠️ Disclaimer

> **IMPORTANT:** The materials, source code, and links contained within this repository are intended solely for educational purposes, academic research, and authorized security assessments (penetration testing/red teaming). 
>
> Accessing, modifying, or interacting with target systems without prior, explicit, and written authorization from the system owner is illegal and strictly prohibited. The author of this repository assumes absolutely no liability for any misuse, damage, or legal consequences resulting from the application of the techniques, tools, or concepts documented herein. By utilizing these resources, you agree to operate in full compliance with all applicable local, national, and international laws.

---

## 🎯 Introduction
This roadmap is designed for penetration testers and security researchers aiming to master **C** and **C++** from scratch. 

Crucially, **C and C++ are treated as two independent tracks** in this guide. 
* **The C Track** focuses heavily on memory management, pointer arithmetic, buffer overflows, and low-level system interactions (the foundational vectors for memory corruption).
* **The C++ Track** focuses on modern offensive tool development, implant architecture, object-oriented reverse engineering, and advanced EDR evasion tactics.

---

# 🔴 TRACK 1: The C Programming Language
*Objective: Master memory layout, pointer mechanics, and fundamental exploitation (Memory Corruption & Shellcode).*

### Phase 1: Syntax & Core Foundations
Before hunting for memory leaks, you must understand how C compiles and executes.
* [**Learn-C Interactive Tutorial**](https://www.learn-c.org/en) - A fast, interactive way to grasp the baseline syntax without setting up a local environment.
* [**Complete C Programming Course**](https://github.com/kitretsusaisama/Complete-C-Programming-Course) - A structured GitHub repository containing comprehensive syntax foundations.
* [**Hacking in C 2019: C Fundamentals (PDF)**](https://cryptojedi.org/peter/teaching/hic2019/c_print.pdf) - Academic slide deck covering C basics with a slight lean towards low-level operations.

### Phase 2: The Danger Zone (Memory & Pointers)
This phase bridges standard programming and security vulnerabilities. Misunderstanding pointers is the root cause of spatial and temporal memory corruption.
* [**Hacking in C 2019: Pointers (PDF)**](https://cryptojedi.org/peter/teaching/hic2019/pointers_print.pdf) - A deep dive into pointer mechanics, arrays, and memory addresses.
* [**Secure Coding: Pointers and OS Files (PDF)**](https://docenti.ing.unipi.it/p.perazzo/teaching/intecs/02.secure-coding-pointers-osfiles.pdf) - University of Pisa lectures detailing how pointer mismanagement leads to exploitable states.
* [**Hacking in C 2020: Lectures & Handouts**](https://thomwiggers.nl/courses/hacking-in-c-2020/lectures/) | [(Direct PDF)](https://thomwiggers.nl/courses/hacking-in-c-2020/lectures/c-programming-handout-nonotes.pdf) - Video lectures and materials specifically mapping C programming constructs to security flaws.

### Phase 3: The Hacker's Mindset (Classic Exploitation)
Required reading for understanding how memory corruption is actually weaponized.
* [**Hacking: The Art of Exploitation (PDF - 2010)**](https://dn790005.ca.archive.org/0/items/hackingtheartofexploitation_202003/Hacking%20the%20art%20of%20Exploitation.pdf) - The absolute gold standard for understanding stack overflows, format strings, and the hacker mindset. 
* [**The Shellcoder's Handbook 2nd Edition (PDF)**](https://ia801309.us.archive.org/26/items/Wiley.The.Shellcoders.Handbook.2nd.Edition.Aug.2007/Wiley.The.Shellcoders.Handbook.2nd.Edition.Aug.2007.pdf) - The definitive guide to shellcode generation, exploitation methods across the C family, and OS-level vulnerability research.
* [**C for Hackers - Overview (PDF)**](https://elhacker.info/ebooks%20Joas/C%20for%20Hackers%20%E2%80%93%20Overview%20PT.pdf) - A practical guide analyzing different hacking tools written in C.

### Phase 4: Modern Linux Exploitation (GLIBC & Heap) 🔥 *[NEW]*
Modern Linux environments (Fedora, Kali, Parrot) heavily mitigate standard stack overflows. Mastering C today requires understanding the heap.
* [**how2heap (Shellphish)**](https://github.com/shellphish/how2heap) - The definitive repository for understanding modern GLIBC heap exploitation techniques (Use-After-Free, Fastbin Dup, Tcache poisoning) directly via C code execution.
* [**LiveOverflow Binary Exploitation Series**](https://www.youtube.com/playlist?list=PLhixgUqwRTjxglIsyE-Sq65Bc9AWgj5Rz) - Exceptional visual breakdowns of C memory corruption, Linux binary reversing, and dynamic analysis using GDB.

### Phase 5: Advanced Engineering & Win32 API
Transitioning from standard terminal programs to malware development and system-level manipulation.
* [**Expert C Programming: Deep C Secrets (PDF)**](https://progforperf.github.io/Expert_C_Programming.pdf) - Advanced compiler behavior, memory alignment, and the difference between arrays and pointers at the hardware level.
* [**Getting Started with Win32 API**](https://r3dlevy.github.io/blog/offensive-development-with-c-and-c-getting-started-with-win32-api-and-practical-examples) - Crucial bridge tutorial for interacting directly with the Windows API (process injection, memory allocation).
* [**OffensiveC Repository**](https://github.com/impongsup/OffensiveC) - A collection of raw offensive C code snippets and tooling.

---

# 🔵 TRACK 2: The C++ Programming Language
*Objective: Master modern OOP, EDR evasion, dynamic payload delivery, and binary reverse engineering.*

### Phase 1: Modern C++ Theory
C++ is vastly different from C under the hood (Name Mangling, vTables, Object Orientations).
* [**Learn-CPP**](https://www.learn-cpp.org/) - The industry standard tutorial for up-to-date C++ fundamentals.
* [**Meeting C++ 2025 Slides (PDF)**](https://meetingcpp.com/mcpp/slides/2025/meeting_cpp990082.pdf) - Excellent deep dive into modern C++ theory and architectural paradigms. (Very Nice for theory!!!)

### Phase 2: Offensive Tool Development
Weaponizing C++ for red teaming, focusing on stealth and Windows internals.
* [**OffensiveCpp Repository**](https://github.com/lsecqt/OffensiveCpp) - Practical, modern examples of weaponizing C++ (beacons, process injection, keyloggers).

### Phase 3: Defense Evasion & Windows Internals 🔥 *[NEW]*
Modern AV/EDR solutions monitor APIs via user-land hooking. C++ is the language of choice for bypassing these controls, but you need undocumented structures to do it smoothly.
* [**How to Unhook a DLL Using C++ (ired.team)**](https://www.ired.team/offensive-security/defense-evasion/how-to-unhook-a-dll-using-c++) - Step-by-step guide on mapping a clean `ntdll.dll` from disk to overwrite in-memory hooks.
* [**Evasion Techniques Video**](https://www.youtube.com/watch?v=OpkLuvx1dw4) - Visual breakdown of modern defense evasion concepts.
* [**The Vergilius Project**](https://www.vergiliusproject.com/) - A massive, searchable database of undocumented Windows kernel and user-mode C/C++ structures. Absolutely critical when writing custom syscalls or advanced C++ malware.
* [**ReactOS Source Code**](https://github.com/reactos/reactos) - The best way to understand how the Windows API operates under the hood is to read the source code of its open-source clone.

### Phase 4: Reverse Engineering C++
Understanding how C++ compiles is critical for reverse engineering malware or discovering zero-days.
* [**Reverse Engineering C++ (Black Hat Paper)**](https://blackhat.com/presentations/bh-dc-07/Sabanal_Yason/Paper/bh-dc-07-Sabanal_Yason-WP.pdf) - A classic, highly technical breakdown of how compilers implement C++ features (vTables, `this` pointers) and how to identify them in IDA Pro/Ghidra.

---

# 🟢 TRACK 3: Related OffSec Languages & Environments
Building out auxiliary skills for living-off-the-land, exploit automation, and cross-platform payload generation.

### Exploit Automation (Python) 🔥 *[NEW]*
*While C/C++ are used for the payloads and vulnerabilities, Python is the industry standard for delivering them.*
* [**Pwntools (Python)**](https://github.com/Gallopsled/pwntools) - A CTF framework and exploit development library. If you are attacking a vulnerable C binary, you should be writing your exploit script in Python using Pwntools to format the memory addresses and interact with the socket/process.

### Go (Golang)
*Go is incredibly popular in modern OffSec due to its easy cross-compilation and speed.*
* [**Black Hat Go (PDF)**](https://dl.hiva-network.com/Library/security/Black-Hat-Go_Go-Programming-For-Hackers-and-Pentesters.pdf) - Go Programming for Hackers and Pentesters. 

### Bash Scripting
*Essential for automation, post-exploitation enumeration, and living-off-the-land.*
* [**Black Hat Bash (PDF)**](https://elhacker.info/manuales/Lenguajes%20de%20Programacion/Black%20Hat%20Bash.pdf) - Weaponizing shell scripts for penetration testing.

### Virtualization & Hacking Labs 🔥 *[NEW]*
*You need a safe environment to test these C/C++ concepts without destroying your host machine.*
* [**Exploit.Education**](https://exploit.education/) - Downloadable virtual machines (Phoenix, Nebula) perfectly suited for VirtualBox or VMware Workstation Pro. They are specifically designed to practice memory corruption on C binaries at various difficulty levels.
* [**Learning-C Tasks (h0mbre)**](https://github.com/h0mbre/Learning-C) - Excellent, bite-sized tasks for beginners writing C utilities.
* [**Prof. Lettieri's Hacking Lab**](https://lettieri.iet.unipi.it/hacking/) - Extremely high-value repository of hacking environments, exploit templates, and university-level CTF materials.
* [**Radboud University & UniPi Materials**](https://www.cs.ru.nl/E.Poll/hacking/) - Academic exercises for vulnerability discovery.

### General OffSec & Embedded
* [**Offensive Security Toolkit**](https://github.com/NextGenSec-Github/Offensive-Security) - A broad aggregation of offensive tools and reference material.
* [**All-In-One Computer Programming Bible (PDF)**](https://ia802900.us.archive.org/3/items/All.One.Computer.Programming.Bible.Ebook.13/All.One.Computer.Programming.Bible.Ebook.13.pdf) - A general reference manual spanning Mixed C++, Raspberry Pi, and hardware interfacing.
