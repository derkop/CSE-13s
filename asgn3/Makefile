EXECBIN  = sorting

SOURCES  = $(wildcard *.c)
OBJECTS  = $(SOURCES:%.c=%.o)

CC       = clang
CFLAGS   = -Wall -Wpedantic -Werror -Wextra -g

.PHONY: all clean

all: $(EXECBIN)

$(EXECBIN): $(OBJECTS)
	$(CC) -o $@ $^

%.o : %.c
	$(CC) $(CFLAGS) -c $<

clean:
	rm -f $(EXECBIN) $(OBJECTS)

format:
	clang-format -i -style=file *.[ch]
