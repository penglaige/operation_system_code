obj-m += slab_layer.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

test:
	sudo dmesg -C
	sudo insmod slab_layer.ko
	sudo rmmod slab_layer.ko
	dmesg

