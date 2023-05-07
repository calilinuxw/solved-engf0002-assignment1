Download Link: https://assignmentchef.com/product/solved-engf0002-assignment1
<br>
The following exercises are intended to get you started with Python. At the very least, you must complete the prerequisites before the next lecture. If you’ve programmed in python before, you can probably skip the first few exercises. If you’ve not programmed in python before, get as far as you can, but we don’t expect you to complete everything.

This assignment is not assessed, but you do need to hand it in via Moodle by Monday 7th October at 12 noon so we can see how you’ve got on. Feel free to collaborate with your friends, but list who you have collaborated with in your submission.

<h1>Prerequisite 1</h1>

Install python 3.7 on the machine you intend to use to do your coursework. If you have problems, come and see the ENGF0002 programming clinic.

<h1>Prerequisite 2</h1>

Install git on your machine. This will allow you to check out software and slides from github. Familiarise yourself with the basics of checking out and updating from a repository.

<h1>Prerequisite 3</h1>

Ensure you can run tkinter packages using your python 3 installation, as we’ll need these for next week’s assignments. Tkinter usually comes pre-installed with python installations, but in some cases you’ll need to install a separate package.

Test your install by checking out

mhandley/ENGF0002-2019/Assignments/assignment1/tkintertest.py from github and checking it runs properly.

From the command line, if python is installed as python3, you can run this as:

python3 tkintertest.py

<h1>Exercise 1: GCD example from class</h1>

Type in the GCD example from class (it’s also in gcd-function.png in the git respository), and get it to run.

Why type it in, rather than cut and paste, or checkout from github? Simply, we want you to get set up with an appropriate editor, and understand the very basics of python. If you type it in, you’ll remember it. Likely you’ll mistype something, and have to understand what python’s error messages are telling you. And at the least, you’ll need to get to grips with python’s use of whitespace to indicate semantic grouping of statements. Doing this with code where you know what the answer should be is useful if you’ve not programmed in python before.

<h1>Exercise 2: Odd or Even</h1>

Write a program that asks the user for a number. Depending on whether the number is even or odd, print out an appropriate message to the user.

Hint: The python3 input() function will read input from the keyboard, but in python3 the result will be a text string, not an integer. You may need to use the int() function to convert it to an integer type.

<h1>Exercise 3: Fizzbuzz</h1>

Write a program that prints the numbers from 1 to 100. But for multiples of three print “Fizz” instead of the number and for the multiples of five print “Buzz”. For numbers which are multiples of both three and five print “FizzBuzz”.

This is one of those classic interview questions that are supposed to distinguish candidates that can program from those than cannot. There are lots of versions of FizzBuzz online, but we’d like you to attempt your own before you go hunting for online solutions.

Hint: modular arithmetic might be useful.

Hint: you can do this with a while loop, as in the GCD example, but it’s more elegant to use a for loop and range operator.

<h1>Exercise 4: Calculating Pi</h1>

We want to compute an approximation of <em>π </em>(3.141592…) up to a certain precision. One way to do this is by using a <em>Monte Carlo method </em>as follows. Consider the square of edge length 1 and the circle of radius 1/2 inscribed in the square, as depicted below. Generate random points within the square. Suppose <em>N</em><sub>hits </sub>points hit the circle, out of a total of <em>N</em><sub>tot </sub>points.

<table width="606">

 <tbody>

  <tr>

   <td width="438">A B C D E F G H I J K L M N O P Q R S T U V W X Y Z</td>

   <td width="167">(original alphabet)</td>

  </tr>

  <tr>

   <td width="438">N O P Q R S T U V W X Y Z A B C D E F G H I J K L M</td>

   <td width="167">(ciphertext alphabet)</td>

  </tr>

 </tbody>

</table>

Then we can approximate <em>π </em>by noting that <em>N</em><sub>hits </sub>estimates the area of the circle and <em>N</em><sub>tot </sub>estimates the area of the square. In fact, recalling that the area of the circle is <em>πr</em><sup>2</sup>, for <em>r</em>=1<em>/</em>2 we have

<em>A</em>circle             <em>π       N</em>hits

<em>A</em>square    4 ≈ <em>N</em>tot =

Implement a function estimatepi(precision) that returns an approximation of <em>π </em>up to precision decimal positions. Use the function random() from the module random to generate random numbers between 0 and 1. (Hint: the more points you generate, the more precise your approximation will be.)

<h1>Exercise 5: Breaking Caesar’s Cipher</h1>

A <em>simple substitution cipher </em>is an encryption method where each letter of the alphabet is replaced by another one, according to a ciphertext alphabet. The Caesar’s Cipher is a very simply substitution cipher, where each letter is replaced by one <em>n </em>places later in the alphabet, wrapping back from Z to A if necessary. For instance, in the cipher

A is replaced by N, B by O and so on. Applying this cipher to the word HELLO produces the word URYYB.

Implement a function breakcipher(text) that takes a string – which is assumed to be encrypted using a Caesar cipher – finds the ciphertext alphabet used to encrypt it and returns the decrypted string. Assume that the decrypted string will be in English, with letters A-Z and no spaces.

As there are only 26 possible Caesar’s Ciphers, you can easily break them by hand. But how would a program automatically decide which of the 26 possible offsets is the correct one?