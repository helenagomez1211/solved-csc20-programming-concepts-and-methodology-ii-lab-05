Download Link: https://assignmentchef.com/product/solved-csc20-programming-concepts-and-methodology-ii-lab-05
<br>
<strong> </strong><strong>Objective: </strong>

The objective of this lab is to get you some experience in using stacks, queues, class packages and UML.

The programming assignment:

In this lab, you are to write an infix evaluator. Given an input string of characters like

“12+34*(56-7)-18/9”, first print the postfix equivalent “12 34 56 7 – * + 18 9 / -” and then print the value of the expression.

Notes: In this lab,

<ol>

 <li>You must use the algorithms given in class to convert infix expressions to postfix expressions and to evaluate postfix expressions.</li>

 <li>You must use the instructor’s stack and queue package.</li>

 <li>You must use the instructor’s frame work depicted by the following class diagrams.</li>

 <li>Copy directory lab05 from ~wang/sample20.</li>

 <li>Complete methods infixToPostfix and evaluatePostfix.</li>

</ol>







Some programming Hints:




<ol>

 <li>To create a stack:</li>

</ol>




Stack theStack = new Stack();







<ol start="2">

 <li>To push ‘#’ into the stack:</li>

</ol>




theStack.push(new Operator(‘#’));







<ol start="3">

 <li>To create a Tokenizer from a string s:</li>

</ol>




Tokenizer T = new Tokenizer(s);







<ol start="4">

 <li>Repeat until no more tokens:</li>

</ol>




While (T.moreTokens()) { …..}







<ol start="5">

 <li>To get the next token:</li>

</ol>




Token Tkn = T.nextToken();







<ol start="6">

 <li>To pop a token into a variable of the type Token:</li>

</ol>




Token Current = (Token) theStack.pop();







<ol start="7">

 <li>To cast a Token into an Operator:</li>

</ol>




Opr = (Operator)Tkn;







<ol start="8">

 <li>To check if a Token variable Tkn contains an Operand:</li>

</ol>




if (Tkn instanceof Operand)…







<ol start="9">

 <li>To check if an operator is a ‘(‘:</li>

</ol>




if (Opr.operator==’(‘)…




<ol start="10">

 <li>To perform an operation:</li>

</ol>




switch(Opr.operator) { case ‘+’: result = opnd1 + opnd2; break;

…

}







<ol start="11">

 <li>To check the operator on the top of the stack:</li>

</ol>




((Operator)theStack.top()).operator


