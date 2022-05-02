# Simplistic Makefile for malloc_count example

CC = mpicc
CXX = mpic++
CFLAGS = -g -W -Wall -ansi -I..
CXXFLAGS = -g -W -Wall -ansi -I..
LDFLAGS =
LIBS = -ldl
OBJS = test.o ../malloc_count.o

all: test

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $<

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c -o $@ $<

test: $(OBJS)
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o $@ $(OBJS) $(LIBS)

clean:
	rm -f *.o test
