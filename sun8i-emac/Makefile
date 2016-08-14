obj-m += sun8i-emac.o

KVER ?= $(shell uname -r)

all:
	make -C /lib/modules/$(KVER)/build M=$(PWD) modules

clean:
	make -C /lib/modules/$(KVER)/build M=$(PWD) clean

install:
	cp sun8i-emac.ko /lib/modules/$(KVER)/kernel/drivers/net/ethernet/
	depmod
