[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=7692818&assignment_repo_type=AssignmentRepo)
# CPSC 323 Parsing Project

This project is made off of a previously built lexical analyzer. It is used to complete the second part of a compiler, parsing. It uses a CLR bottom up parsing technique.  

## Team members and emails

Nicholas Ayson (nick.ayson@csu.fullerton.edu)
Ethan Stupin    (ethstup@csu.fullerton.edu)

## How to compile and execute

In default grammar for assignment 2:  
```python3 main.py code.txt``` 

## Inputs and outputs  

For Assignment 1: assignment1.png  

[grab-landing-page](https://github.com/CSUF-CPSC-Caron-SP22/parsing-project-ne/blob/master/assignment1.PNG)
  
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