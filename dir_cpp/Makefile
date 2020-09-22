TARGET = hello
PREFIX = /usr/local/bin
SOURCES = main.cpp hello.cpp sum.cpp
OBJECTS = $(SOURCES:.cpp=.o)

CC = g++
CFLAGS = -c -Wall

.PHONY: all clean install uninstall

all: $(SOURCES) $(TARGET)

$(TARGET): $(OBJECTS)
	$(CC) $(OBJECTS) -o $@

.cpp.o:
	$(CC) $(CFLAGS) $< -o $@

clean:
	rm -rf *.o $(TARGET)

install:
	install $(TARGET) $(PREFIX)

uninstall:
	rm $(PREFIX)/$(TARGET)
