# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > concurrency is that more than one task starts run and complete in overlapping time periods without order

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 
 ### Why have machines become increasingly multicore in the past decade?
 > When the CPU sped is more than 3-4GHz the power consumption starts to increase too fast. Therefor we make multicore processors instead.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > you can use concurrency to run two programs at the same time.

 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > Harder to debug
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > processes is managed by OS, has its own virtual memory address space, can be interrupted and they can run in parallel with other processes 

Threads is managed by OS, every thread is in a particular process, threads in the same process share the same virtual address space, can be interrupted, can run in parallel with other threads on different processors

Green threads: Not managed by OS, threads that are scheduled by runtime library or virtualmachine.

Coroutines are components of a computer program that generalize subroutines by allowing multiple entry points for suspending and resuming execution at some locations. 

 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > pthread_create() -> thread
threading.Thread() -> green thread

 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > The GIL prevents multiple threads to execute python bytecodes at once. This is necessary because the memorymanagement in python is not thread-safe.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > using subprosesses so rhey does not share memory.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > The GOMAXPROCS variable limits the number of operating system threads that can execute user-level Go code simultaneously.
