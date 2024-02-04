CPP = g++
CFLAGS = -std=c++17 -Wall -Wextra -pedantic -ggdb
LFLAGS = -lm
EXEC = executable

${EXEC} : out/main.o
	${CPP} -o $@ $^ ${LFLAGS}

out/%.o : src/%.cpp
	${CPP} ${CFLAGS} -o $@ -c $<

run : ${EXEC}
	./${EXEC}

clean :
	rm -rf out/*.o

cleanall :
	rm -rf out/*.o ${EXEC}
