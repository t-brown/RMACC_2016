#
# Makefile for MPI exercises
#

CC      = mpicc
FC      = mpifc
CFLAGS  = -O0 -g #-traceback -w3
FCFLAGS = -O0 -g #-traceback

EXES = hello      \
       ring       \
       iring      \
       rring

all: $(EXES)

.PHONY:    all clean
.SUFFIXES:
.SUFFIXES: .c .f90 .o .mod

%:: %.f90
	$(FC) -o $@ $(FCFLAGS) $<

%.o: %.f90
	$(H5FC) -c -o $@ $(FCFLAGS) $<

clean:
	-$(RM) $(EXES) *.o *.mod
