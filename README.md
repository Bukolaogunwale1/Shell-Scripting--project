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

 ![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/1d4fabfb-5eaa-4696-880a-b4ee53e10800)

 
 o To proceed with the script we start with a declaration#! /bin/bash

To assign values to variable e.g

Run `name='john'`  and save the file

Retrieving the value Run `echo $name`

<img width="958" alt="ist picture" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/8cf7355a-258a-420d-b2f0-5beaa18656a1">

<img width="872" alt="john" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/483602db-3982-4bfa-b10a-53c3ac9ae25e">

Control Flow statement

- Bash provides a control flow statement like if-else, for loops, while loops and case statement to control the flow of execution in your scripts. These statements allows you to make a decision,iterates over lists, and execute different commands based on conditions.

Using `if-else` to execute script based on Condition

Run

```

`#!/bin/bash`

# Example script to check if a number is positive, negative, or zero

read -p "Enter a number: " num

if [ $num -gt 0 ]; then
   echo "The number is positive."
elif [ $num -lt 0 ]; then
   echo "The number is negative."
else
   echo "The number is zero."
fi

``` 

<img width="958" alt="to check if no is positive or negative" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/91a6ff93-29be-4a83-8af4-844d50a500fa">

- Iterating through a listing using a loop

To list all the number from 1-5

Run

```

# Example script to print numbers from 1 to 5 using a for loop

for (( i=1; i<=5; i++ ))
do
    echo $i
done 

```

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/869023a7-d42a-4529-9f05-261ae37a7092)

**Command line subtitution**: Allow you to capture the output of a command and use it as a value within your script. you can use the backtick or $()syntax for command subtitution.
- To print current date using the backtick .
  Run

  ```
  
  # Using backtick for command line subtitution 

  current_date=`date +%Y-%m-%d`

  echo $current_date

  ```
  
<img width="872" alt="using back tick for command substituition" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/dcde2d20-d545-4905-8fe0-07857e34f954">

- To print current date using $()

Run

```
#! /bin/bash

# Syntax for command substuition 

current_date=$(date +%Y-%m-%d)
echo $current_date

```

<img width="960" alt="syntax for command substitution" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/f32e8d65-e283-414b-93a2-f5cb585e8346">

 #INPUT AND OUTPUT 

 Bash provides various ways to handle inputs and Output. ,you can use the read command to accept user input,and output text through the console using the echo command. Additionally you can redict input and output using operators
 
- >to ouput to a file

- < to input from a file

- | to pipe the output of one into the input of another

- To accept user input e.g

  Run

```
  
  echo "Enter your name:"
read name

```

<img width="920" alt="output text to tye terminal" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/8a3fbcc6-767c-46c3-b22b-27e72e268494">


- To output Text to Terminal e.g

Run `echo my name is bukola` 


<img width="920" alt="output text to tye terminal" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/b58ac934-0a96-4aac-b037-5b4462270a1b">

- To output the result of a command line into a file

- Run `echo "Hello world" index.txt`

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/a8e31aff-59ea-4e84-8848-4577a5014c6f)

- pass the content of a file as input to a command

- Run grep "w" < index.txt

- pass the result of a command as input to another command

- Run echo "hello world" | grep "pattern"

# Functions

Bash allows you to define and use functions to group related commands together.functions provides a way to modularize your code and make it more reusable. you can define function using the function keyword or simply by declaring the function name followed by parenthesis.

- To Define a function to greet user

-Run

```

# Define a function to greet the user
greet() {
    echo "Hello, $1! Nice to meet you."
}

# Call the greet function and pass the name as an argument
greet "John"

```

<img width="876" alt="call the greet function and pas sthe name as an argument" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/e7ab307b-4048-433c-a77f-26910b16ccd2">

## Writing a shell script
- Make a folder called shell-scripting where all the files will be kept

Run `mkdir shell-scripting`
-create a file called user-input.sh

Run `touch user-input.sh`

<img width="953" alt="mkdir real" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/a4635385-baee-4362-bd80-bb13e3a93732">

- Open user-input.sh file with a code editor and paste the following code and save

paste

```

# Prompt the user for their name
echo "Enter your name:"
read name

# Display a greeting with the entered name
echo "Hello, $name! Nice to meet you."

```

-change the file permission to an executable file

Run `chmod +x user-input.sh`

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/7ad02831-202c-44e0-bf27-3d66a2d64ae1)

To run the script, Run  `./user-input.sh`

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/e0a1a361-3e0f-40f7-9526-deb7466ebd68)

## Directory Manipulation and Navigation

To write a script that will display the current directory, create a new directory called "my_directory"change to that directory, create two new files inside it, list the files and move back one level up,remove the "my_directory" and its contents and finally list the file in the current directory.

- create a file called navigating-linux-filesystem.sh

Run `touch navigating-linux-filesystem.sh`

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/258801a5-064b-415e-9e90-8ac540256d10)

- Open file with code editor paste the following code and save

```
 
