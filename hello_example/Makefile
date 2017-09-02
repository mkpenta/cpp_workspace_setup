#To use this make file, navigate to the directory containgin the make file and type "make"
#		

all: hello

hello: hello.o
		g++ -std=c++1y -o hello hello.o

hello.o: hello.cpp
	g++ -c -std=c++1y hello.cpp
	
clean:
	rm *.o hello

#In  a make file we need to specify how to build the program. We do this by creating targets and rules.
# the name to the left of the colon is the target. to the right are the prerequisite to make the target 
# the line follwing the target is the rule. this is tab indented and is the command to compile and make the program. 
# 
# !!--> It must be on TAB indented on level from the target. It cannot be spaces <--!!
# 
# when we specify make without any other information we mean make all. So make looks for the target all and finds it has
# a prerequisite condition, hello. To make all we need to make hello first. 
# 
# Make looks for hello and finds it has a prerequisite, hello.o. To make hello we need to make hello.o first. 
# Make looks for the target hello.o and finds it has a prequisite of hello.cpp (which is ok as long as that file exists) 
# and since this is not another target, it can build hello.o. Now that hello.o has been built,  
# 
# The clean rule can be used to clean up previously built programs. to run the clean rule
# type: make clean
# 
# you can specify any rule when calling make. To build this program you could also type "make hello" 
# one make file can make many programs.

# the hello rule explained:
#   gcc is the compiler
#   -std=c++1y forces the compiler to use the C++14 standard 
#   -o is the output flag. It sets the name for the program output by the compiler.
	
# the hello.o rule explained:
#   gcc is the compiler
#   -std=c++1y forces the compiler to use the C++14 standard 
#   -c creates object files

# the clean rule explained:
#   rm is the remove command
#   hello is the file to remove

##
# Below is another make example that works for multiple files - modeled from  http://mrbook.org/blog/tutorials/make/
##

#all: hello

#hello: main.o factorial.o hello.o
#    g++ main.o factorial.o hello.o -o hello

#main.o: main.c
#    g++ -c main.c

#factorial.o: factorial.c
#    g++ -c factorial.c

#hello.o: hello.c
#    g++ -c hello.c

#clean:
#    rm *.o hello
