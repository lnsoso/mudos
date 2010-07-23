
SRC=uids.c contrib.c db.c sockets.c develop.c math.c 
OBJ=uids.$(O) contrib.$(O) db.$(O) sockets.$(O) develop.$(O) math.$(O) 

.c.$(O):
	$(CC) $(CFLAGS) -I.. -c $*.c

all: $(OBJ)
	ar rcu packages.$(A) $(OBJ)
	$(RANLIB) packages.$(A)

clean:
	rm -f *.$(O)
	rm -f packages.$(A)
