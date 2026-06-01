# Arch_Distro
My custom Arch Linux System developmental guide for **x86_64 bit architecture**.

[LFS: Version 13.0-systemd](https://www.linuxfromscratch.org/lfs/)

> "I solemnly swear to mess up my working system just for the sake of learning purposes".
                                                                - Unknown Arch user


## Prepare the Host System

**Requirements**: A *Host System other than* the developmental system.

> If you don't have 2 systems, can develop your linux system *on a virtual machine*.

### Check Host Requirements
There is a *script written to check host system requirements (**available in the repository**)*.

> Run the script **host_sys_req_checker.sh**<br>
> ``` $ chmod +x path/to/host_sys_req_checker.sh ```<br>
> ``` $ path/to/host_sys_req_checker.sh ```<br>
![alt text](Visual_Guides/checker_script_output.png)

> Install any packages which *isn't **up-to-date** or **downloaded***.

### Connect to Linux System:
1. Boot the installation package|iso.
![alt text](Visual_Guides/ARCH_root_terminal.png)
*after booting, it should look similar*
2. Find out the ip address of your machine.
``` $ ip a ```
3. SSH into the terminal from your host machine.
``` $ ssh hostname@<ip-address> ```<br>
eg. 
    $ ssh root@10.192.245.12

### Additional Steps: (for virtual machine users)
*SSH part is slightly different for vm users (**rest of steps are same**)*

1. Perform **Port Forwarding**<br>
    eg. Guest Port -> 3022<br>
        Host Port -> 22
2. Now can perform *ssh from host to virtual machine.*
``` $ ssh -p <Guest_Port> hostname@<loop_back_address> ```<br>
eg. 
    $ ssh -p 3022 root@127.0.0.1


## Partition


