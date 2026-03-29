# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:
process is independent program in execution that has its own memory space and system resources and execution state managed by the operating system.
thread is a lightweight unit of execution that exists within a process and shares the same memory and resources with other threads in that process.
Processes are heavier and require more overhead for creation and context switching and communication, while threads are faster to create and more efficient because they share the same address space.
For this assignment threads were used instead of separate processes because threads allow us to simulate multiple tasks running concurrently without the complexity of managing separate memory spaces. Using threads also improves performance and makes the simulation closer to how modern operating systems handle multitasking efficiently.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:
In Round-Robin scheduling, when a process does not finish within its assigned time quantum and it is paused and placed back at the end of the ready queue.This behavior ensures that all processes share the CPU fairly and prevents any single process from monopolizing execution time.**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
 P2 completed quantum 4000ms │ Overall progress: 55%
Remaining time: 3200ms
 P2 yields CPU for context switch

 P2 added to ready queue │ Burst time: 7200ms │ Priority: 5

```

**Explanation of example:
In this example process P2 executed for its full time quantum 4000ms but did not complete because it still had 3200ms remaining. As a result it yielded the CPU and was placed back into the ready queue. This allows other processes to run before P2 gets another turn. This is important because it keeps the scheduling fair and helps prevent starvation.**


---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: Process P1 is in the New state when the thread object is first created in the code before the start() method is called.

2. **Runnable**: P1 enters the Runnable state and becomes ready to be scheduled by the CPU scheduler.After calling start(). 

3. **Running**: P1 enters the Running state when it starts executing as in the output: P1 executing quantum [2296ms]

4. **Waiting**: P1 enters the Waiting state when Thread.sleep() is called during execution which simulates the process waiting for a period of time before continuing.

5. **Terminated**:  P1 enters the Terminated state after completing its execution as shown in the output: P1 finished execution!

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server Handling Requests

**Description**: A web server handles multiple client requests simultaneously by assigning each request to a separate thread for processing.


**Why Round-Robin works well here**: Round-Robin scheduling ensures that each request receives CPU time in a fair and predictable manner, preventing any single request from blocking others. Also improves system responsiveness because all requests are processed in small time slices instead of waiting for long operations to complete.


### Example 2: Operating System Task Scheduling

**Description**:An operating system schedules multiple processes using CPU scheduling algorithms to ensure efficient execution of tasks.



**Why Round-Robin works well here**: It ensures that all processes get CPU time fairly. It improves system responsiveness by sharing CPU time between processes.


---

## Summary

**Key concepts I understood through these questions:**
1. Difference between processes and threads 
2. How Round-Robin scheduling works
3. Thread lifecycle and states

**Concepts I need to study more:**
1. Advanced scheduling algorithms
2. Synchronization between threads
