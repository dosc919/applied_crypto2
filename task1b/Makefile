CC=gcc
CFLAGS=-c -Wall
LDFLAGS=
SOURCES=aes.c aes_square.c
OBJECTS=build/$(SOURCES:.c=.o)
EXECUTABLE=build/aes_square

all: run
	$(SOURCES) $(EXECUTABLE)

$(EXECUTABLE): $(OBJECTS)
	$(CC) $(LDFLAGS) $(OBJECTS) -o $@

build/%.o: %.c
	$(CC) $(CFLAGS) -c $<  -o $@

run: $(EXECUTABLE)
	./$(EXECUTABLE)

run4: $(EXECUTABLE)
	./$(EXECUTABLE) 4

run5: $(EXECUTABLE)
	./$(EXECUTABLE) 5

.PHONY: all run

clean:
	rm -rf $(EXECUTABLE) $(OBJECTS)