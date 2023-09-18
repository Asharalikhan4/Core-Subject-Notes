# Operating System
An operating system acts as an intermediary between the user of a computer and computer hardware. The purpose of an operating system is to provide an environment in which a user can execute programs conveniently and efficiently.
An operating system is a software that manages computer hardware. The hardware must provide appropriate mechanisms to ensure the correct operation of the computer system and to prevent user programs from interfering with the proper operation of the system.
1. An operating system is a program that controls the execution of application programs and acts as an interface between the user of a computer and the computer hardware.
2. A more common definition is that the operating system is the one program running at all times on the computer (usually called the kernel), with all else being application programs.
3. An operating system is concerned with the allocation of resources and services, such as memory, processors, devices, and information. The operating system correspondingly includes programs to manage these resources, such as a traffic controller, a scheduler, a memory management module, I/O programs, and a file system.

## Goal of Operating System
1. Convenience( Primary goal)
2. Efficiency (Secondary goal)

## Functions of Operating System
1. Process management
2. Memory management
3. Storage management
4. Protection and Security
5. Input-Output management

## 1. Process Management
1. Creating and deleting user and system processes.
2. Suspending and resuming processes.
3. Process synchronization.
4. Inter-process communication.
5. Deadlock Handling.

## 2. Memory management
1. Deciding which process and data to move into and out of memory.
2. Keeping tracks of which part of memory are currently being used and by whom.
3. Allocating and deallocating memory space as needed.

## 3. Storage management
1. File-System Management
    - Creating and deleting files.
    - Creating and deleting directories to organize files.
    - Supporting primitives for manipulating files and directories.
    - Mapping files into secondary storage.
    - Backing up files on stable(non volatile) storage media.
2. Mass-Storage Management
    - Free space management
    - Storage allocation
    - Disk Scheduling

## 4. Protection and Security
The operating system uses password protection to protect user data and similar other techniques. It also prevents unauthorized access to programs and user data.

## 5. I/O System Management
The module that keeps track of the status of devices is called the I/O traffic controller. Each I/O device has a device handler that resides in a separate process associated with that device.

The I/O subsystem consists of -

- A memory Management component that includes buffering, caching and spooling.
- A general device driver interface.

# Process Concept
Early Computer - One program at a time<br/>
Modern Computer - Multiprogramming, Multitasking

**Process:** A process is a program in execution.

A process includes
1. Program Counter
2. Content of the processor’s register.

## Program vs Process
A process is a program in execution. For example, when we write a program in C or C++ and compile it, the compiler creates binary code. The original code and binary code are both programs. When we actually run the binary code, it becomes a process.
A process is an ‘active’ entity, instead of a program, which is considered a ‘passive’ entity. A single program can create many processes when run multiple times; for example, when we open a .exe or binary file multiple times, multiple instances begin (multiple processes are created).

## What does a process look like in memory?
![](./assets/processImage.png "San Juan Mountains")

- **New (Create)** – In this step, the process is about to be created but not yet created, it is the program which is present in secondary memory that will be picked up by OS to create the process.
- **Ready** – New -> Ready to run. After the creation of a process, the process enters the ready state i.e. the process is loaded into the main memory. The process here is ready to run and is waiting to get the CPU time for its execution. Processes that are ready for execution by the CPU are maintained in a queue for ready processes.
- **Run** – The process is chosen by CPU for execution and the instructions within the process are executed by any one of the available CPU cores.
- **Blocked or wait** – Whenever the process requests access to I/O or needs input from the user or needs access to a critical region(the lock for which is already acquired) it enters the blocked or wait state. The process continues to wait in the main memory and does not require CPU. Once the I/O operation is completed the process goes to the ready state.
- **Terminated or completed** – Process is killed as well as PCB is deleted.
- **Suspend ready** – Process that was initially in the ready state but were swapped out of main memory(refer Virtual Memory topic) and placed onto external storage by scheduler are said to be in suspend ready state. The process will transition back to ready state whenever the process is again brought onto the main memory.
- **Suspend wait or suspend blocked** – Similar to suspend ready but uses the process which was performing I/O operation and lack of main memory caused them to move to secondary memory. When work is finished it may go to suspend ready.