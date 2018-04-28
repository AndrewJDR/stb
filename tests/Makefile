INCLUDES = -I..

CFLAGS = -DSTB_DIVIDE_TEST
CPPFLAGS = -DSTB_DIVIDE_TEST

ifneq ($(OS),Windows_NT)
CFLAGS += -Wno-pointer-to-int-cast -Wno-int-to-pointer-cast
CPPFLAGS += -Wno-write-strings
endif

#CFLAGS += -O -fsanitize=address

all:
	@echo OS OS OS
	@echo $(OS)
	$(CC) $(INCLUDES) $(CFLAGS) ../stb_vorbis.c test_c_compilation.c test_c_lexer.c test_dxt.c test_easyfont.c test_image.c test_image_write.c test_perlin.c test_sprintf.c test_truetype.c test_voxel.c -lm
	$(CC) $(INCLUDES) $(CFLAGS) -DIWT_TEST image_write_test.c -lm -o image_write_test
