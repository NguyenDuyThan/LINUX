# CXX compiler option
CXXFLAGS	+=	$(OPTIMIZE)	\
		-std=c++11		\
		-Wall			\
		-Winline		\
		-pipe			\
		-g			\

# Library paths
LDFLAGS	+= -L/usr/local/lib
LDFLAGS	+= -L/usr/include

#Library libs
LDLIBS	+=	-lpthread				\
		-lrt					\
		-lm					\
		-lcrypto				\
		-lcurl					\
		-lssl					\

all:
	gcc -o client client.c $(CXXFLAGS) $(LDFLAGS) $(LDLIBS)

install:
	cp server /usr/local/bin/

flash:
	@sudo LD_LIBRARY_PATH=/usr/local/lib/ ./client 192.168.1.75 443

clean:
