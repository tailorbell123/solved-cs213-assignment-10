Download Link: https://assignmentchef.com/product/solved-cs213-assignment-10
<br>
5/5 - (1 vote)

In this lab you will learn to write awk scripts that involve: • built-in variables and functions• expressions and operators• basic pattern matching

3 Background

System administrators often are required to allocate a fixed amount of storage space to users and monitor the space usage. The storage is typically allocated on a file server. When the space usage by any user goes above a threshold, T, an email is sent to the user notifying about the possibility of exhausting the quota of storage space allocated.

4 Problems

4.1 Problem 1

In this problem, you will write an awk script, problem1.awk, to detect if the space usage by any directory goes above 30% of its allocated storage space. If the space usage goes above this threshold, you should output to the console the directory name along with other statistics as mentioned below.

You are provided an input file, input1.txt, to use with problem1.awk. The input1.txt file contains storage space statistics of devices1. The first line of the output printed must have four columns:

<pre>File System|Available Storage|Used|Percentage</pre>

Any other line of expected output looks like (Note that there are no blank spaces in between columns): /dev/loop2|15104|15104|100%your script will be run as:

1devices are represented as directories in Linux

1

awk -f problem1.awk input1.txtHint: check built-in variables and functions OFS, FNR, substr, and length.

4.2 Problem 2

In this problem you will write an awk script, problem2.awk, to print the number of devices that are using all their allocated storage (100%). Use the same input file (input1.txt) as in Problem 1. Your output must be printed onto the console and the first line must print:

<pre>Number of devices on full capacity:</pre>

followed by the name of the device(s) on subsequent lines:

/dev/loop2 /dev/loop3 ..

so on.Finally, the last line must print:Total: N devices,where N is the number of devices having 100% usage.