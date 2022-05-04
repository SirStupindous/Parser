# Default Grammar Parser

This program has a working lexical analyzer, but no parser.

## Your Task

Implement a bottom up parser. The table generated in assignment 1 will be the parse table you use. You can use any language you want, but you will have to provide equivalent functionality of the files provided here. 

## Running the program

You must have a recent version of Python3 installed.

```
python3 main.py [sourcecode]
python3 main.py code.txt
```

## Inputs and outputs  

For Assignment 1: assignment1.png  

![grab-landing-page](https://github.com/CSUF-CPSC-Caron-SP22/parsing-project-ne/blob/master/assignment1.PNG)
  
For Assignment 2: output.txt  

To see output: ```python3 main.py code.txt >> output.txt```   
```(State, Symbol)
[('a', 'id'), ('=', '='), ('b', 'id'), ('+', '+'), ('c', 'id'), ('+', '+'), ('d', 'id'), ('$', '$')]

Stack:  [0]
Input:  ['$']
Shift State  3

Stack:  [0, 3]
Input:  ['$', ('a', 'id')]
Reduce Using Production Number:  4
Production Step: E -> id
Next State 2

Stack:  [0, 2]
Input:  ['$', 'E']
Shift State  5

Stack:  [0, 2, 5]
Input:  ['$', 'E', ('=', '=')]
Shift State  8

Stack:  [0, 2, 5, 8]
Input:  ['$', 'E', ('=', '='), ('b', 'id')]
Reduce Using Production Number:  4
Production Step: E -> id
Next State 7

Stack:  [0, 2, 5, 7]
Input:  ['$', 'E', ('=', '='), 'E']
Shift State  9

Stack:  [0, 2, 5, 7, 9]
Input:  ['$', 'E', ('=', '='), 'E', ('+', '+')]
Shift State  10

Stack:  [0, 2, 5, 7, 9, 10]
Input:  ['$', 'E', ('=', '='), 'E', ('+', '+'), ('c', 'id')]
Reduce Using Production Number:  3
Production Step: E -> E + id
Next State 7

Stack:  [0, 2, 5, 7]
Input:  ['$', 'E', ('=', '='), 'E']
Shift State  9

Stack:  [0, 2, 5, 7, 9]
Input:  ['$', 'E', ('=', '='), 'E', ('+', '+')]
Shift State  10

Stack:  [0, 2, 5, 7, 9, 10]
Input:  ['$', 'E', ('=', '='), 'E', ('+', '+'), ('d', 'id')]
Reduce Using Production Number:  3
Production Step: E -> E + id
Next State 7

Stack:  [0, 2, 5, 7]
Input:  ['$', 'E', ('=', '='), 'E']
Reduce Using Production Number:  1
Production Step: S -> E = E
Next State 1

Stack:  [0, 1]
Input:  ['S']
Accept
```
