
### https://www.youtube.com/watch?v=QXjU9qTsYCc&ab_channel=FrameofEssence

source_file (contains the source_code) -----Compiler----> excecutable_file (machine_code)

The CPU only can processing information if that information is written in binary language. That is the machine code.

_Example of source code:_
'''
int main () {\n\t int x;\n\t x = 3;\n}\n
'''

It's just text!!!

If we send source coe to the compiler we would get the next steps:

1.- Lexical analysis, identify the text inside the code through tokens

2- Sintactic analysis, tokens are organized into hierarchical structure jnown as a parse tree, which is like figuring out what the "grammar" is in this program, the structure.

3.- Then the compiler record context about the program, includir variable and function names.

4.- The final step is to traverse the tree, and figure out some machine coda that would effecively do the same as this particular source code.

__Note__: COmpilers do not go directly from the parse tree to the machine code. There is usually a few intermediate steps that we are going to skip over (intermediate code, optimisation, assembly code, object code, linking, etc).

_Example of assembly code:_
```
pushq   %rbp
movq    $rbsp, %rbp         reserve memory
movl    $3, -4(%rbp)        writte 3 in that memory position
movl    $0, %eax            end of fuction main
popq    %rbp
ret
```

__Note__: The above is an assuption of mine. I am not sure if the commentaries are t true.

If you compile your program in one computer and then you copy it over to another computer and try to run it. It might not work.

If the new computer has a different operating system or has a different processor model, it probably uses a different machine instructions.

So, if you want that your code runs in the another computer you must compile it in that computer too.

