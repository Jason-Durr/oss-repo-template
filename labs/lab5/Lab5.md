
# Lab 4


## 1. Steps 1-5

<img src="step1.png">
<img src="Step2.png">
<img src="Step3.png">
<img src="Step4_1.png">
<img src="Step4_2.png">
<img src="Step5.png">

## 2. My Make file

All: program

program: program.o static_block.a dynamic_block.so

        cc program.o build/static_block.a build/dynamic_block.so -o program

program.o: program.c

        cc -c program.c -o program.o

static_block.a: block.o

        ar rcs build/static_block.a build/block.o -o

dynamic_block.so: block.o

        cc -shared -o build/dynamic_block.so build/block.o

block.o: source/block.c

        cc  -c source/block.c -o build/block.o



## 3. My cmake file

