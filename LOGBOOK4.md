# Environment Variable and Set-UID Program Lab

## Task 1: Manipulating Environment Variables

In the first task, several commands such as env, printenv, export and unset, among others, were used in order to have a better understanding of the functioning and manipulation of environment variables.

* Firstly, by using the printenv command we were able to print out the environment variables, as seen below. 

![task1_1](LOGBOOK_screenshots/LOGBOOK4/task1_1.jpg)

* Secondly, we used export and unset in order to manipulate the environment variables. When using export without any further arguments, it is returned a list of the environment variables (similarly to printenv), as shown in the first screenshot.

![task1_21](LOGBOOK_screenshots/LOGBOOK4/task1_21.jpg)

Here, we can see that HOME has a default value of "/home/seed". Then, when inserting a variable name as argument, as shown in the second screenshot, as well as its new value (/home/seed/cenas), we were able to set this new value to the HOME variable. Afterwards, when unsetting the home variable we deleted it. In the end of the exercise we altered it so it was the same as the beginning.

![task1_22](LOGBOOK_screenshots/LOGBOOK4/task1_22.jpg)

## Task 2: Passing Environment Variables from Parent Process to Child Process

During this exercise we noticed that the output of the two cases was the same, witch means that the environment variables of a parent process and a child process are the same. We concluded that when a fork happens, a new process is created by duplicating the calling process, so they have the same content.

![task2](LOGBOOK_screenshots/LOGBOOK4/task2.png)

## Task 3: Environment Variables and execve()

The output of the first version of the code returns nothing (as demonstrated in the picture bellow), however, the second version outputs the intended content. We concluded that it happens because the command excve does not return the environment by default and so it needs to be specified.

![task3](LOGBOOK_screenshots/LOGBOOK4/task3.png)
![task3_1](LOGBOOK_screenshots/LOGBOOK4/task3_1.png)


## Task 4: Environment Variables and system()

![task4](LOGBOOK_screenshots/LOGBOOK4/task4.png)
![task4_1](LOGBOOK_screenshots/LOGBOOK4/task4_1.jpg)


## Task 5: Environment Variable and Set-UID Programs

All the environment variables set in the parent process get into the child process (as seen in the last screenshot of this section). This means that when the child process is created, during the fork, all the variables are the same which is what we expected since the fork duplicates the process.

![task5](LOGBOOK_screenshots/LOGBOOK4/task5.png)
![task5_3](LOGBOOK_screenshots/LOGBOOK4/task5_3.png)
![task5_31](LOGBOOK_screenshots/LOGBOOK4/task5_31.jpg)


## Task 6: The PATH Environment Variable and Set-UID Programs
![task6](LOGBOOK_screenshots/LOGBOOK4/task6.png)
![task6_1](LOGBOOK_screenshots/LOGBOOK4/task6_1.png)

## Task 7: The LD PRELOAD Environment Variable and Set-UID Programs
[todo]

## Task 8: Invoking External Programs Using system() versus execve()
[todo]

## Task 9: Capability Leaking
[todo]
