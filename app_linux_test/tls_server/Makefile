# CXX compiler option
CXXFLAGS	+=	$(OPTIMIZE)	\
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
	gcc -o server server.c $(CXXFLAGS) $(LDFLAGS) $(LDLIBS)

install:
	cp server /usr/local/bin/

flash:
	LD_LIBRARY_PATH=/usr/local/lib/ ./server 443

clean:
	rm -rf *.o;rm -rf server
