# Worksheet J6 Question
## Zoe Bogan

1. The outputs are not consistent. The order of when the threads start and end after thread 1 of afternoon is started. As well as the number of "good afternoons" are printed followed by the number of "good mornings" differ.

2. The output has more of a pattern where it alternates morning and afternoon then it prints the same one twice and then back to alternating morning and afternoon. The afternoon thread starts first in the sequence. Overall the order changes and the threads that finish first happen at the end of the print statements but the order of which threads finish differ.
3. Because GreetingsThread is a child class of Thread (extends Thread) the run() method is overridden in that class so that when main is exited the run() method continues.
4. Joining the morning thread for 5 seconds makes the morning thread to be the first one to start and outputs the first 5 print statements. After this the afternoon thread runs and is alternated with the morning thread until the morning thread is finished. Then the afternoon thread completes its cycle.
5. ```join()``` without any parameters of seconds runs the entire thread rather than the amount stated in the parameters, ```join(10)```. So ```join(10)``` will join the first 10 prints then starts other threads.
6. ```isAlive()``` checks the status of a thread and if it is still running without blocking the execution. ```join()``` forces a thread to wait to finish.
7. The threads finish in the order of Cheetah, hare, and tortoise because each of their trends corresponds to a speed that is then divided in a ```sleep``` function which sleeps the thread, because tortoise has the smallest number input it sleeps that longest.
8. If the code below is added after the tortoise thread starts, then the hare thread is able to move through the first 2 laps before the other two animals therefore it finishes first. However making the hare thread have a head start may not be possible because the operating system decides which thread to start first. 
```java
    public class AnimalFootRace {
    public static void main(String[] args) {
        Thread tortoiseThread = new AnimalRacerThread("Tortoise", 5);
        Thread hareThread = new AnimalRacerThread("Hare", 20);
        Thread cheetahThread = new AnimalRacerThread("Cheetah", 50);

        System.out.println("On your marks, get set, go!");
        tortoiseThread.start();
        hareThread.start();
        try {
            hareThread.join(2000);
        } catch (InterruptedException e) {
            System.out.println("Interrupted while joining a thread...");
        }
        cheetahThread.start();
    }
}
```
9. Implementing a new thread.
```java
public class AnimalFootRace {
    public static void main(String[] args) {
        Thread tortoiseThread = new AnimalRacerThread("Tortoise", 5);
        Thread hareThread = new AnimalRacerThread("Hare", 20);
        Thread cheetahThread = new AnimalRacerThread("Cheetah", 50);
        Thread jaguarThread = new AnimalRacerThread("Jaguar", 100);

        System.out.println("On your marks, get set, go!");
        tortoiseThread.start();
        hareThread.start();
        try {
            hareThread.join(2000);
        } catch (InterruptedException e) {
            System.out.println("Interrupted while joining a thread...");
        }
        cheetahThread.start();
        jaguarThread.start();
    }
}
```
Because I inputted a larger integer in of the speed of the jaguar, its trend finishes before the other three without the giving the hare a head start. With joining the harethread the cheetah and jaguar thread have more back and forth rather than all three threads (tortoise, cheetah, and jaguar) being more randomly run.
10. 
