# c_22_commandLineArgument

## DESCRIPTION

The program takes a command line argument as a user's name, then greets the user.

In code below we declared the main function to **not** have any arguments (**void**) and have a return value which type is integer.
> int main(void)

But we can declare the main function to have command line arguments:
> int main(int argc, string argv[])

**argc** is the argument count, it needed to know how much words there are in the *argv[]* string array.

**argv[]** is a string array which will contain all the words we type into the prompt.

**argv[0]** is always the first word in the command prompt. If we like to run the program as the following:

> ./build/commandLineArgument.exe TheUserInput

then

> argv[0] = "./build/commandLineArgument.exe"

> argv[1] = "TheUserInput"

> argv[2] = "(null)"

The **argc** in the above case would be equal to **2** because there are two words in the string array exluded the null at the end of the array.

## INSTALL LIBRARIES

The source code uses the cs50 library what you can download [HERE](https://github.com/cs50/libcs50).

To install the cs50 library follow the steps:

1. Open git bash terminal and change the current working directory to `src`:   
  	> cd ./libsc50/src

2. Compile the cs50.c source into .o with:
	> gcc -c cs50.c -o cs50.o

3. Make the library archive:  
  	> ar rcs libcs50.a cs50.o

4. Copy the `libcs50.a` file into your compiler's `lib` directory

5. Copy the `cs50.h` file into your compiler's `include` directory


## COMPILE AND RUN THE CODE

The code is written in C, the compiler used to generate the exe is: `gcc Rev10, Built by MSYS2 project 12.2.0`

Run the below code in terminal (git bash) to compile the source:

> gcc commandLineArgument.c -lcs50 -o ./build/commandLineArgument

To run the executable run the below code in terminal (git bash):

> ./build/commandLineArgument.exe
