# The Little Man OS<br>
The little man OS, is an operating system designed in the LMC language developed by peter higginson,<br>
the goal is to use this language to develop increasingly difficult code, as it is a very simple language<br>
within our toolchain, we have expanded the LMC language to include new functions which do not exists and are neccesary for development.<br>
<br>
## the file setup<br>
each file is setup as a .lmc file, when it comes to compiling, we built a translator that turns lmc into aarch64 asm code,<br>
this is because the lmc asm language does not actually exist, and only exists to teach students assembly early on in their studies.<br>
<br>
## The language set,<br>
The language commands are as follows:<br>
<br>
Instructions<br>
  HLT            stop<br>
  LDA x          accumulator = x<br>
  STA x          x = accumulator<br>
  ADD x / SUB x  add or subtract x<br>
  BRA label      branch always<br>
  BRZ label      branch if the accumulator is zero<br>
  BRP label      branch if zero or positive<br>
  INP            read a number from the serial console<br>
  OUT [x]        print a number (the accumulator if no operand)<br>
  OTC [x]        print a character or a CHA string<br>
  IMP "file"     include another .lmc file<br>
<br>
Operands<br>
  42             slot 42 (an 8 byte cell)<br>
  name           a data label<br>
  #5  #0x10  #'A'   an immediate value (not for STA)<br>
<br>
Data (name: TYPE value, or the classic  name TYPE value)<br>
  DAT 8 bytes   INT 4 bytes   CHA 1 byte or "string"   FLO   DUB<br>

The program starts at the label  main:<br>
Comments start with ; or //<br>

## Future plans for toolchain<br>
In the future I am for this toolchain to have:<br>
1. A compiler<br>
2. support for x86_64 CPUs<br>
3. and obviously have the OS working<br>
<br>
## Plans for OS<br>
The operating system's kernel will be built using LMC,<br>
i am still determining the worth of building the GUI for the OS in LMC, or whether to move<br>
languages to that such as the C family. but in the end, all code used in the OS, will run<br>
off of the LMC compiled kernel. the current plan is to aim to get it running on a raspberry pi 3B+<br>
as that is what i have to hand (Hence the reason for aarm64 based kernel for now)<br>
<br>
## Current timeline<br>
currently the runtime isn't the biggest, as specifications are still being worked on,<br>
if you have any ideas or requests, please let me know via github, or the email on my github<br>

this is the current timeline:<br>
~~Starting the toolchain~~ <br>
building basic data structures <br>
