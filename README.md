Download Link: https://assignmentchef.com/product/solved-lab-6-reverse-words-on-line
<br>
<p class="ui header product-top-header" title="Lab 6 Reverse words on line Solution">Lab 6Reverse words on lineObjectivesPractice taking program argumentsPractice using C libraries and functionsPractice converting strings to integersPractice manipulating C stringsPractice top-down program design and reading pseudocodeOverviewFor this lab, you will write a program that reads N lines of data from the command-line, one entire line at a time, and reverses the words of each line. In this example, N = 1:

[esus] $ ./lab6 1the quick brown fox jumps over the lazy dogdog lazy the over jumps fox brown quick the

N is a number provided via command-line argument.

DetailsRequirements:

Take in a single command-line argument.Print an error message if not enough or too many program argumentsConvert it to an integer (print error and quit if entered less than 0)Read in that many lines from standard input.For each line, scan the entire line using fgets.Implement a function to reverse the words in the line, and call it on every input line.The words must appear in reverse order, but still readable from left to right.NOTE: Punctuation and extra spaces should be omitted in the reversed stringPrint out the reversed lineCommand-line argumentCommand-line arguments are a way for you to provide input to the program at the moment it is executed. For this program, you will use a single command-line argument to provide the number of lines to be read from standard input, as an integer greater than or equal to zero.

Convert string to intTo obtain the value of N from this command-line argument, you must convert it to an int. Use the function strtol to accomplish this. With the call to strtol, you must provide the ‘base’ of the number returned. In our case, we want a standard ‘base 10’ number returned. In addition, you will need to use type casting to convert the result of the function back into an int.

int N = (int) strtol( str, NULL, 10);

NOTE: Be sure to #include &lt;stdlib.h to use this function.Standard Input using fgetsIn this lab, you will use a function called fgets to read input from the keyboard. This function is also used to read data from files, however we can use it to read keyboard input by specifying the global variable stdin as the file pointer parameter. Up until now, we have typically used scanf to accomplish this, but fgets is actually better, because we can control how much data is read in. This helps to prevent buffer overflow errors, in which the string is stored in memory that is not allocated for it. To read input in this way, use the function like this:

#define SIZE 80…char str[SIZE];if ( fgets( str, SIZE, stdin ) ) {// input was successful}

Algorithm to reverse a stringYou may attempt to design an algorithm to solve this problem on your own if you’d like. However, you may also implement a C language version of the pseudocode provided below.

PROCEDURE reverse( string line ):declare local strings: temp, wordidx &lt;- string length of lineword_len &lt;- 0

// scan thru characters one by oneloop until idx &lt; 0:if line[ idx ] is a space and word_len 0:

copy word_len characters from line to wordconcatenate word + ” ” on end of tempword_len &lt;- 0 // reset word length to 0

else if line[ idx ] is alphanumeric:

word_len &lt;- word_len + 1

end ifend loop

// copy over the last word after the loop (if any)if word_len 0:copy word_len characters from line to wordconcatenate word on end of tempend if

line &lt;- temp // copy temp back into lineend PROCEDURE

Functions of intereststdio.h:

fgetsRead data from files or standard inputstdlib.h:

strtolConvert a string to a long integerctype.h:

isalnumChecks if a character is alphanumericstring.h:

memsetSets memory to a specific value. Useful to re-initialize local string variables to 0 for re-use in a loop.strncpyCopies some number of characters out of a string.strlenGets the number of characters in a string (not including the null terminator).strcatConcatenates one string onto another.strchrSearches a string for the first occurrance of the given characterExample Execution[esus] $ ./lab6ERROR: Please provide an integer greater than or equal to 0

[esus] $ ./lab6 -3ERROR: Please provide an integer greater than or equal to 0

[esus] $ ./lab6 2the quick brown fox jumps over the lazy dogdog lazy the over jumps fox brown quick thewhat is lovelove is what

[esus] $ ./lab6 1a test… i demand a test!test a demand i test a

Compile &amp; TestCompile your program using this gcc command. c99 is a shortcut for running gcc -std=c99, which uses the C99 standard instead of the default C89 standard.

$ c99 -Wall lab6.c -o lab6

NOTE: Make sure you output what is expected, nothing more and nothing less.You should use the Lab Grader tool to check your work. This assignment name is ‘lab6’, so you should run the tool like this (substitute your own filename):

./grade lab6 last_first_lab6.c

ResourcesYou should attend the Friday Lab session to seek assistance from the TAs and CAs.For specific questions, attend the weekly lab session or attend the TA’s office hours.You are encouraged to use resources or tutorials on the internet to learn unix or C. Check the class resource list for some links to resources.SubmissionAssigned: March 28thLab Day: April 1stDue Date: April 4th, 8:00am

Make sure you included ample and informative comments – it is 20% of your grade!Rename your C file to last_first_lab6.c and substitute your last and first name.

NOTE: If you fail to follow the above file naming conventions, your program cannot be graded automatically and you will lose points.Submit your .c file to the D2L Dropbox for Lab 6. Detailed Instructions

NOTE: Submit only your C file to D2L. Do not submit your object file or executable program. Do not archive (e.g. zip) your file.Each student will complete and submit this assignment individually. Submit your work on or before the deadline as late work will receive a 50% penalty. Labs submitted more than 24 hours late will not be accepted.

<span class="kksr-muted">Rate this product</span>