Learning Objectives

General
Who designed and implemented the original Unix operating system
Who wrote the first version of the UNIX shell
Who invented the B programming language (the direct predecessor to the C programming language)
Who is Ken Thompson
How does a shell work
pid and a ppid
To manipulate the environment of the current process
The difference between a function and a system call
How to create processes
The three prototypes of main
How does the shell use the PATH to find the programs
Execute another program with the execve system call
Suspend the execution of a process until one of its children termination.
EOF / “end-of-file”?

Requirements

General
Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
Your shell should not have any memory leaks
No more than 5 functions per file
All your header files should be include guarded
Use system calls only when you need to (why?)
Write a README with the description of your project
You should have an AUTHORS file at the root of your repository, listing all individuals having contributed content to the repository.

GitHub
*There should be one project repository per group. If you and your partner have a repository with the same name in both your accounts, you risk a 0% score. Add your partner as a collaborator. *

compiler: gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh

Tasks
0. 

Write a beautiful code that passes the Betty clone  

1.

Write a UNIX command line interpreter

Display a prompt and wait for the user to type a command. A command line always ends with a new line.
The prompt is displayed again each time a command has been executed.
The command lines are simple, no semicolons, no pipes, no redirections or any other advanced features.
The command lines are made only of one word. No arguments will be passed to programs.
If an executable cannot be found, print an error message and display the prompt again.
Handle errors.
You have to handle the “end of file” condition (Ctrl+D)
You don’t have to:

use the PATH
implement built-ins
handle special characters : ", ', `, \, *, &, #
be able to move the cursor
handle commands with arguments
execve will be the core part of your Shell, don’t forget to pass the environ to it…
    
2.

Handle command lines with arguments
    
3. 

Handle the PATH
fork must not be called if the command doesn’t exist
    
4. 

Implement the exit built-in, that exits the shell
Usage: exit
5.

Implement the env built-in, that prints the current environment.
