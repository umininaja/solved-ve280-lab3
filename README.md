Download Link: https://assignmentchef.com/product/solved-ve280-lab3
<br>
Ex1. Card Game!

Related Topics: <em>Recursion</em>.

<strong>Problem:</strong> Let’s play with cards! You are given a sequence of n cards, all placed face down, and the number written on the other side of each card is guaranteed to be unique and positive. Each card is also indexed from 0 to n-1, which corresponds to its position in the sequence. Among the cards, there is always one with <strong>280</strong> on it. The rule of the game is stated as follows:

<ol>

 <li>You will be given a start position, namely <em>p</em>. Make its face up.</li>

 <li>If the card on that position has value <strong>280</strong>, then you win. Otherwise, proceed to step 3.</li>

 <li>Suppose the value on the card at this position <em>p</em> is <em>v</em>. Then you can choose <strong>either</strong> the card on position <em>p+v</em> <strong>or</strong> position <em>p-v</em>. Once a card is chosen, <strong>make its face up</strong>. Note that the chosen position must be <strong>valid</strong>, i.e., you cannot choose a card outside the given sequence. Moreover, you cannot choose a card already face up. If no card can be chosen, you lose.</li>

 <li>Once you’ve picked your card from step 3, update the current position, go to step 2.</li>

</ol>

<strong>Requirement:</strong> Please refer to ex1.cpp in the starter_files folder. The skeleton code is already provided. You are required to use <strong>recursion</strong> to implement the function below, where count is the number of element in the card array, arr[] represents the sequence of values on each card, position is the start position of the game. You may use a helper function if you want.

<strong>Input Format:</strong> There will be 3 lines, the first line only contains the number of cards in the sequence. The second line gives the values of all the cards. The third line specifies the start position (0-index based).

<strong>Output Format:</strong> Either 0 (for false) or 1 (for true).

<strong>Hint:</strong>

<ol>

 <li>We guarantee that the start position is valid.</li>

 <li>Once a card has been chosen, you cannot choose it again. Therefore, you should find a way to record this.</li>

</ol>

Ex2. Fold And Fold Again

Related Topics: <em>Recursion</em>, <em>Function pointer</em>.

In this exercise, you will need to implement the <a href="https://en.wikipedia.org/wiki/Fold_(higher-order_function)">fold</a> function below, where count is the number of elements in the arr array, fn points to a function, which takes in two ints and returns an int, and initial is a value.

You are welcomed to write a helper function for the recursion.

If count == 0, just return the initial value. Otherwise, take count = 3 for example, the return value could have been equivalently calculated as follows:

In short, the fold function will take each element in the array as well as the previous return value, until we have gone through the whole array. And it will return the last calculated value.

To help you understand how the fold function works, write two fn functions to be used with the fold function:

a function called fn_add such that fold(n, arr, fn_add, 0) returns the sum of the elements in arr. a function called fn_count_odd such that fold(n, arr, fn_count_odd, 0) returns the number of odd numbers in arr.

<strong>Hint:</strong> Please be aware that the order of inputs into the fn function matters. The first one should be the element from the array, and the second one should be either the initial value or the previous return value of fn.

<strong>Requirement:</strong> Please refer to ex2.cpp in the starter_files folder, you will need to implement fold, fn_add and fn_count_odd functions. You only need to submit ex2.cpp for this problem.

Ex.3 Play with Integers

Related Topics: <em>Program Arguments</em>.

<strong>Problem:</strong> You will use cin to read an array of int and do some data manipulation according to the program arguments. There are several options for the program:

–help: print the message Hey, I love Integers. and exit, ignore all other options.

–add: add all the numbers in the array, record the result. No need to worry about the integer overflow. –small &lt;int&gt;: find the smallest element in the array, add this element to the int passed through the argument, and print the result.

–verbose: verbose mode, see the output format for details.

<strong>Input Format:</strong> There will be 2 lines, the first line only contains the number of int in the array. The second line gives the whole array.

<strong>Example 1</strong> (contains –help):

<em>Program Argument:</em> ./ex3 –help or ./ex3 –verbose –help

<em>Output Format:</em> Hey, I love Integers. Notice that when we have –help in the argument, we will only print this line and return.

<strong>Example 2</strong> (contains add):

<em>Program Argument:</em> ./ex3 –add <em>Output Format:</em> 15 because 1+2+3+4+5=15.

<strong>Example 3</strong> (contains verbose):

<em>Program Argument:</em> ./ex3 –add –verbose <em>Output Format:</em>

<strong>Example 4</strong> (contains verbose):

<em>Program Argument:</em> ./ex3 –small 3 –verbose <em>Output Format:</em>

Note that if no data operation is mentioned in the argument, no matter whether the verbose mode is on or not, we simply output one line: No work to do!. If both data operations are there, always first output the things related to the <strong>add</strong> operations. Please also be aware that the order of all the options will be <strong>random </strong>and you may assume that there are no unknown options in the argument and the argument must be valid.

<strong>Requirement:</strong> Create a file with name ex3.cpp and write your function there.