# Shell-Scripting--project
Shell Scripting

# what is a shell

The shell is the operating system's command-line interface (CLI) and interpreter for the set of commands that are used to communicate with the system. A shell script is usually created for command sequences in which a user has a need to use repeatedly in order to save time.

### Shell Scripting

Usually, shells are interactive, which means they accept commands as input from users and execute them. However, sometimes we want to execute a bunch of commands routinely, so we have to type in all commands each time in the terminal.

As a shell can also take commands as input from file, we can write these commands in a file and can execute them in shell to avoid this repetitive work. These files are called Shell Scripts or Shell Programs. Shell scripts are similar to the batch file in MS-DOS. Each shell script is saved with .sh file extension e.g., myscript.sh.

A shell script has syntax just like any other programming language. If you have any prior experience with any programming language like Python, C/C++ etc. It would be very easy to get started with it.

A shell script comprises the following elements –

Shell Keywords – if, else, break etc.

Shell commands – cd, ls, echo, pwd, touch etc.

Functions :

Control flow – if..then..else, case and shell loops etc.

# Shell scripting elements

Variables : Bash allows you define work and work with variables.

Variable can store data of various type such as numbers, string, and array. You can assign values to variables using operators(=).And access their values using variable name preceded by a $ Sign.

To create a default shell script
- To create an a default shell script
  
 ` touch myscript.sh`

 
 o To proceed with the script we start with a declaration#! /bin/bash

To assign values to variable e.g

Run `name='john'`  and save the file

Retrieving the value Run `echo $name`

<img width="872" alt="john" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/483602db-3982-4bfa-b10a-53c3ac9ae25e">

Control Flow statement

- Bash provides a control flow statement like if-else, for loops, while loops and case statement to control the flow of execution in your scripts. These statements allows you to make a decision,iterates over lists, and execute different commands based on conditions.

Using `if-else` to execute script based on Condition

Run

`#!/bin/bash

# Example script to check if a number is positive, negative, or zero

read -p "Enter a number: " num

if [ $num -gt 0 ]; then
   echo "The number is positive."
   elif [ $num -lt 0 ]; then
   echo "The number is negative."
   else
   echo "The number is zero."
fi`


    echo "The number is zero."
> fi

