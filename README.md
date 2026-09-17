# WEPP
This is the WEPP model used by NRCS and the WEPP Windows interface. **The last released version of WEPP is in a seperate repository (wepp2012) that should not be changed.** The code is compiled using the Intel FORTRAN compiler and can be built for Windows or Linux. The makefile included will build on Unbuntu 20.04. To build a 64 bit Linux version use the makefile64 file. 

When building the model for use in watershed application copy the files from the subdirectory **watershed-large-arrays** overwriting the default include files. These files define larger array sizes internal to WEPP.

## Building under Linux
Type 'make' in the directory with the source code. The default is to use the Intel compiler (ifx). A 64 bit version can be built using the 'makefile64' file with the 'make' command.

## Building under Windows


## Other Compilers
The gfortran comiler can be used. Uncomment the flags ((FLAGS), compiler(FC) and linker(LINKER) lines in the makefile to use gfortran compiler instead of the Intel compiler:
```
FFLAGS = $(FFLAGS_GNU)
FC = $(FC_GNU)
LINKER = $(LINK_GNU)

#FFLAGS = $(FFLAGS_IFORT)
#FC = $(FC_IF)
#LINKER = $(LINK_IF)

```