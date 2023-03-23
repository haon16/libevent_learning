src = $(wildcard *.c)
target = $(patsubst %.c, %, $(src))

args = -Wall

ALL: $(target)

$(target):%:%.c
	gcc $< -levent -o $@ $(args)

clean:
	-rm -rf $(target)

.PHONY: clean ALL