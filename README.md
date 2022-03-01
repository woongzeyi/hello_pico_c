# hello_pico_c

LED Blinking program for Raspberry Pi Pico self-made in C with pico-sdk

## Howto clone

```
$ git clone https://github.com/woongzeyi/hello_pico_c.git
$ cd hello_pico_c
$ git submodule update --init
$ cd pico-sdk
$ git submodule update --init
cd ../..
```

## Howto build 

```
$ sudo apt update
$ sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential 
$ cd hello_pico_c
$ mkdir build
$ cd build
$ cmake ..
$ make -j4
$ cd ../..
```

## Howto load & run

Make sure your Pico is connected in BOOTSEL mode (holding down BOOTSEL button while connecting)

```
mkdir -p /mnt/pico
sudo mount /dev/sda1 /mnt/pico
cd hello_pico_c/build
sudo cp hello_pico_c.uf2 /mnt/pico
sudo sync
sudo umount /mnt/pico
cd ../..
```
