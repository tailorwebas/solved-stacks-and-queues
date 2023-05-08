Download Link: https://assignmentchef.com/product/solved-stacks-and-queues
<br>
In this assignment, you will be implementing Stacks and Queues.  You will then use stacks and queues to test if words are palindromes, and use stacks to decompose phrases into words (to find new palindromes).




<ul>

 <li>Implement ​MyStack​ (use the included ​MyLinkedList​ to store the stack elements)

  <ul>

   <li>Implements S​ tackInterface</li>

  </ul></li>

</ul>

○      Throws a ​StackException​ if peek or pop are called on an empty stack

<ul>

 <li>Implement ​MyQueue ​(use ​MyLinkedList​ to store the stack elements)

  <ul>

   <li>Implements ​QueueInterface</li>

  </ul></li>

</ul>

○     Throws a ​QueueException ​ if peek or dequeue are called on an empty queue

<ul>

 <li>Test your MyStack and MyQueue ​<strong>thoroughly </strong></li>

 <li>In ​java

  <ul>

   <li>Implement ​stackToReverseString()​ using MyStack</li>

  </ul></li>

</ul>

○         Implement ​reverseStringAndRemoveNonAlpha()​  using ​MyStack

○    Implement ​isPalindrome()​, which returns true if a word or phrase is a palindrome, using M​ yStack ​ and M​ yQueue

○    CHALLENGE: Implement ​explorePalindrome() ​ which lists all possible backwards decompositions of a phrase (e.g. “evil guns” =&gt; snug live“), a common trick to make new palindromes (uses MyStack)

<ul>

 <li>Style requirements <strong>(</strong>​ <strong>NEW!) </strong>

  <ul>

   <li>Indent your code properly</li>

  </ul></li>

</ul>

■    There are several mainstream “styles” of indentation, pick one and be consistent.  EG: <a href="https://javaranch.com/styleLong.jsp">h</a>​ <a href="https://javaranch.com/styleLong.jsp">ttps</a><a href="https://javaranch.com/styleLong.jsp">://</a><a href="https://javaranch.com/styleLong.jsp">javaranch</a><a href="https://javaranch.com/styleLong.jsp">.</a><a href="https://javaranch.com/styleLong.jsp">c</a><a href="https://javaranch.com/styleLong.jsp">o</a><a href="https://javaranch.com/styleLong.jsp">m</a><a href="https://javaranch.com/styleLong.jsp">/</a><a href="https://javaranch.com/styleLong.jsp">styleL</a><a href="https://javaranch.com/styleLong.jsp">o</a><a href="https://javaranch.com/styleLong.jsp">ng</a><a href="https://javaranch.com/styleLong.jsp">.</a><a href="https://javaranch.com/styleLong.jsp">jsp</a>

○    Name your variables with helpful and descriptive names

■   Whats a good variable name? Here is a <a href="https://a-nickels-worth.blogspot.com/2016/04/a-guide-to-naming-variables.html">g</a>​ <a href="https://a-nickels-worth.blogspot.com/2016/04/a-guide-to-naming-variables.html">uide</a>

○    Add comments before every function, and in your code

■   Comments should say ​<strong>what you are trying to do</strong>​ and <strong>w</strong>​ <strong>hy </strong>

■   Consult this <a href="https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118">g</a>​ <a href="https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118">uide</a> <a href="https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118">t</a><a href="https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118">o </a><a href="https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118">c</a><a href="https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118">o</a><a href="https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118">mmenting</a>

<h1>Point breakdown</h1>

<strong>Stacks</strong>​ – 20 points

<strong>Queues</strong>​ – 20 points

<strong>Style</strong> ​ – 15 points




<strong>Implementing the functions: </strong>

String ​stackToReverseString​(MyStack)​ – 10 points

String ​reverseStringAndRemoveNonAlpha​(String)​ – 5 points

Boolean ​isPalindrome​(String)​ – 10 points

void​ ​explorePalindrome​()​ (and its helper)​ – 20 points




<h1>Implementing MyStack and MyQueue</h1>

In this assignment, we will be making heavy use of the classes M​ yStack​  and M​ yQueue​.  You have already implemented​ MyLinkedList.java​ in a previous assignment.  You can use your code, or the sample ​MyLinkedList.java ​provided.




Implement ​MyStack.java​ and​ MyQueue.java ​using the provided interfaces and exceptions.




