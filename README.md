# MACROCalc
A full interpreter for the **MACROCalc** language in C++

This interpreter incorporates scoping, conditional statements, loops, and enhanced mathematical operations, allowing for the evaluation and execution of MACROCalc code files. This project was developed in C++ as a collaborative group assignment.

## Features

- **Variable Declarations and Scoping**  
  Supports numeric variable declarations with `var` and manages variable scopes using `{` and `}`.

- **Math and Logic Operators**  
  Includes support for arithmetic (`+`, `-`, `/`, `*`, `**`), logical (`&&`, `||`), and comparison (`<`, `>=`, etc.) operators.

- **Conditionals and Loops**  
  Implements `if`, `else`, and `while` statements to support conditional and repetitive execution.

- **Print Functionality**  
  Outputs both strings and expressions, with formatted output that replaces variables within braces.

- **Error Handling**  
  Detects and reports syntax errors, undeclared variables, redeclarations within the same scope, invalid assignments, and illegal operator chaining.

## Components

### Lexer (`lexer.hpp`)
The lexer processes MACROCalc code to tokenize inputs, ignoring whitespace and comments. The tokenized output is then used by the parser to build the Abstract Syntax Tree (AST).

### Abstract Syntax Tree (AST) (`ASTNode.hpp`)
The AST represents the hierarchical structure of MACROCalc code. Each `ASTNode` corresponds to specific syntax elements (e.g., expressions, statements). This structure enables organized code execution and error checking.

### Symbol Table (`SymbolTable.hpp`)
The symbol table tracks variables across multiple scopes, ensuring each variable is accessible only within its appropriate scope. It manages variable creation, shadowing, and retrieval.

### Interpreter (`Project2.cpp`)
The main interpreter, `Project2.cpp`, processes the AST to execute the MACROCalc code. It supports parsing statements, evaluating expressions, and handling various control structures.
