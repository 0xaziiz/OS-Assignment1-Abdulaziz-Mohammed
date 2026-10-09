# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers


---


## 👤 Student Information


| **Field**            | **Your Answer**                   |
| -------------------- | --------------------------------- |
| **Full Name**        | Abdulaziz Alshathri       |
| **Student ID**       | 446050854      |
| **University Email** | 446050854@std.psau.edu.sa          |
| **GitHub Username**  | 0xaziiz            |
| **Repository Link**  | https://github.com/0xaziiz/OS-Assignment1-Abdulaziz-Mohammed |

---

## 🎥 Video Link

**Video Link**: To be added after recording


---

## 🗺️ Work Roadmap (follow in this order)

| **Step** | **What to do**                                                                     | **Where**         | **Marks**     |
| -------- | ---------------------------------------------------------------------------------- | ----------------- | ------------- |
| 0        | Read `README.md`, then read and run the full code                                  | Your IDE          | –             |
| 1        | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 150), **commit** | GitHub + code     | Part 1 (1)    |
| 2        | Feature 1: Process Priority, **commit**                                            | Code              | Part 2 (0.25) |
| 3        | Feature 2: Context Switch Counter, **commit**                                      | Code              | Part 2 (0.25) |
| 4        | Feature 3: Waiting Time Tracking, **commit**                                       | Code              | Part 2 (0.5)  |
| 5        | Development Log (5+ entries, different dates)                                      | This file, Part A | Part 3 (0.5)  |
| 6        | Reflection (4 questions)                                                           | This file, Part B | Part 3 (0.5)  |
| 7        | Technical Answers (4 questions)                                                    | This file, Part C | Part 3 (0.5)  |
| 8        | Record the video, upload it, paste the link above                                  | Video + this file | Part 4 (1.5)  |
| 9        | Final check, then submit the repo link on Blackboard                               | Blackboard        | –             |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 3 meaningful commits. Aim for 6 or more.**

| **#** | **Commit**                  | **Example message**                                        |
| ----- | --------------------------- | ---------------------------------------------------------- |
| 1     | Student ID set              | `Set my student ID: 441234567`                             |
| 2     | Feature 1: Priority         | `Feature 1: Added priority field to Process class`         |
| 3     | Feature 2: Context switches | `Feature 2: Implemented context switch counter`            |
| 4     | Feature 3: Waiting time     | `Feature 3: Added waiting time tracking and summary table` |
| 5     | Development log entries     | `Docs: Added development log entries 1-3`                  |
| 6     | Reflection and answers      | `Docs: Completed reflection and technical answers`         |
| 7     | Video link                  | `Docs: Added demo video link`                              |

**Rules:**

- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline.
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 3 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)


## Your Development Log

### Entry 1 - October 5, 2026

**What I did:** Set up my GitHub project and added my student ID.

**Details:** I forked the starter repository, renamed it, and opened the project in VS Code. I changed the student ID to `446050854` and pushed the change to GitHub.

**Challenges:** I was still learning how to work with Git and GitHub.

**Solution:** I followed the setup steps and checked that my change appeared in the repository.

**Time spent:** About 30 minutes.

---

### Entry 2 - October 6, 2026

**What I did**: Added a priority number for each process.

**Details**: I added the priority field and generated a number from 1 to 10. The priority appears when a process enters the ready queue.

**Challenges**: Priority should not change the Round-Robin order.

**Solution**: I kept the queue FIFO and only displayed the priority.

**Time spent**: About 1 hour and 30 minutes.

---

### Entry 3 - October 7, 2026

**What I did**: Added the context switch counter.

**Details**: I added `contextSwitchCount` and increased it each time the scheduler starts a process thread. The total is shown at the end.

**Challenges**: A process may run more than once, so counting only processes would be wrong.

**Solution**: I updated the counter inside the scheduling loop.

**Time spent**: About 1 hour.

---

### Entry 4 - October 8, 2026

**What I did**: Added waiting time and turnaround time.

**Details**: I used `System.currentTimeMillis()` to track waiting time. The final table shows the burst time, waiting time and turnaround time.

**Challenges**: A process may return to the queue and wait again.

**Solution**: I added the waiting periods together before printing the table.

**Time spent**: About 2 hours.

---

### Entry 5 - October 9, 2026

**What I did**: Tested the final program.

**Details**: I ran the simulation and checked the priority numbers, context switch count, and waiting time table. I also checked that unfinished processes returned to the ready queue.

**Challenges**: I wanted to make sure the changes did not affect Round-Robin scheduling.

**Solution**: I followed the queue messages in the output and checked the final table.

**Time spent**: About 45 minutes.

---


## Development Log Summary

**Total time spent on assignment**: About 5 hours and 45 minutes.

**Most challenging part**: Tracking waiting time when a process enters the queue more than once.

**Most interesting learning**: A process can have more than one turn in Round-Robin.

**What I would do differently next time**: I would keep notes after each session.

# Part B: Reflection (0.5 mark)


