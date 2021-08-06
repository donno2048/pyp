# pyp

A minified [pyp](https://code.google.com/archive/p/pyp/) compatible with python3

You can also install the [python package](https://github.com/donno2048/pyp3)

Pyp is a linux command line text manipulation tool similar to awk or sed, but which uses standard python string and list methods as well as custom functions evolved to generate fast results in an intense production environment.

Because pyp employs it's own internal piping syntax ("|") similar to unix pipes, complex operations can be proceduralized by feeding the output of one python command to the input of the next.

This greatly simplifies the generation and troubleshooting of multistep operations without the use of temporary variables or nested parentheses. The variable "p" represents each line as a string, while "pp" is entire input as python list:

```sh
ls | ./pyp "p[0] | pp.sort()" #gives sorted list of first letters of every line
```

```sh
ls | ./pyp "p.replace('.', ',')" #replaces . with ,
```
