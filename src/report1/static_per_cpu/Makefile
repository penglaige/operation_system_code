obj-m += static_per_cpu.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

test:
	sudo dmesg -C
	sudo insmod static_per_cpu.ko
	#sudo rmmod static_per_cpu.ko
	dmesg

