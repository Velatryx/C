# 💻 Interactive Ethical Hacking & Secure C/C++ Developer Lab Guide

## ⚠️ Disclaimer

> **IMPORTANT:** The materials, source code, and links contained within this repository are intended solely for educational purposes, academic research, and authorized security assessments (penetration testing/red teaming). 
>
> Accessing, modifying, or interacting with target systems without prior, explicit, and written authorization from the system owner is illegal and strictly prohibited. The author of this repository assumes absolutely no liability for any misuse, damage, or legal consequences resulting from the application of the techniques, tools, or concepts documented herein. By utilizing these resources, you agree to operate in full compliance with all applicable local, national, and international laws.

---

## 🎯 Methodology: How to Use This Lab Manual
This guide is structured into an **interactive, project-based lab manual**. 
Instead of reading textbooks cover-to-cover, this format prompts you to write code immediately. Each module sets a target task, identifies the specific reference link from your collection to study, and points directly to where the solutions or source code implementations are located.

---

# 🔴 PART 1: Interactive C Track (Vulnerability Discovery & Memory Mechanics)

## Module 1: Baseline Syntax & Systems Utility Building
Before analyzing memory space, you must understand how C structures data and interfaces with the operating system.

### 🛠️ Interactive Lab 1.1: Standard Syntax & Code Execution
*   **Your Objective:** Write, compile, and execute fundamental C applications focusing on arrays, loops, and file parsing.
*   **Study & Interactive Platform:** Complete the browser-based challenges on the [Learn-C Interactive Platform](https://www.learn-c.org/en).
*   **Local Exercises & Solutions:** Clone the [h0mbre/Learning-C Repo](https://github.com/h0mbre/Learning-C). Complete challenges 1 through 8. The answers and reference templates are stored directly inside each challenge's solution folder.

---

## Module 2: Low-Level Memory Manipulation & Corruption Fundamentals
Understanding exactly how the stack behaves when memory constraints are deliberately broken.

### 🛠️ Interactive Lab 2.1: The Wargame Environment (OverTheWire)
*   **Your Objective:** Connect to a remote Linux server via SSH and solve progressive technical challenges to retrieve access flags, transitioning from basic Linux commands to binary manipulation.
*   **Interactive Platform:** [OverTheWire: Wargames](https://overthewire.org/wargames/).
*   **The Path:** 
    1.  **Bandit:** Start here to master the Linux command-line interface.
    2.  **Leviathan:** Transition into basic reverse engineering and identifying vulnerabilities in programs.
    3.  **Narnia:** Begin hands-on binary exploitation, specifically learning how buffer overflows operate in a live environment.
*   **Supporting Material:** [The Shellcoder's Handbook PDF](https://ia801309.us.archive.org/26/items/Wiley.The.Shellcoders.Handbook.2nd.Edition.Aug.2007/Wiley.The.Shellcoders.Handbook.2nd.Edition.Aug.2007.pdf) (Read Chapter 1 & 2 for architecture limits).

### 🛠️ Interactive Lab 2.2: Advanced Heap Manipulation & GLIBC Mechanics
*   **Your Objective:** Write C routines that manipulate dynamic memory space (`malloc`/`free`) to observe how modern allocators handle data and how mismanagement leads to vulnerabilities.
*   **Core Concepts to Learn:** Heap structures, chunk management, fastbins, forward/backward pointers.
*   **Verified Lab Code & Solutions:** Complete the interactive suite within the [Shellphish how2heap Repository](https://github.com/shellphish/how2heap). Each `.c` file serves as an interactive lesson that prints heap states in real-time, functioning as a standalone tutorial and solution.

---

# 🔵 PART 2: Interactive C++ Track (Secure Architectures & Modern Tooling)

## Module 3: Modern C++ Paradigms & Object-Oriented Security
C++ introduces significant complexity over C. Understanding how objects, virtual tables, and memory are managed by the compiler is critical for both defending and analyzing C++ applications.

### 🛠️ Interactive Lab 3.1: Modern Syntax & Component Building
*   **Your Objective:** Learn the fundamentals of modern C++ structures, including Vectors, Classes, and Pointers.
*   **Interactive Platforms:**
    *   [Learn-CPP Interactive Tutorial](https://www.learn-cpp.org/) - A browser-based IDE to test syntax immediately.
    *   [Codédex - Learn C++](https://www.codedex.io/cpp) - A gamified approach to C++ fundamentals.

### 🛠️ Interactive Lab 3.2: Secure C++ Interfacing & API Usage
*   **Your Objective:** Develop a C++ application that safely queries the operating system and interacts with standard APIs, observing how memory is allocated and released to prevent leaks.
*   **Study & Documentation Material:** [r3dlevy - Win32 API Practical Examples Guide](https://r3dlevy.github.io/blog/offensive-development-with-c-and-c-getting-started-with-win32-api-and-practical-examples).
*   **Structural Blueprint Review:** Review the [lsecqt OffensiveCpp Library](https://github.com/lsecqt/OffensiveCpp) for object-oriented structural patterns and how complex interactions are modeled.

---

## Module 4: Reverse Engineering & Binary Analysis
To secure applications, you must understand how they are disassembled and analyzed by reverse engineers.

### 🛠️ Interactive Lab 4.1: Embedded Systems Analysis (Microcorruption)
*   **Your Objective:** Act as a security researcher tasked with analyzing electronic locks. You will use an in-browser debugger and assembly view to reverse engineer the device's code and identify logic flaws.
*   **Interactive Platform:** [Microcorruption Wargame](https://microcorruption.com/).
*   **Core Concepts to Learn:** Real-world assembly language, low-level execution flow, and debugging techniques.

### 🛠️ Interactive Lab 4.2: Compiler Behavior & Code Mangling
*   **Your Objective:** Write a simple C++ program utilizing polymorphism (virtual functions) and analyze the resulting compiled binary to locate the virtual method table (vTable).
*   **Study Material:** [Reverse Engineering C++ (Black Hat Paper)](https://blackhat.com/presentations/bh-dc-07/Sabanal_Yason/Paper/bh-dc-07-Sabanal_Yason-WP.pdf). This paper is essential for understanding how C++ features are translated into machine code.

---

# 🟢 PART 3: Automation & Tooling Scripts

## Module 5: Developing Exploit Wrappers (Python/Bash)

### 🛠️ Interactive Lab 5.1: Python/Bash Interaction Frameworks
*   **Your Objective:** When interacting with vulnerable binaries or remote services in your lab environments (like OverTheWire), write Python or Bash scripts to automate the connection and data delivery process.
*   **Python Automation Core:** Use the [Pwntools](https://github.com/Gallopsled/pwntools) framework to manage the interaction loop between your attack machine and target binaries.
*   **Bash Scripting Reference:** Refer to the [Black Hat Bash PDF](https://elhacker.info/manuales/Lenguajes%20de%20Programacion/Black%20Hat%20Bash.pdf) for creating robust shell tools.
