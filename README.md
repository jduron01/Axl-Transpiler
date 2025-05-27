[![Compilation Check](https://github.com/jduron01/Axl-Transpiler/actions/workflows/compiler.yml/badge.svg)](https://github.com/jduron01/Axl-Transpiler/actions/workflows/compiler.yml)

# Axl Source-to-Source Compiler
Implementation of a transpiler for my language called Axl. Converts Axl code to C++. Used Flex and Bison for the lexer and parser respectively, and C was used to implement the semantic analysis, abstract syntax tree, and code generation.

## Installing Flex and Bison
* Installing Flex: `sudo apt-get install flex`
* Installing Bison: `sudo apt-get install bison`

## Compiling the Flex, Bison, and Source Files
```bash
flex scanner.l
bison -d parser.y
gcc -o axlc -lfl lex.yy.c parser.tab.c symbol_table.c semantics.c ast.c code_gen.c
```

## Running the Executable to Convert Source Code to C++
```bash
./axlc [file name]
```

## Compiling the C++ File and Running the Program
```bash
g++ -o [name] output.cpp
./[name]
```
