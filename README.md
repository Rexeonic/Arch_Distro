# Arch_Distro
My custom Arch Linux System developmental guide for **x86_64 bit architecture**.

[LFS: Version 13.0-systemd](https://www.linuxfromscratch.org/lfs/)

> "I solemnly swear to mess up my working system just for the sake of learning purposes".
                                                                - Unknown Arch user


## Prepare the Host System

**Requirements**: A *Host System other than* the system on which 
                  linux system is to be developed.

> If you don't have 2 systems, can develop your system *on a virtual machine*.

### Check Host Requirements
There is a *script written to check host system requirements (**available in the repository**)*.

> Run the script **host_sys_req_checker.sh**
> ``` $ chmod +x path/to/host_sys_req_checker.sh ```
> ``` $ path/to/host_sys_req_checker.sh ```

### Connect to Linux System:
1. Boot the installation package|iso.
2. Find out the ip address of your machine.
``` $ ip a ```
3. SSH into the terminal from your host machine.
``` $ ssh hostname@<ip-address> ```
eg. 
    $ ssh root@10.192.245.12

### Additional Steps: (for virtual machine users)
*SSH part is slightly different for vm users (**rest of steps are same**)*

1. Perform **Port Forwarding**
    eg. Guest Port - 3022
        Host Port - 22
2. Now can perform *ssh from host to virtual machine.*
``` $ ssh -p <Guest_Port> hostname@<loop_back_address> ```
eg. 
    $ ssh -p 3022 root@127.0.0.1





