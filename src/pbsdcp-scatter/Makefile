MPICC=mpicc
CFLAGS=

build: pbsdcp-scatter 

pbsdcp-scatter: pbsdcp-scatter.c misc.o  fileattr.o
	$(MPICC) $(CFLAGS) -o pbsdcp-scatter pbsdcp-scatter.c misc.o fileattr.o

misc.o: misc.c fileattr.h fileattr.o
	$(MPICC) $(CFLAGS) -c misc.c

fileattr.o: fileattr.c fileattr.h
	$(MPICC) $(CFLAGS) -c fileattr.c

fileattr.h : 

clean : 
	rm -rf pbsdcp-scatter *.o
