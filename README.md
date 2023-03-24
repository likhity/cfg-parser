# C++ Context-Free Grammar Parser

This C++ program reads and parses a context-free grammar. 

Then, based on the request, it will output one of:

1. All of the terminals followed all of the non-terminals of the grammar (in the order in which they appeared when the grammar was read)
2. The grammar with all of the useless rules removed
3. The FIRST sets of the grammar
4. The FOLLOW sets of the grammar
5. A "YES" or "NO" telling you whether or not the grammar has a predictive parser.

To use this program, first run `make`:
```bash
make
```

This will compile the C++ files into an executable `parser.exe`.

To use the program, you will pass in a number in [1 - 5] as a command line argument to the executable telling the program which task to run.

```bash
./parser.exe 1
```

The program will wait for the grammar from standard input.

The grammar should be inputted in this format:

For each rule, you specify it as
leftHandSideSymbol -> rightHandSideSymbol(s) *

The star '*' signals the end of the rule's definition.

After you have specifed all rules, input a hash '#' to signal the end of the grammar. Then, press Ctrl+D to signal end of input.

You can either choose to input your own grammar like this or test the program using the automated test script `test_p3.sh` by doing:
```bash
./test_p3.sh n
```
where **n** is the task number to test.