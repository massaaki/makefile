```
gcc -c ./src/float_vector.c -I ./include -o ./obj/float_vector.o
gcc -c ./src/mytime.c -I ./include -o ./obj/mytime.o
gcc apps/app.c ./obj/float_vector.o  -I include -o bin/app

If you should want to compile with another
gcc -c ./src/mytime.c -I ./include -o ./obj/mytime.o
gcc apps/app_with_mytime.c ./obj/float_vector.o ./obj/mytime.o -I include  -o bin/app_with_time

gcc apps/app_with_mytime.c ./obj/*.o -I include  -o bin/app_with_timer

```
