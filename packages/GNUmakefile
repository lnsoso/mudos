
SRC=uids.c contrib.c db.c sockets.c develop.c math.c 
OBJ=uids.$(O) contrib.$(O) db.$(O) sockets.$(O) develop.$(O) math.$(O) 

OBJ=$(addprefix $(OBJDIR)/,$(subst .c,.o,$(SRC)))

$(OBJDIR)/%.o: %.c
	$(CC) -I$(OBJDIR) -I.. $(CFLAGS) -o $@ -c $<

all: $(OBJ)
	ar rcu packages.$(A) $(OBJ)
	$(RANLIB) packages.$(A)

clean:
	rm -f *.$(O)
	rm -f packages.$(A)
