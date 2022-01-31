# Learning and using threading,concurrency and multiprocessing modules in python

Definition of concurrency is simultaneous occurrence. In Python, the things that are occurring simultaneously are called by different names (thread, task, process) but at a high level, they all refer to a sequence of instructions that run in order.

In computing, a process is an instance of a computer program that is being executed. Any process has 3 basic components:
- An executable program.
- The associated data needed by the program (variables, work space, buffers, etc.)
- The execution context of the program (State of process)

A thread is an entity within a process that can be scheduled for execution. Also, it is the smallest unit of processing that can be performed in an OS.

In simple words, a thread is a sequence of such instructions within a program that can be executed independently of other code. For simplicity, we can assume that a thread is simply a subset of a process.

Multiple threads can exist within one process where:

- Each thread contains its own register set and local variables (stored in stack).
- All thread of a process share global variables (stored in heap) and the program code.

In a simple, single-core CPU, it is achieved using frequent switching between threads. This is termed as context switching. In context switching, the state of a thread is saved and state of another thread is loaded whenever any interrupt (due to I/O or manually set) takes place. Context switching takes place so frequently that all the threads appear to be running parallelly (this is termed as multitasking).


![multithreading-python-21](https://user-images.githubusercontent.com/42691222/151760729-df2ca20f-e907-4c8a-b1e5-b6d6d887292b.png)
