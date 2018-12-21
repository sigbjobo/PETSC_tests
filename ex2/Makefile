PETSC_DIR=/global/apps/PETSc/3.4.4
FC                 = mpif90  -O2

ALL: test
Makefile	= Makefile
CFLAGS = -I${PETSC_DIR}/include
FFLAGS = -I${PETSC_DIR}/include/finclude 
SOURCESC = 
SOURCESF = main.F
OBJ = $(SOURCESF:.F=.o)
CLEANFILES = ${OBJ} test
include ${PETSC_DIR}/conf/variables
include ${PETSC_DIR}/conf/rules
test: 	${OBJ} $(Makefile)
	$(FC) $(FFLAGS) $(OBJ) -o test ${PETSC_SYS_LIB}