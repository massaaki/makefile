# Masks

APPS = ./apps
BIN= ./bin
INCLUDE= ./include
OBJ = ./obj
SRC= ./src

FLAGS = -Wall -Werror -Wextra

all: mylibs myapps

mylibs: \
	$(OBJ)/float_vector.o \
	$(OBJ)/mytime.o

myapps:
	gcc $(FLAGS) $(APPS)/app.c ./$(OBJ)/*.o -I $(INCLUDE) -o $(BIN)/app
	gcc $(FLAGS) $(APPS)/app_with_mytime.c $(OBJ)/*.o -I $(INCLUDE) -o $(BIN)/app_with_mytime

$(OBJ)/%.o: $(SRC)/%.c $(INCLUDE)/%.h
	gcc -c $< -I $(INCLUDE) -o $@

run:
	./bin/app

clean:
	rm ./bin/* ./obj/*
