Name: Shravun Sunkum
File List: 
README.txt - File containing information of project
Main.java - Executable file able to be run
Scanner.java - Parses input file into understandable tokens (Used Professor Carpenter's given Scanner)
Parser.java - Helper class for storing key information throughout the project
Prog.java - Starts program with initial parsing
DeclSeq.java - Parse, print, semantic checks, and execution for decl-seq grammar
StmtSeq.java - Parse, print, semantic checks, and execution for stmt-seq grammar
Decl.java - Parse, print, semantic checks, and execution for decl grammar
DeclInt.java - Parse, print, semantic checks, and execution for decl-int grammar
DeclRef.java - Parse, print, semantic checks, and execution for decl-ref grammar
IdList.java - Parse, print, semantic checks, and execution for id-list grammar
Stmt.java - Parse, print, semantic checks, and execution for stmt grammar
FuncDecl.java - Parse, print, semantic checks, and execution for stmt grammar
Formals.java - Parse, print, semantic checks, and execution for stmt grammar
FuncCall.java - Parse, print, semantic checks, and execution for stmt grammar
Assign.java - Parse, print, semantic checks, and execution for assign grammar
Out.java - Parse, print, semantic checks, and execution for out grammar
IfStmt.java - Parse, print, semantic checks, and execution for if grammar
Loop.java - Parse, print, semantic checks, and execution for loop grammar
Conditional.java - Parse, print, semantic checks, and execution for cond grammar
Compare.java - Parse, print, semantic checks, and execution for cmpr grammar
Expr.java - Parse, print, semantic checks, and execution for expr grammar
Term.java - Parse, print, semantic checks, and execution for term grammar
Factor.java - Parse, print, semantic checks, and execution for factor grammar
Executor.java - Helper class for storing key variable data throughout the project 
Special Features/Comments: 
    - Stack of hashmaps for storing variable data
    - Heap for accessing data for reference variables
    - Executor helper class for storing key information
    - HashMap for storing functions 

Design:
    - The overall design of the executor uses a hashmap for global variables
    - A stack of hashmaps for local variables 
    - This stack is also put into another stack to represent a frame
    - Frames are used for function calls
    - An array list to resemble a heap for reference variables 
    - A hashmap for storing function names with the function body


Testing:
    - A bug that I encountered was that I wrote increment++ inside a function call
    when I really meant to do ++increment. This led to having the reference counter 
    not work properly and took some debugging to find. 
    - The way I tested this was by setting up breakpoints throughout my code and walking
    through different test files. 