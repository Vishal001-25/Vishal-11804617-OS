Problem:
1.
Consider the scenario, there are 3 student processes and 1 teacher process. Students are supposed to do their assignments
and they need 3 things for that-pen, paper and question paper. The teacher has an infinite supply of  all the three things.
One students has pen, another has paper and another has question paper. The teacher places two things on a shared table and
the student having the third complementary thing makes the assignment and tells the teacher on completion. The teacher then
places another two things out of the three and again the student having the third thing makes the assignment and tells the 
teacher on completion. This cycle continues. WAP to synchronise the teacher and the students.

Explanation:
1.In the given solution I have taken all the student processes and resources in a structure named "requirement".
2.I have given student 1 with pen, student 2 with paper and student 3 with question paper using boolean values.
3.I have initialized a "while" loop to share the resources among the students with the help of menu-driven format
in which the user will enter the resources the student needs.
4.If one student process is completed there will be a message printed on the screen saying process is completed.
5.If one student process is executing no other student process or teacher process will execute and for achieving this I
have if statements as the mutex locks.
6.When a process starts to execute it acquires the lock and when it completes the execution releases the lock, which is 
similar to that of if statements.
7.After completionof all the 3 processes the loop will end which depicts the end of the program.


2.
Two types of people can enter into a library- students and teachers. After entering the library,
the visitor searches for the required books and gets them. In order to get them issued, he goes 
to the single CPU which is there to process the issuing of books. Two types of queues are there
at the counter-one for students and one for teachers. A student goes and stands at the tail of 
the queue for students and similarly the teacher goes and stands at the tail of the queue for 
teachers (FIFO). If a student is being serviced and a teacher arrives at the counter, he would
be the next person to get service (PRIORITY-non preemptive). If two teachers arrive at the same
time, they will stand in their queue to get service (FIFO). WAP to ensure that the system works
in a non-chaotic manner.
If a teacher is being served and during the period when he is being served, another teacher comes,
then that teacher would get the service next. This process might continue leading to increase in 
waiting time of students. Ensure in your program that the waiting time of students is minimized.

Explanation:
Multi-level feedback queue scheduler Q consists of 3 linear queues, i.e., Q1, Q2, and Q3.
•	Q1 is round robin with time quantum 6 (RR6),
•	Q2 is round robin with time quantum 10 (RR10), and
•	Q3 follows first come first serve (FCFS)
•	The process cannot be executed in the lower queue if there are any jobs in all higher queues. 
For example, Q1 has 5 processes, Q2 has 1 process, and Q3 has 1 process. Then, first the process
in Q1 should be executed (and completed), and then a process in Q2 is executed. Finally, Q3 will
get CPU resource.
•	A new process enters queue Q1 which is served RR5. • When it gains CPU, a process receives 5 
milliseconds. 
             • If it does not finish in 5 milliseconds, the process is moved to queue Q2. 
             • At Q2 process is again served RR8 and receives 8 additional milliseconds. 
             • If it still does not complete, it is preempted and moved to queue Q3. 
             • At Q3 process is executed by first come first serve. 
             • If it still does not complete, it is processed at Q2 until completed.
