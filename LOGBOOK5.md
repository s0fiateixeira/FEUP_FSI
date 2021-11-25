This logbook is divided into 2 sections, one referring to the CTF - week 5, and another concerning the tasks for week 5.

# CTF - Week 5
____
____

# Buffer Overflow Attack Lab

## Task 1: Getting Familiar with Shellcode

When running the a32.out and the a64.out files, a shell is launched and we can use it, as we can see in the following screenshot. In this case we used the command "ls".

![task1](LOGBOOK_screenshots/LOGBOOK5/task1.png)

## Task 2: Understanding the Vulnerable Program

During the second task, we compiled the vulnerable program and made it a root-owned SET-UID program, as seen in the following screenshot.

![task2](LOGBOOK_screenshots/LOGBOOK5/task2.png)


## Task 3: Launching Attack on 32-bit Program

In the first part of the task we used a debugging method to search for the ebp value and the buffer's address. We noted that the ebp was 0xffffca48 and the buffer's address was 0xffffc9dc as seen in the screenshot below.

![task3_1](LOGBOOK_screenshots/LOGBOOK5/task3_1.jpg)

By opening the exploit.py code we were able to see that the bytes before the return address were filled with NOP's instructions. This instructions are for no operation, which provoques the jump for the next instruction. To improve the chance of success of jumping to the part of the stack that contains the shellcode, we can put the shellcode after the NOP instructions so we can eventually get to the shellcode. The code in the next screenshot shows that we started to write the shellcode at the end of the stack, so the start variable needs to be the subtraction between 517 and the length of the shellcode. On the ret variable we opted to use the return value plus 250 which make the return value jump to the middle of the NOP's and we eventually are able to read the shellcode. Then the offset was calculated by the offset between the ebp and the buffer witch is 108 and we added 4 which was the size of the return value.

![task3_2](LOGBOOK_screenshots/LOGBOOK5/task3_2.png)

With this, we are able to use the files with root permission now.

![task3_3](LOGBOOK_screenshots/LOGBOOK5/task3_3.png)
