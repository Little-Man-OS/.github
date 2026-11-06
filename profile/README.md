# The Little Man OS
The little man OS, is an operating system designed in the LMC language developed by peter higginson,
the goal is to use this language to develop increasingly difficult code, as it is a very simple language
within our toolchain, we have expanded the LMC language to include new functions which do not exists and are neccesary for development.

## the file setup
each file is setup as a .lmc file, when it comes to compiling, we built a translator that turns lmc into aarch64 asm code,
this is because the lmc asm language does not actually exist, and only exists to teach students assembly early on in their studies.

## The language set,
The language commands are as follows:

Instructions
  HLT            stop
  LDA x          accumulator = x
  STA x          x = accumulator
  ADD x / SUB x  add or subtract x
  BRA label      branch always
  BRZ label      branch if the accumulator is zero
  BRP label      branch if zero or positive
  INP            read a number from the serial console
  OUT [x]        print a number (the accumulator if no operand)
  OTC [x]        print a character or a CHA string
  IMP "file"     include another .lmc file

Operands
  42             slot 42 (an 8 byte cell)
  name           a data label
  #5  #0x10  #'A'   an immediate value (not for STA)

Data (name: TYPE value, or the classic  name TYPE value)
  DAT 8 bytes   INT 4 bytes   CHA 1 byte or "string"   FLO   DUB

The program starts at the label  main:
Comments start with ; or //

## Future plans for toolchain
In the future I am for this toolchain to have:
1. A compiler
2. support for x86_64 CPUs
3. and obviously have the OS working

## Plans for OS
The operating system's kernel will be built using LMC,
i am still determining the worth of building the GUI for the OS in LMC, or whether to move
languages to that such as the C family. but in the end, all code used in the OS, will run
off of the LMC compiled kernel. the current plan is to aim to get it running on a raspberry pi 3B+
as that is what i have to hand (Hence the reason for aarm64 based kernel for now)

## Current timeline
currently the runtime isn't the biggest, as specifications are still being worked on,
if you have any ideas or requests, please let me know via github, or the email on my github

this is the current timeline:
~~Starting the toolchain~~ <br>
building basic data structures <br>
