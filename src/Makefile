# Uncomment this on Solaris.
#LIBS = -lsocket -lnsl

CFLAGS?= -O2

OBJS = cache.o rfc1035.o util.o option.o forward.o isc.o \
       network.o dnsmasq.o dhcp.o lease.o rfc2131.o 

.c.o: dnsmasq.h config.h 
	$(CC) $(CFLAGS) $(RPM_OPT_FLAGS) -Wall -W -c $*.c 

dnsmasq : $(OBJS) dnsmasq.h config.h
	$(CC) -o $@  $(OBJS) $(LIBS)



