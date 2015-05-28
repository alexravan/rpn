#RPN Calculator
Maxwell Bennett & Alexander Ravan

December 8, 2014

Reverse Polish notation (RPN) is a mathematical notation in which every operator follows all of its operands, in contrast to Polish notation, which puts the operator in the prefix position. It is also known as postfix notation and is parenthesis-free as long as operator arities are fixed. [Wikipedia][1]

###Register Useage
* r0: .zero
* r1: non-volatile and return address for check1 and check2
* r2: stack pointer
* r3: non-volatile and 2nd stack pointer for printing stack
* r4: volatile 
* r5: temporary
* r6: temporary
* r7: temporary

 We only use one stack, the first two elements on the stack are pushed my main.
 These are user's r3 and main's return address in r1.
 
 Our print module works by taking a number from the stack and performs 
 arithmetic operations ontop of stack, without changing the actual value of
 the stack (We emulate a 2 stack system by using 2 stack pointers on one stack)

 [1]: http://en.wikipedia.org/wiki/Reverse_Polish_notation "Wikipedia"