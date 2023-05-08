# c_21_uppercase

## DESCRIPTION

The program takes a string from the user, then changes the lowercase letters to uppercase.
Uppercase letters in the user string will remain uppercase.

## ALGORITHM

To change the lowercase letters to uppercase we have to look at the ASCII table. 
There is a pattern we recognize between upper and lowercase letters, let's see two examples:

| Lowercase Letter 	| ASCII code (DEC)	| Uppercase Letter	| ASCII code (DEC)	|
|-------------------|-------------------|-------------------|-------------------|
| a 			   	| 97				| A					| 65				|
| c					| 99				| C					| 67				|

### v1.0  
There is always __32__ between the lowercase and uppercase letters.
We can iterate through the letters of a string in loop and check each character in the string. If the character is between 'a' and 'z' then we have to subtract 32 from the character's decimal value, this way we change it to uppercase. 

### v2.0  
The best way is using a library where this process is already implemented. This library is `ctype.h`.


## INSTALL LIBRARIES

The source code uses the cs50 library what you can download [HERE](https://github.com/cs50/libcs50).

To install the cs50 library follow the steps:

1. Open git bash terminal and change the current working directory to `src`:   
  `cd ./libsc50/src`

2. Compile the cs50.c source into .o with:  
  `gcc -c cs50.c -o cs50.o`

3. Make the library archive:  
  `ar rcs libcs50.a cs50.o`

4. Copy the `libcs50.a` file into your compiler's `lib` directory

5. Copy the `cs50.h` file into your compiler's `include` directory


## COMPILE AND RUN THE CODE

The code is written in C, the compiler used to generate the exe is: `gcc Rev10, Built by MSYS2 project 12.2.0`

Run the below code in terminal (git bash) to compile the source:

> gcc uppercase.c -lcs50 -o ./build/uppercase

To run the executable run the below code in terminal (git bash):

> ./build/uppercase.exe
