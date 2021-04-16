THIRD FORTH
===========

THIRD is a little FORTH-like system that I have used in several situations
to bring up hardware. It *does* *not* adhere to any FORTH standard; its
vocabulary is its own and is unlike any other FORTH system of which I am
aware. I was a FORTH newbie when I designed THIRD, and it shows. FORTH is
still not my primary programming language; all of my serious work is done
in C, FORTRAN, or assembler.

The internals of THIRD are extremely odd. They are also extremely
inefficient. The intent of the system is to be extremely portable, *not*
to be your primary programming language. It is intended to be a primary
debugging tool to generate test loops in the initial debug stages of new
hardware project. Once the system is running well enough to support *any*
*other* programming environment, THIRD is ditched and development moves on
to the target language intended for the system.

THIRD is itself written in two other languages: QDL and StupidCode. QDL is
a FORTH-like language to handle the high-level definitions. StupidCode is a
simple stack-based assembly language to describe the portions of THIRD that
would be written in assembly language if this were a *normal* system.

Porting THIRD to a new processor involves writing a new backend for the
compiler to convert the StupidCode primitives into the appropriate assembly
language and providing the system-specific I/O and initialization code.

The high-level bits of THIRD have been executed on processors ranging from
32 to 8 bits with both endianisms. StupidCode is newer; although I have
several StupidCode compilers, the only ones to generate code that has
actually been executed are the Z80 and PDP-8 versions.

 - Roger Ivie

Codacy Badge