Make sure you have implemented a ​public​ String t​ oString(​ ) ​ method on MyStack and MyQueue that prints out the contents of the stack from the top down and prints out the queue from the front to back. So, for example, after the following code:

MyStack stack = ​ new​  MyStack(); MyQueue queue = ​ new​  MyQueue();  stack.push(​ “Hello”​ ); queue.enqueue(​ “Hello”​ ); stack.push(​ “big”​ ); queue.enqueue(​ “big”​ ); stack.push(​ “world”​ ); queue.enqueue(​ “world”​ );




System.out.println(​ “Stack = “​  + stack);

System.out.println(​ “Queue = “​  + queue);




Then the output would be:

Stack = (world, big, hello)

Queue = (hello, big, world)




<strong>Test your code thoroughly!! </strong>W​         e have provided ​T estQueuesAndStacks.java ​ as an example of some ways to test your code, but you will want to edit it to try out many possible situations. Make sure your code behaves <strong>e</strong>​ <strong>xactly</strong>​ as you expect it to, before starting the second half of the assignment.

Is this a palindrome?

A palindrome is a word or phrase that reads the same backwards and forwards, if you ignore punctuation and spaces. For example:

<ul>

 <li>A dog! A panic in a pagoda!</li>

 <li>ABBA</li>

 <li>Cigar? Toss it in a can. It is so tragic. ● Yo, bottoms up! (U.S. motto, boy.) ●  Stressed was I ere I saw desserts.</li>

</ul>

