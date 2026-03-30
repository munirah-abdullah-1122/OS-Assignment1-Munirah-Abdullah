# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.



---

## Your Development Log:

### Entry 1 - [March 27, 2026, 11:00 PM]
**What I did**: Set up GitHub repository and project 

**Details**: 
- Created a GitHub account using university email  
- Forked the starter repository  
- Renamed the repository according to assignment instructions  
- Added my student ID (445052165) in SchedulerSimulation.java 
- Ran the program successfully to verify initial execution  

**Challenges**: Initial confusion between GitHub fork and clone operations

**Solution**: Watched a short tutorial and practiced both methods to understand the difference

**Time spent**: 2 hour

---

### Entry 2 - [March 28, 2026, 1:00 AM]
**What I did**: Studied the starter code and understood scheduling logic

**Details**: 
- Analyzed Process class and SchedulerSimulation  
- Understood how Round-Robin scheduling works  
- Observed how threads are created and executed  
- Traced program output step by step

**Challenges**: Understanding how threads interact with the ready queue

**Solution**: Re-read code and linked it with OS concepts from textbook

**Time spent**: 1 hour

---

### Entry 3 - [March 28, 2026, 9:00 AM]
**What I did**: Implemented Feature 1 (Process Priority) 

**Details**:
- Added priority variable to Process class  
- Modified constructor to include priority  
- Generated random priority values for each process  
- Displayed priority when process enters ready queue

**Challenges**: Passing priority correctly between different parts of the code

**Solution**: Carefully updated constructor and verified object creation

**Time spent**: 2 hour

---

### Entry 4 - [March 28, 2026, 10:00 PM]
**What I did**: Implemented Feature 2 (Context Switch Counter)

**Details**:
- Added a counter variable to track context switches  
- Incremented counter before starting each thread  
- Printed total number of context switches at the end

**Challenges**: Finding the correct location to count context switches

**Solution**: Placed increment before thread.start() to reflect actual scheduling 

**Time spent**: 2 hour

---

### Entry 5 - [March 29, 2026, 2:00 AM]
**What I did**: Implemented Feature 3 (Waiting Time Tracking) and final testing

**Details**: 
- Added variables to track waiting time  
- Calculated waiting time for each process  
- Displayed summary of waiting times at the end  
- Tested the program multiple times to verify correctness 

**Challenges**: Calculating waiting time accurately

**Solution**: Used System.currentTimeMillis() and verified results through output

**Time spent**: 3 hours

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [3 days]

**Most challenging part**: Understanding Round-Robin behavior and waiting time calculation

**Most interesting learning**: How CPU scheduling ensures fairness between processes

**What I would do differently next time**: Start earlier and test each feature step by step
