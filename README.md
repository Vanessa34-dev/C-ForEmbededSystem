# C++ ForEmbededSystem
Note: on embedded programming requires two systems:
                        A build system: The system we use to write the code
                        A target system: The system our code is going to be run on

on this exercice, we use :ubuntu on docker - build system
                            raspberry pi on qemu - target system

1- set up environment :
download and run ubuntu on docker (docker run -ti -v $HOME/test:/mnt ubuntu:bionic),
download and install qemu (https:/​/​www.​qemu.​org/​download/),
download Raspbian Lite image, Kernel image and Device tree blob,
emulate a Raspberry Pi–like ARM system using QEMU.

2- install cross compilation tools for ARM on the build system 
->apt install -y crossbuild-essential-armel

3- set up a ssh communication between build system and target system

4-copy a compiled file from build system to target system

5- Use gdbserver for remote debugging 
on target system: install first gdb server (apt-get install gdbserver) and run it after (exemple: gdbserver 0.0.0.0:9090 ./hello)
on build system: install gdb-multiarch package(apt install -y gdb-multiarch) and run = gdb-multiarch -q ./hello 
                                                                                 (gdb) target remote 172.17.0.1:1234
                                                                                 (gdb) continue     (( this commande will run our binary on a remote ARM system))
                                                                                 

                  
