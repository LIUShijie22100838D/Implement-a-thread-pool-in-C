gcc thrd_pool.c -c -fPIC
gcc -shared thrd_pool.o -o libthrd_pool.so -I./ -L./ -lpthread
g++ -Wl,-rpath=./ thrdpool_test.cc -o thrdpool_test -I./ -L./ -lthrd_pool -lpthread
