# Specify the compiler
CC = g++

CCOPTS = -g -Wall
LIBS = -lpthread

# Make the source
all:	router ping-client

common.o : common.h common.cpp 
	$(CC) $(CCOPTS) -c common.cpp
 
router:  router.cpp common.o  
	$(CC) $(CCOPTS) common.o router.cpp -o router $(LIBS) 

ping-client: ping-client.cpp common.o
	$(CC) $(CCOPTS) common.o ping-client.cpp -o ping-client $(LIBS) 

clean :
	rm -f common.o router ping-client
