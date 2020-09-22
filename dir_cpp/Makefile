TARGET = hello
SOURCES = main.cpp hello.cpp sum.cpp
OBJECTS = $(SOURCES:.cpp=.o)

CC = g++
CFLAGS = -c -Wall

.PHONY: all clean

all: $(SOURCES) $(TARGET)

$(TARGET): $(OBJECTS)
	$(CC) $(OBJECTS) -o $@

.cpp.o:
	$(CC) $(CFLAGS) $< -o $@

clean:
	rm -rf *.o $(TARGET)