## Question 1: What did you learn about multithreading?


**Your Answer:** 

I learned how Java threads work in this assignment. The `Process` class implements `Runnable`. We use `new Thread(process)` to create a thread. The `start()` method starts it, and `join()` makes the main thread wait. The `sleep()` method is used to simulate the process working. I also learned why a process may need more than one turn.

## Question 2: What was the most challenging part of this assignment?


**Your Answer:** 

The hardest part for me was waiting time. A process does not always finish in one turn. It can return to the ready queue and wait again. I had to understand how to count all those waiting periods. At first, I confused waiting time with burst time. After checking the queue flow, it made more sense.

## Question 3: How did you overcome the challenges you faced?


**Your Answer:** 

I worked on one feature at a time. I read the methods related to the ready queue. I checked the program output after each change. For waiting time, I used `markReadyQueueEntry()` and `updateWaitingTime()`. I also made sure priority did not change the FIFO order. Testing the program helped me find out whether my changes worked.

## Question 4: How can you apply multithreading concepts in real-world applications?


**Your Answer:** 

Multithreading is useful when a program needs to do more than one task. A music app can play a song while the user changes the volume. A browser can load a page while the user uses another tab. In our simulation, threads run the processes one turn at a time. Round-Robin gives unfinished processes another chance to run. This helped me understand why scheduling is important.


---

# Part C: Technical Answers (0.5 mark)


## Question 1: Thread vs Process

**Question:** Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes? Mention at least **TWO** specific differences (e.g., memory sharing, creation overhead, communication speed), and reference relevant parts of `SchedulerSimulation.java`.


**Your Answer:**

A process is a running program with its own memory, while threads share memory inside the same process. Threads are faster to create and can share data more easily than separate processes. In my code, `Process` is only a simulated process, and `new Thread(process)` runs it using a Java thread.

## Question 2: Ready Queue Behavior

**Question:** In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from **your** program output, including **how many times that process was re-queued** before it finished, and explain why re-queueing matters for fairness.


**Your Answer:** 

When a process does not finish within its time quantum, it goes back to the ready queue. In my run, P1 had a burst time of 6882 ms, and the quantum was 5000 ms. P1 returned to the queue once, then finished its remaining 1882 ms. This gives the other processes a chance to run instead of waiting for P1 to finish. Re-queueing helps keep Round-Robin fair.

Example from my output:

```
➕ P1 added to ready queue │ Burst time: 6882ms │ Priority: 3
▶ P1 executing quantum [5000ms]
P1 yields CPU for context switch
➕ P1 added to ready queue │ Burst time: 6882ms │ Priority: 3
▶ P1 executing quantum [1882ms]
✓ P1 finished execution!

```

**Explanation of example:** P1 runs for 5000 ms, goes back to the ready queue once, and later finishes its remaining 1882 ms.

## Question 3: Thread Lifecycle

**Question:** A thread goes through these states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (e.g., P1) from your simulation. For each state, explain **when** P1 enters it and **which line or method call** triggers the transition (`Thread.start()`, `Thread.join()`, `Thread.sleep()`, etc.).


**Your Answer:** 

1. **New**: P1 gets a new thread when the program calls `new Thread(process)`.
2. **Runnable**: `start()` makes P1 ready to run.
3. **Running**: P1 executes its `run()` method when the scheduler gives it a turn.
4. **Waiting**: P1 pauses with `Thread.sleep()` (timed waiting), while the main thread waits for it with `join()`.
5. **Terminated**: P1's thread ends after its `run()` method finishes; another thread is created if P1 needs another turn.

## Question 4: Real-World Applications

**Question:** Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. **At least one** must be an operating-system-level scenario (e.g., how an OS scheduler shares CPU time among running programs). The second can be any application you choose. For each, explain what the system is and **why Round-Robin fits** (fairness, responsiveness, predictability).


**Your Answer:** 

### Example 1 (operating-system level): CPU scheduling

**Description**: An operating system can share CPU time among threads from different running programs. Each thread gets a short turn before another one can run. This is similar to the processes in my simulation.

**Why Round-Robin works well here**: Round-Robin stops one thread from using the CPU for too long. It gives the other threads a chance to run and helps keep the system responsive.

### Example 2: Server requests

**Description**: A server can have many client requests waiting for work. It can divide longer jobs into smaller turns. Requests that need more work can return to the queue.

**Why Round-Robin works well here**: Round-Robin gives each request a turn, so one long request does not block all the others. This is like putting P1 back in the ready queue in my program.

## Summary

**Key concepts I understood through these questions:** Threads, ready queues, and Round-Robin scheduling.

**Concepts I need to study more:** Thread synchronization and how real operating systems switch between threads.

---

# ✅ Final Checklist (complete before submitting)

- [x] Student information and repository link
- [x] Three code features and separate commits
- [x] Development log, reflection, and technical answers
- [ ] Add public video link (2–3 minutes)
- [ ] Submit GitHub repository URL on Blackboard
