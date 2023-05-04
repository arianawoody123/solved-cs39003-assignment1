Download Link: https://assignmentchef.com/product/solved-cs39003-assignment1
<br>
<ol>

 <li>Translate the following two C programs using GCC/Linux to the assembly language of x86-64 (Intel 64-bit processor) without optimization. Use the following command to generate the assembly code:</li>

</ol>

gcc -Wall -S &lt;program name&gt;.c

<ol start="2">

 <li>Rename the generated assembly files as ass1a roll.s and ass1b roll.s, where “roll” is your roll number. Add comments for each line of the assembly language program. Your comment should explain the functionality of the instruction and the connection to the original C program. Also make sure that your commented file can be compiled to generate the executable file. Upload the two files on Moodle server.</li>

</ol>

<strong>Program 1: </strong><em>ass1a.c</em>

#include &lt;stdio.h&gt;

int main()

{ int num1, num2, greater;

num1 = 45; num2 = 68;

if (num1 &gt; num2)       greater = num1; else      greater = num2;

printf (“
The greater number is: %d”, greater);

return 0;

}

1

<strong>Program 2: </strong><em>ass1b.c</em>

#include &lt;stdio.h&gt;

int GCD (int, int); int GCD4 (int, int, int, int);

int main()

{

int a = 45, b = 99, c = 18, d = 180, result; result = GCD4 (a, b, c, d);

printf (“
GCD of %d, %d, %d and %d is: %d”,

a, b, c, d, result);

printf (“
”);

return 0;

}

int GCD4 (int n1, int n2, int n3, int n4)

{ int t1, t2, t3;

t1 = GCD (n1, n2); t2 = GCD (n3, n4); t3 = GCD (t1, t2);

return t3; }

int GCD (int num1, int num2)

{ int temp;

while (num1 % num2 != 0)

{

temp = num1 % num2; num1 = num2; num2 = temp; }

return num2;

}