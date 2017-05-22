# compro

## Name
compro - An Assistant Tool for Competitive Programming

## Requirements
- OS X (any versions)
- Bash 4.0 or higher
### How to check
```sh
$ bash --version
```
### How to upgrade (OS X)
Install bash via [Homebrew](https://brew.sh/)
```sh
$ brew install bash
```
and update compro line 1 as below.
```diff
-#!/bin/bash
+#!/usr/local/bin/bash
```

## Usage
Type
```sh
$ cd workspace_directory # Your workspace
$ compro --init
```
so that initialize the directory for working.

After initialization, type

```sh
$ compro
```
then following instructions and prompt appear.
```
============================================================
   compro - An Assistant Tool for Competitive Programming
============================================================
Type `help` to list commands
Type `exit` to finish

Contest > Task $ 
```

## Features
### Manage your contest
You can manage contest and tasks(problems).
```
Contest > Task $ contest ICPC2017
ICPC2017 > Task $ task A
ICPC2017 > A $ ls
A.c
ICPC2017 > A $ edit # editor declared in $EDITOR is called.
ICPC2017 > A $ task B
ICPC2017 > B ls
A.c B.c
```

### Using template file
Before initialization `compro --init`, you may create a template file in the same directory.
If you decleare template file during initialization, all program files are copied from the template file.

### Easy test and easy submit
Example: test input for problem A is "1 2".
Copy "1 2" to your clipboard.
```
ICPC2017 > A $ input
Saving input from clip board...
1 2
Input saved!
```
This will be kept as input of A.
If you change the task, input of B is called (if you have ever saved it).

To compile and run with your input, type
```
ICPC2017 > A $ run
```

If you have no troubles,
```
ICPC2017 > A $ submit
Program copied!
```

Then all you have to do is pasting your program to the submit page.

## Available Language
- C

## LICENSE
MIT
