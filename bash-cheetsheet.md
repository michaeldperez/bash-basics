# <div align="center">Bash Cheatsheet</div>

## Interpreter Directives

`#!/bin/bash [-opts]`

`#!/usr/bin/env bash`

## Make bash file executable
`chmod u+x` *filename.sh*

## Argument Variables

`\$1`...`\$n`: positional arguments

`$*`: all arguments

`$#`: number of arguments

`$?`: exit status of last command

`${#variable}`: length of string variable


## Executing commands
`$(...)`

## Variables

### Variable definition
`variablename=variablevalue` (no spaces; use lowercase)

### Variable calling
`$variablename` or `"$variablename"`

## Reading Input
`read [-opts] variable_to_save_input`

If no variable is supplied, input is saved in `$REPLY`

Common ptions:

- `-n` or `-N`: number of characters to read.
- `-s`: suppress output (i.e. for passwords).
- `-r`: read *raw* input (i.e. ignore escape sequences).
- `-p prompt`: print the prompt string (w/o newline).

## Conditional Expression
`[[ expression ]]`

Examples:
- `[[ $str ]]`: tests whether `$str` is non-empty.
- `[[ $str = "x" ]]`: tests whether `$str` is equal to `x`.
- `[[ -e $filename ]]`: tests whether `$filename` exists.
- `[[ -d $directory ]]`: tests whether `$directory` exists.

### Arithmetic Tests
`[[ arg1 operator arg2 ]]`
#### Operators:
- `-eq`: equal.
- `-ne`: not equal.
- `-lt`: less than.
- `-le`: less than or equal.
- `-gt`: greater than.
- `-ge`: greater than or equal.

**Note**: the usual operators `>`, `<`, `=`, etc. only work with string variables.