
EE_BIN  = ps2link.elf
EE_OBJS = ps2link.o cmdHandler.o excepHandler.o exceptions.o cd.o

EE_INCS += -I../include

LOADADDR = 0xc0000
ifeq ($(DEBUG),1)
LOADADDR = 0xd00000
endif
EE_LDFLAGS += -Wl,-Ttext -Wl,$(LOADADDR)

all: $(EE_BIN)

clean:
	-rm -f $(EE_OBJS) $(EE_BIN)

include $(PS2LIB)/Makefile.pref
include $(PS2LIB)/Makefile.eeglobal