# Display current directory
echo "Current directory: $PWD"

# Create a new directory
echo "Creating a new directory..."
mkdir my_directory
echo "New directory created."

# Change to the new directory
echo "Changing to the new directory..."
cd my_directory
echo "Current directory: $PWD"

# Create some files
echo "Creating files..."
touch file1.txt
touch file2.txt
echo "Files created."

# List the files in the current directory
echo "Files in the current directory:"
ls

# Move one level up
echo "Moving one level up..."
cd ..
echo "Current directory: $PWD"

# Remove the new directory and its contents
echo "Removing the new directory..."
rm -rf my_directory
echo "Directory removed."

# List the files in the current directory again
echo "Files in the current directory:"
ls

```

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/12159c10-e23f-4273-947b-2761a9aa6a92)

- Run chmod +x navigating-linux-filesystem.sh to make the file executable

- Run the script ./navigating-linux-filesystem.sh


![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/12159c10-e23f-4273-947b-2761a9aa6a92)

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/83fce706-8ee9-4362-b2f4-513cc42e28ae)

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/2b27dae4-e425-44e2-acfb-02cd5b8c7613)


## File Operation and Sorting

To write a script that can create three files(file1.txt,file2.txt and file3.txt),display the file in their current order, sort them alphabetically,save the sorted files in the (sorted_files.txt) display the sorted files,removes the original files,rename the sorted files to sorted_files_sorted_alphabetically.txt and finally display the content of the final sorted files.

- Open a file called (sorting.sh) by running  `touch sorting.sh`
 
<img width="960" alt="files sorting" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/61e9ef5d-9b02-40cc-b557-258ec466600c">

<img width="934" alt="file sorting second one" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/71fe6a06-ec9a-4cf3-b230-14e6f2512e11">


**Working with numbers and calculations**

To write a script that defines two variables num1 and num2, with numeric values, perform basic arithmethic operations (addition,subtraction,multiplication,division and modules) and display its results. it also perform more complex operation such as raising numb1 to power 2 and calculatin the square root of num2, and display those results as well.

Create a file called calculation.sh using `touch calculation.sh`
- Open the calculations.sh file using a code editor, paste the following code and
  
```

# Define two variables with numeric values
num1=10
num2=5

# Perform basic arithmetic operations
sum=$((num1 + num2))
difference=$((num1 - num2))
product=$((num1 * num2))
quotient=$((num1 / num2))
remainder=$((num1 % num2))

# Display the results
echo "Number 1: $num1"
echo "Number 2: $num2"
echo "Sum: $sum"
echo "Difference: $difference"
echo "Product: $product"
echo "Quotient: $quotient"
echo "Remainder: $remainder"

# Perform some more complex calculations
power_of_2=$((num1 ** 2))
square_root=$(awk "BEGIN{ sqrt=$num2; print sqrt }")

# Display the results
echo "Number 1 raised to the power of 2: $power_of_2"
echo "Square root of number 2: $square_root"

```

![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/379fe62f-80b6-447d-97b2-7f90df0da2a1)

- To make the calculations.sh file executable  `Run chmod +x calculations.sh`
  Run the script `./calculations.sh`
  ![image](https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/9072efd7-f336-403d-9810-c623d3b0a860)

**File Back up and Stamping**

This script defines source directory and backup directory paths. it then create timestamps using the current date and time,and create a backup directory with the timestamp appended to its name. The script then copies all files from the source directory to the backup directory using the cp command with -r option for recursive coping. Finally,it displays a message indicating the completion of the backup process and shows the path of the backup directory with the timestamp

- To create a file called backup.sh run `touch backup.sh`  Then
- Open the backup.sh file with a code editor, paste the code below and save

```

# Define the source directory and backup directory
source_dir="/c/Users/HP/Documents"
backup_dir="$Home/path/to/backup_directory"

# Create a timestamp with the current date and time
timestamp=$(date +"%Y%m%d%H%M%S")

# Create a backup directory with the timestamp
backup_dir_with_timestamp="$backup_dir/backup_$timestamp"

# Create the backup directory
mkdir -p "$backup_dir_with_timestamp"

# Copy all files from the source directory to the backup directory
cp -r "$source_dir"/* "$backup_dir_with_timestamp"

# Display a message indicating the backup process is complete
echo "Backup completed. Files copied to: $backup_dir_with_timestamp"

```

<img width="739" alt="newww" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/84def848-06c9-493c-8590-33bd117f9387">

-To make the backup.sh file executable, `run chmod +x backup.sh`

-Run the script `./backup.sh`

<img width="958" alt="backup completed" src="https://github.com/Bukolaogunwale1/Shell-Scripting--project/assets/122865359/28f40ea4-6c18-4cf5-b1a3-2d046363a20e">




