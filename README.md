# MACROCalc
A full interpreter of the MACROCalc language in C++

This interpreter incorporates scoping, conditional statements, loops, and enhanced mathematical operations, allowing the evaluation and execution of MACROCalc code files. This project was developed in C++ as a group assignment.

Features:
Variable Declarations and Scoping: Supports numeric variable declarations with var and manages variable scopes using { and }.
Math and Logic Operators: Supports + , - , / , * , ** , && , || , < , >= , etc.
Conditionals and Loops: Includes support for if, else, and while statements.
Print Functionality: Outputs both strings and expressions, with formatted output for variable values within braces.
Error Handling: Detects and reports syntax errors, undeclared variables, redeclarations within the same scope, invalid assignments, and illegal operator chaining.

Components:
Lexer (lexer.hpp)
The lexer processes MACROCalc code to tokenize inputs, ignoring whitespace and comments. The tokenized output is used by the parser to build the Abstract Syntax Tree (AST).

Abstract Syntax Tree (AST) (ASTNode.hpp)
The AST represents the hierarchical structure of MACROCalc code. Each ASTNode corresponds to specific syntax elements (e.g., expressions, statements). This structure enables organized code execution and error checking.

Symbol Table (SymbolTable.hpp)
The symbol table tracks variables across multiple scopes, ensuring each variable is accessible only in the relevant scope. It manages the creation, shadowing, and retrieval of variables.

Interpreter (Project2.cpp)
The main interpreter, Project2.cpp, processes the AST to execute the MACROCalc code. It supports parsing statements, evaluating expressions, and handling various control structures.
