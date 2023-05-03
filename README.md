Download Link: https://assignmentchef.com/product/solved-cs-1027-computer-science-fundamentals-ii-assignment-1
<br>
<h1>Question 1:  60 points</h1>

The goal of this question is to demonstrate UML diagrams, Classes, Objects, Inheritance Polymorphism.

Consider the following requirements:

<ol>

 <li>Interface <strong><em>People</em></strong></li>

</ol>

<h1> Methods o convertGrade()</h1>




<ol>

 <li>Class <strong><em>Student</em></strong> implements <strong><em>People</em></strong></li>

</ol>

The class <strong><em>Student</em></strong> is not abstract (this means you have to override the method <strong>convertGrade</strong>). The <strong>convertGrade()</strong> method is implemented as the following:

If grade is &gt;=90, output is A


If grade is &gt;=80, output is A

If grade is &gt;=70, output is B

If grade is &gt;=60, output is C

If grade &lt;60, output is F

<ul>

 <li>Attributes o <strong>ID</strong> of type integer (int) o <strong>name</strong> of type String o <strong>grade</strong> of type integer</li>

 <li>Methods</li>

</ul>

o Constructor(int, String, int) of 3 parameters to initialize the instance variables o <strong>toString()</strong> that returns the name and ID of person objects:

Example: name is Joe ID is 1000







<ol>

 <li>Class <strong><em>Undergrad </em></strong>inherits from class Student</li>

</ol>

<ul>

 <li>Attributes o <strong>gpa</strong> of type float</li>

 <li>Methods</li>

</ul>

o <strong><em>Constructor (float, int, String, int). </em></strong>The constructor will initialize the gpa and call the

Student’s constructor to initialize the ID, name and grade o <strong>print() </strong>that calls <strong>toString()</strong> method to print the <strong>ID</strong>, <strong>name</strong> of an <strong>Undergrad</strong> object followed by printing the <strong>gpa</strong>

Example: name is Laila ID is 5000 gpa is 3.7




<ol>

 <li>Class <strong><em>Grad</em> </strong>inherits from class <strong>Student</strong></li>

</ol>

<ul>

 <li>Variables o <strong><em>supervisor </em></strong>of type String</li>

 <li>Methods

  <ul>

   <li><strong>Constructor (String, int, String, int) </strong>that has a similar function to Undergrad’s constructor</li>

   <li><strong>convertGrade() </strong>that overrides the <strong>convertGrade()</strong> method based on the following rules:</li>

  </ul></li>

</ul>

If grade is &gt;=80, output is A

If grade is &gt;=70, output is B

If grade &lt;70, output is F

Note:

<ol>

 <li>The visibility of all attributes in the super class is protected</li>

 <li>The visibility of all attributes in the subclasses is private</li>

 <li>The visibility of all methods in all classes is public</li>

 <li>Each private variable must have two public methods; getter and setter</li>

</ol>




<ul>

 <li>Construct the UML class diagram based on the above requirements. If you do not know any tool to construct the class diagram, you can download NClass from</li>

</ul>

<a href="http://nclass.sourceforge.net/downloads.html">http://nclass.sourceforge.net/downloads.html</a><a href="http://nclass.sourceforge.net/downloads.html">.</a> NClass is free and very easy to use. Submit the actual class diagram (image) and not the source code of the diagram. Check the paragraph called “How to use NClass” below for more details. Use NClass to generate java code for you

(you will see 4 files, one for the interface and 3 for the classes)

<ul>

 <li>Write a program in Java to implement the above requirements.

  <ol>

   <li>Complete the implementation of all methods in all files generated from NClass</li>

   <li>Write a new class (new file) called StudentDemo.java that contains the main method. In this class, you need to:

    <ol start="3">

     <li>Create an <strong>Undergrad</strong> object called <strong>u</strong> of <strong>gpa</strong>8, <strong>ID</strong> 100, <strong>name</strong> “ali” and <strong>grade</strong> 95</li>

     <li>Print the details of the object <strong>u</strong> (call the <strong>print</strong> method)</li>

    </ol></li>

  </ol></li>

</ul>

<ul>

 <li>Change the <strong>ID</strong> of <strong>u</strong> to 500 iv. Print again the details of the object <strong>u</strong></li>

</ul>

<ol>

 <li>Call the method (and print the results) <strong>convertGrade()</strong> of <strong>u</strong></li>

 <li>Crate a <strong>Grad</strong> object called <strong>g</strong> of supervisor “mike” <strong>ID</strong> 200, <strong>name</strong> “sami” and <strong>grade</strong> 95 vii. Change the <strong>supervisor</strong> to “tim”</li>

</ol>

<ul>

 <li>Print the string representation of the object <strong>g</strong></li>

</ul>

<ol>

 <li>Call the method (and print the results) <strong>convertGrade()</strong> of <strong>g</strong></li>

 <li>Create a variable <strong>s</strong> of Student type and refers it to Undergrad object <strong>u</strong></li>

</ol>

