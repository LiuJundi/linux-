#
# Makefile for the linux romfs filesystem routines.
#
# new version-200906 by xing-ds

obj-$(CONFIG_ROMFS_FS) += romfs.o

romfs-y := storage.o super.o

KDIR := /lib/modules/$(shell uname -r)/build
PWD := $(shell pwd)

all:
	make -C $(KDIR) SUBDIRS=$(PWD) modules

clean:
	rm *.o *.ko *.mod.c Module.symvers Module.markers modules.order -f

