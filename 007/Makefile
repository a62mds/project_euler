CC=g++ -std=c++11
CCFLAGS=-I.

EXEC=large_prime

SRCS=main.cpp Primes.cpp
DEPS=Primes.h
OBJS=$(SRCS:%.cpp=%.o)

.PHONY: all run clean

all: $(EXEC)

$(EXEC): $(OBJS)
	$(CC) -o $@ $^ $(CCFLAGS)

%.o: %.cpp $(DEPS)
	$(CC) -c -o $@ $< $(CCFLAGS)

run:
	@if [ -x $(EXEC) ]; then ./$(EXEC); \
	else chmod +x $(EXEC) && ./$(EXEC); fi

clean:
	rm -f *.o
