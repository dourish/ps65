PS65 -- A Pascal System for the 65C02

Pascal p-code compiler for 65C02. This is based on the "Tiny Pascal"
articles published in Byte magazine between September and November
1978. That was also the basis for a Pascal compiler that I built for
the BBC Micro in 1985 (along with other ideas I took from the Dragon
book). BBC Basic made it pretty easy to do this since it handled
recursion well, with parameterized procedures. This is going to be
tricker since I'll write it directly in assembly language.

The first phase is a single-phase compiler that generates code for an
imaginary virtual machine, the p-machine. A second progra then
interprets these p-codes dynamically. A third phase that I didn't
implement before would be to translate p-codes directly into 6502
instructions.

The base language implemented in the articles is fairly restricted. It
has no records, no pointers, no call-by-name parameters, and limited
array support. It would be nice if I could use this basic language to
write a compiler, in Pascal, for a more extensive language. In the BBC
Basic version, I added several of these features in directly.



