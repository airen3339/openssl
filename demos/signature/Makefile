#
# To run the demos when linked with a shared library (default):
#
#    LD_LIBRARY_PATH=../.. ./EVP_EC_Signature_demo
#    LD_LIBRARY_PATH=../.. ./EVP_DSA_Signature_demo
#    LD_LIBRARY_PATH=../.. ./EVP_ED_Signature_demo
#    LD_LIBRARY_PATH=../.. ./rsa_pss_direct
#    LD_LIBRARY_PATH=../.. ./rsa_pss_hash

CFLAGS = -I../../include -g -Wall
LDFLAGS = -L../..
LDLIBS = -lcrypto

all: EVP_EC_Signature_demo EVP_DSA_Signature_demo EVP_ED_Signature_demo rsa_pss_direct rsa_pss_hash

%.o: %.c
	$(CC) $(CFLAGS) -c $<

EVP_EC_Signature_demo: EVP_EC_Signature_demo.o
EVP_DSA_Signature_demo: EVP_DSA_Signature_demo.o
EVP_ED_Signature_demo: EVP_ED_Signature_demo.o
rsa_pss_direct: rsa_pss_direct.o
rsa_pss_hash: rsa_pss_hash.o

test: ;

clean:
	$(RM) *.o EVP_EC_Signature_demo EVP_DSA_Signature_demo EVP_ED_Signature_demo rsa_pss_direct rsa_pss_hash
