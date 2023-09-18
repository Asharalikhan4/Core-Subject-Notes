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
