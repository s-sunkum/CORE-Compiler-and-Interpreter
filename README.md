# CORE Compiler and Interpreter in Java

This project contains a Java compiler and interpreter for the programming language CORE. The project implements a subset of the CORE language, including features such as formal languages and grammars, recursive descent parsing, data types, expressions, control structures, parameter passing, memory management, and functional programming principles.

## What is CORE?

CORE is a simple programming language designed for educational purposes. It serves as a foundational language to understand essential concepts in programming languages and compilers. The language features basic data types, expressions, control structures, and parameter passing mechanisms. It is an ideal language for learning about language design, parsing techniques, and compiler and interpreter implementation.

# Language
```
<prog> ::= program { <decl-seq> begin { <stmt-seq> } }
         | program { begin { <stmt-seq> } }

<decl-seq> ::= <decl> | <decl><decl-seq> | <func-decl> | <func-decl><decl-seq>

<stmt-seq> ::= <stmt> | <stmt><stmt-seq>

<decl> ::= <decl-int> | <decl-ref>

<decl-int> ::= int <id-list> ;

<decl-ref> ::= ref <id-list> ;

<id-list> ::= id | id , <id-list>

<func-decl> ::= id ( ref <formals> ) { <stmt-seq> }

<formals> ::= id | id , <formals>

<stmt> ::= <assign> | <if> | <loop> | <out> | <decl> | <func-call>

<func-call> ::= begin id ( <formals> ) ;

<assign> ::= id = <expr> ;
           | id = new instance;
           | id = share id ;

<out> ::= output ( <expr> ) ;

<if> ::= if <cond> then { <stmt-seq> }
       | if <cond> then { <stmt-seq> } else { <stmt-seq> }

<loop> ::= while <cond> { <stmt-seq> }

<cond> ::= <cmpr>
         | ! ( <cond> )
         | <cmpr> or <cond>

<cmpr> ::= <expr> == <expr>
         | <expr> < <expr>
         | <expr> <= <expr>

<expr> ::= <term>
         | <term> + <expr>
         | <term> - <expr>

<term> ::= <factor>
         | <factor> * <term>

<factor> ::= id
           | const
           | ( <expr> )
           | input ( )

```

## Features

The CORE compiler and interpreter in Java provide the following features:

- **Formal Languages and Grammars:** The project leverages formal language theory and grammars to parse and interpret CORE programs.

- **Recursive Descent Parsing:** The project uses a recursive descent parsing technique to analyze the structure of CORE programs and generate an abstract syntax tree (AST).

- **Data Types and Expressions:** The compiler and interpreter support basic data types, including integers, booleans, and strings. They handle expressions involving arithmetic, logical operations, and string manipulation.

- **Control Structures:** The compiler and interpreter implement control structures such as conditionals (if-else statements) and loops (while and for statements) to control the flow of program execution.

- **Parameter Passing:** The compiler and interpreter handle function calls and parameter passing mechanisms, allowing users to define and invoke functions within CORE programs.

- **Memory Management:** The compiler and interpreter manage memory allocation and deallocation, ensuring efficient usage of system resources during program execution.

- **Functional Programming Principles:** The project incorporates functional programming principles, such as higher-order functions and lambda expressions, to enable users to write concise and expressive code.

## Getting Started

To use the CORE compiler and interpreter, follow these steps:

1. Clone the repository: `git clone https://github.com/s-sunkum/CORE-Compiler-and-Interpreter-java.git`
2. Compile the Java source files: `javac *.java`
