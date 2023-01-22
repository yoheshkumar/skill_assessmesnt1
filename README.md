### SKILL_ASSESSMENT-1
## Tittle: 
Minimization of Boolean Function using K-Map and Verilog Implementation

## Aim: 
The aim of this assignment is to minimize a given Boolean function using K-Map and simulate the minimized logic diagram using Verilog.

## Introduction: 
Boolean algebra is a mathematical system that uses only two values, 0 and 1, to represent and manipulate logical expressions. Boolean functions are used in digital logic design to represent the behavior of digital circuits. The process of reducing the number of terms and/or the number of literals in a Boolean function is known as minimization. K-Map is one of the most common techniques used for Boolean function minimization. In this assignment, we will minimize a Boolean function using K-Map and then simulate the minimized logic diagram using Verilog.

## Logic diagram:

## Logical expression: F(A,B,C) = A′B + BAC′ + A'B′C′

## Block diagram:

## Truth table/Excitation table:

## Explanation: 
The given Boolean function can be minimized using K-Map. The K-Map for the given function is as follows:

Using the K-Map, we can identify the following minterms: m1 = (1, 2, 5) and m2 = (3, 6, 7). Therefore, the minimized Boolean function is F(A,B,C) = m1 + m2 = A′B + BAC′ + A'B′C′
```
# verilog code
module logic_diagram(A, B, C, F);
    input A, B, C;
    output F;

    not n1(nA, A);
    not n2(nB, B);
    not n3(nC, C);

    and a1(t1, nA, B);
    and a2(t2, B, nC);
    and a3(t3, A, nB, nC);

    or o1(F, t1, t2, t3);

endmodule
```

## RTL diagram:

## Timing diagram:

## Result: The minimized Boolean function is F(A,B,C) = A′B + BAC′ + A'B′C′. The logic diagram for the minimized function has been successfully simulated using Verilog.
