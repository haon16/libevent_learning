target1 = read_fifo
target2 = write_fifo
src = $(wildcard *.c)
obj = $(patsubst %.c, %.o, $(src))

args = -Wall

ALL: $(target1) $(target2)

$(target1):$(target1).o
	gcc $< -levent -o $@ $(args)

$(target2):$(target2).o
	gcc $< -levent -o $@ $(args)

$(obj):%.o:%.c
	gcc -c $< -o $@ $(args)

clean:
	-rm -rf $(obj) $(target1) $(target2)

.PHONY: clean ALL