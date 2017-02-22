#Archivo Makefile Simple

PROYECTO= muestreo
DESTDIR= /usr/local/bin
CFLAGS= -Wall
LDFLAGS= -lm
CC= gcc
OBJETO= archivos.o muestreo.o procesamiento.o


all: $(PROYECTO)

%.o: %.c
	$(CC) -c $< $(CFLAGS)

$(PROYECTO): $(OBJETO)
	$(CC) $^ -o $@ $(LDFLAGS)

.PHONY: clean

install: all
	if[! -d /usr/local/bin]; then \
		sudo mkdir /usr/local/bin; \
	fi; \
	sudo cp muestero /usr/local/bin

unistall: 
	rm /usr/local/bin/$(PROYECTO)

clean: 
	rm -f *.o $(PROYECTO)
