CC=gcc
CPFLAGS=-Wall 
LDFLAGS= -lcrypto -lpthread -lssl

SRC= bt_lib.c bt_file.c peer.c bencode.c bt_sock.c bt_client.c bt_setup.c 
OBJ=$(SRC:.c=.o)
BIN=bt_client

	
all: $(BIN)

$(BIN): $(OBJ)
	$(CC) $(CPFLAGS)-o $(SLEEP)  $(BIN) $(OBJ) $(LDFLAGS)


%.o:%.c
	$(CC) -c $(CPFLAGS) $(SLEEP) -o $@ $<  

$(SRC):


clean:
	rm -rf $(OBJ) $(BIN)

client:
	mkdir -p ./client$(num)
	cp ./bt_client ./client$(num)/
	cp ./*.torrent ./client$(num)/
	
sleep: SLEEP=-D _SLEEP_
sleep: all	
