# C++ Context-Free Grammar Parser

This C++ program reads and parses a context-free grammar. 

Then, based on the request, it will output one of:

1. All of the terminals followed all of the non-terminals of the grammar (in the order in which they appeared when the grammar was read)
2. The grammar with all of the useless rules removed
3. The FIRST sets of the grammar
4. The FOLLOW sets of the grammar
5. A "YES" or "NO" telling you whether or not the grammar has a predictive parser.

Clone this repository if you want to test out the program.

This C++ program has been compiled into an executable `parser.exe` (Use `parser_w.exe` if on Windows).

To use the program, you will pass in a number in [1 - 5] as a command line argument to the executable telling the program which task to run.

```bash
./parser.exe 1
```
(Use `parser_w.exe` if on Windows)

The program will wait for the grammar from standard input.

The program expects an input Grammar in this format:

Each rule is expected to be inputted like this: a left-hand-side non-terminal, followed by an arrow, followed by zero or more space-separated right-hand-side symbols, followed by a star (*).

leftHandSideSymbol -> rightHandSideSymbol(s) *

If you input zero right hand side symbols, the program will take that as meaning the leftHandSideSymbol generates epsilon (the empty string "").

The star character (*) signals the end of the rule's definition.

After you have specifed all rules, use a hash '#' to signal the end of the grammar. 

An example input looks like this:
```
decl -> idList colon ID *
idList -> ID idList1 *
idList1 -> *
idList1 -> COMMA ID idList1 *
#
```
In this example, `idList1` can generate the empty string or `COMMA ID idList1`.

After you have inputted your grammar, press `Ctrl`+`D` to signal end of input (Press `Ctrl`+`Z` followed by `Enter` if on Windows).

The program will then output the requested information about the grammar.

You can either choose to input your own grammar like this or test the program using the automated test script `test.sh` (Use `test_w.sh` if on Windows) by doing:
```bash
./test.sh n
```
where **n** is the task number to test.

I cannot make the source code of this program available to the public.