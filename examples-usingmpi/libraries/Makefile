all: all-redirect

CC = mpicc

SEQ_SOURCES = seq.c seqex.c seqdef.h
LA_SOURCES  = LA_dis_1.h LA_dis_2.h LA_dmatrix_1.h LA_dvector_1.h \
	LAX_dvector_ddot_stride.c LAX_dvector_ddot_stride2.c \
	LA_library_1.c LA_library_1a.c
SOURCES = $(SEQ_SOURCES) $(LA_SOURCES)

all-redirect: seqex

.SUFFIXES:
.SUFFIXES: .o .c

seqex: $(SEQ_SOURCES)
	$(CC) -o seqex seqex.c seq.c

clean:
	-rm -f *.o *~

.PHONY: all-redirect sources clean
sources:
	@echo ${SOURCES}
