boot.bin: boot.asm
	nasm -f bin.asm -o boot.bin

master.img:boot.bin
	bximage -q -hd=16 -func=create -sectsize=512 -imgmode=flat master.img
	dd if boot.bin of=master.img bs=512 count=1 conv=notrunc
