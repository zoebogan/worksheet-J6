# Worksheet J6 Question
## Zoe Bogan

1. The outputs are not consistent. The order of when the threads start and end after thread 1 of afternoon is started. As well as the number of "good afternoons" are printed followed by the number of "good mornings" differ.

2. The output has more of a pattern where it alternates morning and afternoon then it prints the same one twice and then back to alternating morning and afternoon. The afternoon thread starts first in the sequence. Overall the order changes and the threads that finish first happen at the end of the print statements but the order of which threads finish differ.
3. Because GreetingsThread is a child class of Thread (extends Thread) the run() method is overridden in that class so that when main is exited the run() method continues.
4. Joining the morning thread for 5 seconds makes the morning thread to be the first one to start and outputs the first 5 print statements. After this the afternoon thread runs and is alternated with the morning thread until the morning thread is finished. Then the afternoon thread completes its cycle.
5. ```join()``` without any parameters of seconds runs the entire thread rather than the amount stated in the parameters, ```join(10)``. So ```join(10)`` will join the first 10 prints then starts other threads.
6. 