(demonstrating polymorphism) xi. Call and print the method <strong>convertGrade()</strong> of <strong>s</strong>

<ul>

 <li>Have <strong>s</strong> refer it to <strong>Grad</strong> object <strong>g</strong> (demonstrating polymorphism)</li>

 <li>Call and print the method <strong>convertGrade()</strong> of <strong>s</strong></li>

</ul>




How to use NClass:

<ol>

 <li>Download and install NClass from <a href="http://nclass.sourceforge.net/downloads.html">http://nclass.sourceforge.net/downloads.html</a> b. Run NClass</li>

</ol>

<ol>

 <li>File -&gt; New -&gt; Project</li>

 <li>File -&gt; New -&gt; Java Diagram</li>

 <li>Diagram -&gt; New -&gt; (choose your diagram). You can also choose the shortcuts in the menu bar</li>

 <li>Make sure you use “Generalization” to represent inheritance and “Realization” to represent implementation of an interface</li>

 <li>When you finish the diagram, go to Diagram -&gt; Generate Code -&gt; Choose Java as a language, delete the import list (java.io.* and java.util.*). Also, uncheck the box “Fill methods with ‘Not Implemented’ exceptions</li>

 <li>Press on the Generate button and choose your destination.</li>

 <li>You will notice that 4 files are created.</li>

</ol>

<h1>Question 2 (60 points)</h1>

The goal of this question is to demonstrate infix to postfix conversion using stack. In class, we showed how to evaluate a postfix notation. Please refer to the lectures to learn more about infix and postfix notations.

The algorithm for converting infix to postfix is as follows:

<ol>

 <li>Scan the Infix string from left to right.</li>

 <li>Initialize an empty stack.</li>

 <li>If the scanned character is an operand, add it to the Postfix string. If the scanned character is an operator and if the stack is empty, Push the character to the stack.</li>

 <li>If the scanned character is an operator and the stack is not empty, compare the precedence of the character with the element on top of the stack(topStack). If topStack has higher precedence over the scanned character, Pop the stack, else Push the scanned character to stack. Repeat this step as long as stack is not empty and topStack has precedence over the character.</li>

 <li>If the scanned character is a left brace ‘(‘, Push the character to the stack</li>

 <li>If the scanned character is a right brace

  <ol>

   <li>While the topStack is not left brace AND stack is not empty

    <ol>

     <li>Add the topStack to the Postfix string</li>

     <li>Pop the stack</li>

    </ol></li>

   <li>Pop the stack // when you exit the while loop</li>

  </ol></li>

 <li>Repeat this step until all the characters are scanned.</li>

 <li>After all characters are scanned, you have to add any character that the stack may have to the Postfix string. If the stack is not empty, add topStack to Postfix string and Pop the stack. Repeat this step as long as stack is not empty.</li>

 <li>Return the Postfix string.</li>

</ol>

Write a file called InfixtoPostix.java to implement the above algorithm.

Example:




Let us see how the above algorithm will be implemented using an example.




Infix String: a+b*c-d




Initially the Stack is empty and our Postfix string has no characters. Now, the first character scanned is ‘a’. ‘a’ is added to the Postfix string. The next character scanned is ‘+’. It being an operator, it is pushed to the stack.







Stack:


Postfix String: a




Next character scanned is ‘b’ which will be placed in the Postfix string. Next character is ‘*’ which is an operator. Now, the top element of the stack is ‘+’ which has lower precedence than ‘*’, so ‘*’ will be pushed to the stack.







Stack: +*

Postfix String: ab




The next character is ‘c’ which is placed in the Postfix string. Next character scanned is ‘-‘. The topmost character in the stack is ‘*’ which has a higher precedence than ‘-‘. Thus ‘*’ will be popped out from the stack and added to the Postfix string. Even now the stack is not empty. Now the topmost element of the stack is ‘+’ which has equal priority to ‘-‘. So pop the ‘+’ from the stack and add it to the Postfix string. The ‘-‘ will be pushed to the stack.







Stack: –

Postfix String: abc*





Next character is ‘d’ which is added to Postfix string. Now all characters have been scanned so we must pop the remaining elements from the stack and add it to the Postfix string. At this stage we have only a ‘-‘ in the stack. It is popped out and added to the Postfix string. So, after all characters are scanned, this is how the stack and Postfix string will be:







Stack

Postfix String: abc*+d-




End result:

Infix String : a+b*c-d

Postfix String : abc*+d-

Deliverables:

<ol>

 <li>A zip file of name <strong><em>your uwo user name</em></strong>. This file should contain two folders named question1 and question2 (all lower case). The question1 folder should contain 5 files (People.java, Student.java, Undergrad.java, Grad.java and StudentDemo.java). The question2 folder should contain the file InfixtoPostfix.java</li>

 <li>pdf file. The submission of this file is optional. However, if you feel that you would like to tell the TAs any useful information about your assignment, feel free to write it in this file. This file can be added to the main folder</li>

 <li>Submit the zip file to OWL before the deadline</li>

</ol>