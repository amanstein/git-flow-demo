VERSION=1.1.0-stable
IDIR =../inc
CC=gcc
CFLAGS=-I$(IDIR)

ODIR=obj
LDIR =../lib

LIBS=-lm

_DEPS = 
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))


_OBJ = gitflowdemo.o barfeature.o foofeature.o

OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))


$(ODIR)/%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

gitflowdemo: $(OBJ)
	gcc -o $@-$(VERSION) $^ $(CFLAGS) $(LIBS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(IDIR)/*\~ 
	rm gitflowdemo-$(VERSION)