TARGET := main
INCLUDES := -I. -Iinclude -I../utils/include
SRCS = ../utils/utils.c ../utils/operate.c kernel.c main.c
CC := gcc
OBJS = $(SRCS:.c=.o)

$(TARGET):$(OBJS)
	$(CC) -o $@ $^
	rm -rf $(SRCS:.c=.o)
%.o:%.c
	$(CC) $(INCLUDES) -o $@ -c $<

install:
	cp $(TARGET) ../

clean:
	rm -rf $(basename $(TARGET)) $(SRCS:.c=.o)