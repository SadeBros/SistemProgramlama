CC=gcc
LINK=gcc
CFLAGS=-c -Wall -I.
OBJECT_FILES= homeServer.o gpioDIO.o Keypad.o

.SUFFIXES: .c .o

.c .o:
	$(CC) $^ -o $@ $<

# -lm for Math.h library.
appHomeServer: $(OBJECT_FILES)
	$(LINK) $(OBJECT_FILES) -o $@ -lpthread -lm 

Keypad.o : Keypad.c Keypad.h gpioDIO.h
gpioDIO.o: gpioDIO.c gpioDIO.h gpioTypes.h
homeServer.o: homeServer.c gpioDIO.h Keypad.h Configuration.h
