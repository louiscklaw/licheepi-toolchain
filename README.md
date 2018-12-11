
docker cp fadcc9ffa5a4:/root/zero_imager ./zero_imager
docker cp fadcc9ffa5a4:/root/linux/arch/arm/boot/zImage .
docker cp fadcc9ffa5a4:/root/u-boot/u-boot-sunxi-with-spl.bin .


sudo dd if=/dev/zero of=/dev/sdb bs=1024 count=128

./write_all.sh /dev/sdb brmin
