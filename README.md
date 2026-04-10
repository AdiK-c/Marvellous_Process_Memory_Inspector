# Marvellous_Process_Memory_Inspector
A Linux-based system programming project in C that analyzes the memory layout of a running process using the /proc filesystem. It reads process details and memory mappings to classify segments like heap, stack, code, and data, providing insights into Linux process memory management.
## 🚀 Project Overview

The **Marvellous Process Memory Inspector** is a Linux-based system programming project developed in C that analyzes the memory layout of a running process.

The application takes a **Process ID (PID)** as input and reads system information from the **/proc filesystem** to display process details and memory mappings. It provides insights into how Linux organizes process memory, including code, data, heap, stack, and other segments.

---

## 🛠️ Technologies Used

* **Language:** C
* **Platform:** Linux
* **Concepts:**

  * Linux System Programming
  * Proc Filesystem (`/proc`)
  * Process Memory Layout
  * File Handling (`fopen`, `fgets`)
  * String Parsing (`sscanf`, `strcmp`)

---

## ✨ Features

* 🔍 **Process Information Inspection**

  * Displays process name, state, PID, and thread count

* 🧠 **Memory Map Analysis**

  * Reads `/proc/<pid>/maps`
  * Displays memory regions with:

    * Start Address
    * End Address
    * Size (KB)
    * Permissions
    * Section Type
    * Region Details

* 🧩 **Memory Section Classification**

  * Classifies memory into:

    * TEXT (Code)
    * DATA
    * HEAP
    * STACK
    * VDSO / VVAR
    * OTHER

* 🔐 **Permission-Based Analysis**

  * Identifies readable, writable, and executable regions

* ⚙️ **Dynamic PID Analysis**

  * Works with any running process

---

## 🧩 Project Structure

```id="1y4x9g"
program913.c
│
├── GetSectionType()        → Classifies memory regions
├── ShowMemoryLayout()      → Reads /proc/<pid>/maps
├── ShowProcessInformation()→ Reads /proc/<pid>/status
└── main()                  → User interaction
```

---

## ▶️ How to Run

### Step 1: Compile

```bash id="c1t8kg"
gcc program913.c -o inspector
```

### Step 2: Run

```bash id="1h7k7l"
./inspector
```

---

## 💻 Sample Usage

```id="5j6c2g"
----------- Marvellous Process Inspector -----------

Enter the PID of a process that you want to inspect
1234

Process Information:
Name: bash
Pid: 1234
State: S (sleeping)
Threads: 1

Memory Layout:
Start       End         SizeKB  Perm  Section   Details
...
```

---

## ⚠️ Important Note

* This project works **ONLY on Linux systems**
* It uses the `/proc` filesystem, which is not available on Windows

---

## 🎯 Key Learnings

* Understanding Linux process memory structure
* Working with `/proc` filesystem
* Parsing system-level files
* Memory segment classification
* Low-level system programming in C

---

## 📌 Future Improvements

* Add filtering options (only heap/stack/etc.)
* Export memory layout to file
* Add graphical visualization
* Support multiple PIDs

---

## 👨‍💻 Author

**Aditya Kotewar**

---

## ⭐ Conclusion

This project demonstrates strong fundamentals of **Linux system programming and memory analysis**. It provides hands-on experience with real process data, making it a valuable addition to any developer’s portfolio, especially for system-level and backend roles.

---

