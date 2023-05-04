Download Link: https://assignmentchef.com/product/solved-csci-1133-assignment-2-relativistic-length-contraction
<br>
Use the following template for EVERY function that you write (note: a helper function is a function so it gets a template.)

#==========================================

# Purpose: (What does the function do?)

# Input Parameter(s): (Each parameter by name and what it represents)

# Return Value(s): (What gets returned? Possibilities?)

#==========================================




<h1>Problem A.​Relativistic Length Contraction</h1>

Einstein’s Theory of <u>​</u><u><a href="https://www.youtube.com/watch?v=AInCqm5nCzw">Special Relativity</a></u><u>​</u> tells us that distances between objects moving relative to our inertial reference frame are contracted (shortened).  The upshot of this is that it means that if we put an astronaut on a spaceship travelling at 99% of the speed of light to Alpha Centauri, which is 4.37 light-years away, it will take about 4.41 years according to observers on Earth, but only about 0.62 years according to the astronaut.  This is because Alpha Centauri and Earth would both be moving at about 99% of the speed of light relative to the astronaut, so the distance between the two objects would be contracted greatly from the astronaut’s perspective.




If this gives you a headache, don’t worry about it: you don’t actually need to understand relativity to do this problem.  Write a function called ​length_contract(dist, speed), which takes in two​ numerical values as parameters: ​dist​ is the original distance (in meters) between two objects, and speed​ is the speed (in meters/second) at which we are travelling relative to the two objects.  The function ​<strong>returns</strong>​ (not prints) the contracted distance between the two objects from our reference frame, given by the formula:







where L​0 is the original distance, v is our speed, c is the speed of light (approximate this as 300000000<sub>​ </sub>8            meters/second, or 3 * 10​​), and L is contracted distance.

We’re ignoring several things here, such as the fact that the objects could be moving relative to each other (especially if they’re two different star systems), the time required to accelerate and slow down, and gravitational effects from General Relativity, but this isn’t a terrible approximation of how it would actually work.




<strong>Hint: </strong>

<ul>

 <li>You can find the square root of x without importing math by using the built-in exponent operator:</li>

</ul>

math.sqrt(x) == x**0.5




<strong>Constraints</strong>​:

<ul>

 <li>Do not import/use any Python modules.</li>

 <li>Do not use the input() function,</li>

 <li>Your submission should have no code outside of function definitions (comments are fine)</li>

</ul>




<strong>Examples</strong>​:

&gt;&gt;&gt; length_contract(100, 150000000)

86.60254037844386




&gt;&gt;&gt; length_contract(30000, 0)

30000.0




&gt;&gt;&gt; length_contract(0, 200000000)

0.0




&gt;&gt;&gt; length_contract(4.37, 297000000)

0.6164643623113996




&gt;&gt;&gt; length_contract(1000000, 299999999)

81.64965807128421










<h2>Problem B. ​<strong>The Bessel Run</strong></h2>

Few people realize that astronomer ​<u><a href="https://en.wikipedia.org/wiki/Friedrich_Bessel">Friedrich Bessel</a></u>​ is not only still alive, but is currently working as an intergalactic smuggler pilot, running some contraband materials through a particularly dangerous (and very large) region of space.  The run is 12 parsecs long, as measured by some “stationary” observer (there’s a reason I put that in quotes, but this isn’t a Physics class so we’re ignoring it).   A parsec is a unit of distance equal to about 3.26 light-years.  Bessel intends to fly his spaceship at close to light speed, so that the path will appear much shorter from his perspective due to relativistic length contraction.




Write a function ​bessel_run(speed)​, that takes a single numerical value speed, representing Bessel’s average speed in the run, given in meters/second.




The function must ​<strong>print</strong>​ out the time required to traverse the segment, as seen by a stationary observer, in years (this is just distance / speed, no relativity needed).




The function must ​<strong>return </strong>​the time required to traverse the segment, as seen by Bessel, in years (use the length_contract​ function from problem A, and then compute contracted distance / speed).




You’ll need to convert from parsecs to meters and from seconds to years to do this correctly:

<ul>

 <li>1 parsec = 3.086 * 10​<sup>16</sup>​ meters</li>

 <li>1 year = 31557600 seconds (using astronomical year, not calendar year)</li>

</ul>

Note that because we are using approximations, so long as your answers are within about 1% of the correct value, we’ll accept them.




Try to roughly match the print format in the examples below (you won’t lose points so long as it is reasonable, but it does make it easier to grade).




<strong>Hint: </strong>

<ul>

 <li>You may want to consider writing helper functions to do some of the tasks like unit conversions. Remember, you must write documentation for all functions you write, including helpers.</li>

</ul>




<strong>Constraints</strong>​:

<ul>

 <li>Do not import/use any Python modules.</li>

 <li>Do not use the input() function,</li>

 <li>Your submission should have no code outside of function definitions (comments are fine) You must call the ​length_contract​ function from problem A within ​bessel_run​.</li>

</ul>




<strong>             </strong>

<strong>Examples</strong>​ (value in ​<strong>bold</strong>​ is returned, text in ​<em>italics</em>​ is printed):

&gt;&gt;&gt; bessel_run(200000000)

<em>58.71385083713851 </em>

<strong>43.76272056420821 </strong>

&gt;&gt;&gt; bessel_run(88)

<em>133440570.08440569 </em>

<strong>133440570.08439995 </strong>




&gt;&gt;&gt; bessel_run(299999999)

<em>39.14256735523423 </em>

<strong>0.0031959772405870867 </strong>

<strong> </strong>

&gt;&gt;&gt; bessel_run(150000000) + bessel_run(100000000)

<em>78.28513444951801 </em>

<em>117.42770167427702 </em>

<strong>178.50881404267247 </strong>

<strong> </strong>







<h1>Problem C. (20<em> points</em>​ ​)  Who needs loops?​</h1>

Your friend Ester, who took this class last semester, is taunting you.  She says that because you haven’t learned loops yet, you would need more than 100 lines of code to print out 100 lines of text.  Prove her wrong.




Write a function called ​print_100()​ with no parameters that prints out the string “Who needs loops?” exactly 100 times in a row, once per line, subject to the constraints below.  This function does not return anything.




<strong>Hints: </strong>

<ul>

 <li>You will need to write more than one function for this problem. In fact, it is very difficult to do this problem without at least three.</li>

 <li>Make a function that prints out “Who needs loops?” a reasonable number of times, and then think about what would happen if you called that function multiple times inside another function.</li>

</ul>




<strong>Constraints</strong>​:

<ul>

 <li>You can write a maximum of ​<strong>20</strong>​ lines of code for this problem. This includes all functions you write for this problem (including the line for the function definition), but does not include comments, blank lines, or the functions for problems A and B.</li>

 <li>Do not import/use any Python modules</li>

 <li>Do not use any loops (for or while)</li>

 <li>Do not use the newline character ​’
’</li>

 <li>Do not use the input() function</li>

 <li>Your submission should have no code outside of function definitions (comments are fine).</li>

 <li>Remember, you need to document every function you write</li>

</ul>




<strong>Example</strong>​:

&gt;&gt;&gt; print_100()

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?

Who needs loops?


