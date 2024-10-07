# Compiler Description
Implementation of a small source-to-source compiler for my language. Only compiles simple features in the language. Compiles from my language to C++.

# Installing Flex and Bison
* Installing Flex: sudo apt-get install flex
* Installing Bison: sudo apt-get install bison

# Compilation Steps
1. flex scanner.l
2. bison -d parser.y
3. gcc -lfl -o compiler lex.yy.c parser.tab.c

# Running the Compiler
./compiler [name].txt

# Running the Example Programs
g++ -o [name] output.cpp\
./[name]
