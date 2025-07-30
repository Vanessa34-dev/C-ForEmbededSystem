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
