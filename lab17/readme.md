For this lab, we will use Ruby to write a compiler and a VM for a subset of the Scheme language.

The only functions that we will support will be `println`, `+`, `-`, and `*`.  The only **supported values are integers**.

You may assume that a list will never span multiple lines, so that a program like:

```
  (+ 3
     (* 2 4))
```

would be invalid, but this is acceptable:

```
  (+ 3 (* 2 4))
```

Our compiler will create bytecode files.  In our case, they will be _text files_ for the sake of readability, though a real-world implementation would use a more machine-efficient format.

The bytecode format for our virtual machine (VM) supports the following operations:

`PUSH` -- takes one argument and adds it to the stack.
`PRINT` -- pops the top element of the stack and prints it out.
`ADD` -- pops the top two elements of the stack, ands them together, and then places the result on the stack.
`SUB` -- performs subtraction, following the same pattern as used for ADD.
`MUL` -- performs multiplication, following the same pattern as used for ADD.

Download `compiler.rb` and `vm.rb` from the course website, along with the two sample Scheme programs.  You can compile and run `print.scm` now.  Add support for the additional expressions in both the compiler and the VM.
