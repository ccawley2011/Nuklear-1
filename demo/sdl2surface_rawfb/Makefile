CFLAGS= -std=c89 -Wall -Wextra -pedantic -Wno-unused-function -O0 -g -fvisibility=hidden

.PHONY: clean

demo: demo-sdl1 demo-sdl2 demo-sdl2fb

demo-sdl1: main.c sdl2surface_rawfb.h
	$(CC) -o $@ *.c $(CFLAGS) `sdl-config --cflags --libs` -lm

demo-sdl2: main.c sdl2surface_rawfb.h
	$(CC) -o $@ *.c $(CFLAGS) `sdl2-config --cflags --libs` -lm

demo-sdl2fb: main.c sdl2surface_rawfb.h
	$(CC) -o $@ *.c $(CFLAGS) `sdl2-config --cflags --libs` -lm -DSDL2_WINDOW_SURFACE

clean:
	$(RM) demo demo-sdl1 demo-sdl2 demo-sdl2fb