(from <u>​</u><a href="http://www.palindromelist.net/palindromes-y/">http</a><a href="http://www.palindromelist.net/palindromes-y/">://</a><a href="http://www.palindromelist.net/palindromes-y/">www</a><a href="http://www.palindromelist.net/palindromes-y/">.</a><a href="http://www.palindromelist.net/palindromes-y/">palindr</a><a href="http://www.palindromelist.net/palindromes-y/">o</a><a href="http://www.palindromelist.net/palindromes-y/">melist</a><a href="http://www.palindromelist.net/palindromes-y/">.</a><a href="http://www.palindromelist.net/palindromes-y/">net</a><a href="http://www.palindromelist.net/palindromes-y/">/</a><a href="http://www.palindromelist.net/palindromes-y/">palindr</a><a href="http://www.palindromelist.net/palindromes-y/">o</a><a href="http://www.palindromelist.net/palindromes-y/">mes</a><a href="http://www.palindromelist.net/palindromes-y/">–</a><a href="http://www.palindromelist.net/palindromes-y/">y</a><a href="http://www.palindromelist.net/palindromes-y/">/</a><u>​</u><a href="http://www.palindromelist.net/palindromes-y/">)</a>




In this part of the assignment, you will be writing several functions in P​ alindrome.java t​ o test and create palindromes using your stack and queue implementations.

Example Input &amp; Output

Palindrome.java​ takes as input: a <strong>m</strong>​     <strong>ode</strong>,​ and some <strong>w</strong>​ <strong>ords.  </strong>T​ he mode is either “test” or “expand”, so the function call will be:




<strong>Test for palindromes </strong>

Are these phrases palindromes?

javac Palindrome.java &amp;&amp; java Palindrome test “oboe” “ABBA” “I’m alas, a salami” “evil liver” ‘oboe’: false

‘ABBA’: true

‘I’m alas, a salami’: true

‘evil liver’: false




<strong>Expand palindromes </strong>

Which words could be added to make this a palindrome?

javac Palindrome.java &amp;&amp; java Palindrome expand “an era live” “mug god” an era live:  evil a ren a an era live:  evil aren a an era live:  evil arena mug god:  dog gum




Functions to implement:

String s​ tackToReverseString(​ MyStack):​ ​ your toString function in your stack class prints out the stack in the order that things would be popped from it. What if we want to turn it into a string in the opposite order (the order that things were <strong>p</strong>​ <strong>ushed</strong> to it)?




In Palindrome.java, we do not have access to the internal representation of the stack’s list.  So instead, we have to pop everything off the stack, read it in order and push it pack onto the stack in the original order so that the stack is unchanged

(​<em>Whew!</em>​)

<ul>

 <li>Create an empty string</li>

 <li>Create a new temporary stack</li>

 <li>Pop everything from the original stack onto the new stack</li>

 <li>Pop everything from the new stack back onto the original stack ​<strong>and</strong>​ add it to the string</li>

</ul>


































String ​ reverseStringAndRemoveNonAlpha ​ (String)

Use a stack to reverse a string.  Similar to before.  Also, we want to not only  ●     Create a new stack.

<ul>

 <li>Iterate through the string, and push each character from the string onto the stack, but<strong> only if </strong>​they are alphabetic (ignore spaces and punctuation)</li>

</ul>

○ Character.isAlphabetic w​ ill be a useful function here!

<ul>

 <li>Pop everything from the stack to reconstruct the string in reverse.</li>

 <li>Note: your stack can only contain Objects. Java’s ​char​ datatype isn’t an object though! This means that you will have to wrap it (and later cast it) as a ​Character ​   Look up the Character class in Java’s documentation, or find out more about wrapper classes <a href="https://en.wikipedia.org/wiki/Primitive_wrapper_class">here</a>​.</li>

</ul>




Boolean ​ isPalindrome​ (String)

Implement this function using ​ <strong>both a stack and a queue. </strong>

To test if a string is a palindrome:

<ul>

 <li>Convert the string to lowercase (we don’t care about uppercase vs lowercase characters being different)</li>

 <li>Create a new stack and queue.</li>

 <li>Enqueue and push each character (if it is alphabetic, we don’t want to look at white space or punctuation)</li>

 <li>Pop each character from the stack and dequeue each character from the queue until one is empty</li>

 <li>Notice how in our above functions, pushing and then popping from a stack <strong>r</strong>​ <strong>eversed the order. </strong>​How will you use this to test whether this string is a palindrome?</li>

</ul>




void ​ explorePalindrome​ (String)

This function lists all possible endings that would make this string a palindrome, e.g.:

javac Palindrome.java &amp;&amp; java Palindrome expand “an era live” “mug god” an era live:  evil a ren a an era live:  evil aren a an era live:  evil arena




First, convert the string to lowercase and use your ​reverseStringAndRemoveNonAlpha function to reverse it and remove non-alphabetical characters.




Now, most of the work will be done by a recursive helper function to decompose this new string (“evilarena”) into words.  Takes the original string, the reversed string, an index, and the current stack of words we are building up

​ public​  ​ static​  ​ void​  ​ decomposeText​ (String originalText, String textToDecompose, ​ int​  index, MyStack decomposition)




We have provided a function​ String[] getWords(String text, i​ nt ​ index) t​ hat uses a dictionary to find which words could be created from a string at a given index.  For example getWords(​”isawere”​, ​0​) ​could find the words “i” and “is”,   ​ getWords(“​ isawere”,​ 2​ )​ ​ could find the words (“a”, “aw” and “awe”).




A recursion step:

<ul>

 <li><strong>If the index is at the end of the word, we are finished, print out the words (using reverse print) and the original text. </strong> Else: Find the potential words at that index ●            For each word:</li>

 <li>Push it to the stack</li>

</ul>

○   Recurse at the next index (not *just* i++)

○    If it was part of a correct solution, it will print itself out in a subsequent recursion step (if it reaches a conclusion)

<ul>

 <li>Pop it from the stack</li>

 <li>Confused? See below for a visual explanation of this approach.</li>

</ul>

○    As usual, println statements may help you understand your code’s operation if you get lost.  Consider outputting the list of words from getWords, or printing out the d​ ecomposition ​ stack each time you push or pop from it.  Just remove your debug statements before turning in your code.




<h1>Turning the code in</h1>




<ul>

 <li>Create a directory with the following name: &lt;student ID&gt;_assignment3 where you replace &lt;student ID&gt; with your actual student ID. For example, if your student ID is 1234567, then the directory name is 1234567_assignment3</li>

 <li>Put a copy of your edited files in the directory (MyQueue.java, MyStack.java, and Palindrome.java)</li>

 <li>Compress the folder using zip. Zip is a compression utility available on mac, linux and windows that can compress a directory into a single file. This should result in a file named &lt;student ID&gt;_assignment3.zip (with &lt;student ID&gt; replaced with your real ID of course).</li>

 <li>Double-check that your code compiles and that your files can unzip properly.</li>

</ul>

You are responsible for turning in working code.

<ul>

 <li>Upload the zip file through the page for <a href="https://canvas.ucsc.edu/courses/12730/assignments/40191">Assignment 3 in canva</a><u>​ </u><a href="https://canvas.ucsc.edu/courses/12730/assignments/40191">s</a></li>

</ul>

<h1>Visual example of palindrome search with stacks</h1>


