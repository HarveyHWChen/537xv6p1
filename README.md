537xv6p1
========
Project 1b: xv6 Intro

We'll be doing kernel hacking projects in xv6 , a port of a classic version of unix to a modern processor, Intel's x86. It is a clean and beautiful little kernel, and thus a perfect object for our study and usage.

This first project is just a warmup, and thus relatively light on work. The goal of the project is simple: to add a system call to xv6. Your system call, getsyscallinfo() , simply returns the value of a counter.

Specifically, you need to add one counter that increments every time a system call is made. The counter should be incremented before each time a system call is issued; when getsyscallinfo() is called, the calling program can thus discover how many total system calls have been made.

Details

Your new syscall should look like this: int getsyscallinfo(void) .

Your system call returns the number of calls made since the system booted on success, and -1 on failure.

The count for a system call should only be incremented before the call is finished executing, not after.

Tips

Find some other system call, like getpid() . Basically, copy it in all the ways you think are needed. Then modify it to do what you need.

Most of the time will be spent on understanding the code. There shouldn't be a whole lot of code added.

Using gdb (the debugger) may be helpful in understanding code, doing code traces, and is helpful for later projects too. Get familiar with this fine tool!

The Code

The source code for xv6 (and associated README) can be found in ~cs537-2/ta/xv6/ . Everything you need to build and run and even debug the kernel is in there; start by reading the README.

You may also find the following book about xv6 useful, written by the same team that ported xv6 to x86: book . Particularly useful for this project: Chapters 0 and 3 (and maybe 4). Note that our version of xv6 is slightly older than the book's, so you may encounter a difference here and there.
