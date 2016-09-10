# `lt3wstack`

The weighted stack is just a stack that associates nodes with weights
(or priorities, depending on how you look at it).  When a node is
pushed onto the stack, it will pop all those nodes with a weight
greater than or equal to its own.

    \wstack_new:N         create new weighted stack
    \wstack_show:N        output data to terminal (no weights yet)
    \wstack_use:Nn(nn)?   interface to \seq_use:Nn(nn)?
    \wstack_g?push:Nnn    (globally)? push #3 to #1 with weight=#2
    \wstack_g?pop_to:Nn   (globally)? pop #1 down past weight #2
    \wstack_g?clear:N     (globally)? clear content of stack

## TODO

- Use docTeX
- `\wstack_show:N` should call the object a 'weighted stack', not a
  'sequence'.
- `\wstack_show:N` should have nicer output; something more along the
  lines of

        l.16 \wstack_show:N \l_tmp_wstack
        The weighted stack \l_tmp_wstack contains the following {items} at (weights):
        > (4) {four}
        > (2) {two}
        > (1) {one}
        <recently read> }
