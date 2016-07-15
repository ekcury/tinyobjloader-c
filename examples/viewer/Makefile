UNAME_S := $(shell uname -s)
ifeq ($(UNAME_S),Darwin)
LD_FLAGS=-framework OpenGL -lglfw3 -lglew
endif
ifeq ($(UNAME_S),Linux)
LD_FLAGS=-lGL -lGLU -lglfw3 -lGLEW -lX11 -lXrandr -lXinerama -lXxf86vm -lXcursor -lm -pthread -ldl
endif

all:
	clang -c trackball.c
	clang -o viewer -g -O2 -pedantic -ansi -Wno-deprecated-declarations viewer.c trackball.o $(LD_FLAGS)