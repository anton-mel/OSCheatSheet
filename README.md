# OS CheatSheet

Operating System - is a layer of software that provides 2 important services: 

1. Abstraction -- hides details of different hardware configurations, so applications do not have to be tailored for each possible device that might be present on a system.
2. Arbitration -- manages access to a shared hardware resources, which enables multiple applications to share the same hardware simultaneously.

**Hardware Resources**

**CPU**; executes program instructions; multiple CPU cores execute instructions in parallel.
**Memory**; hierarchy of different memory speeds: 
1. Registers [D-flip-flops] & cache [SRAM] ($) is the fastest memory; attached to a CPU.
2. Random access memory (RAM) [DRAM: capacitors and transistors, so requires periodical refreshing to store data unlike SRAM] - slower, keeps pages (looses data with power loss).
3. Persistent Memory [Hard Disk Drives, Solid-State Drives] - slowest.
**I/O devices** (LKMs); Includes keyboard, mouse, network interface card (NIC), screen, printer...
**Power and System Management**; Power supply, internal cooling (fans, etc.)

**ABSTRACTIONS**
Allow the hardware device manufactures by different manufactures to have **same interface within software for applications to use,** although have different low-lever instruction sets and capabilities. *If we did not have common interface, we would need to do internal programming for the game video or sound cards*.

**ARBITRATION**
Allow hardware by shared by multiple applications simultaneously. OS ensures that all applications can access resources by dividing the CPU core time among different programs, managing the access to RAM, I/O, and disk; enforces system and security policies to isolate applications from each other (in an ideal word, at least)

Operating system **splits userspace:** Libraries, Utilities, and Applications with the **Hardware.** The OS then provides a mechanism known as `SysCalls` (system calls) that enables applications on the userspace to interact with hardware resources through this abstraction layer. It also has an **interrupt handling mechanism** that sends alerts from the bottom of the hardware. Moreover, OS can also manage and terminate the applications by sending signals to the application.

---

**System Form Factors**

Specifications of standard size for equipment that allows computer components to be interchangeable with one another. Standard form factors:
1. ATX (Typical workstation systems)
2. UATX, mini-ITX (Smaller systems)
3. Rackmount (Typical servers in a data centers)
4. Laptop systems are proprietary, so hard to interchange

**INFO:** Each workstation system typically supports one user at a time -- systems may be shared between users or dedicated to a single user. Frequently ATX or uATX form factor. One power supply unit per system -- efficiency can be an issue, especially with many systems. Can be used to host server applications in smaller settings (small businesses or NPOs).

Server applications and larger-scale environments such as enterprise are hosted in the Rackmount systems -- a space efficient way to put a lot of servers in one data-center. Divided into "units" (U) - a typical rack is 42U tall. 

So the most space efficient servers that 1U system with 12 cores in each machines can enable 48cores be split per rack [Will not have room for expansion]. 
2U is less space-efficient; allows for more expansion [Disk drives, add-in cards].
4U least space-efficient, most expansion (up to 16 2.5" drives) [Generally have many redundant components].

---

