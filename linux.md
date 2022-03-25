# BASH SHELL SCRIPT

A Unix/Linux Shell is a command line interpreter which interact with kernel on user's behalf.User can directly enter command on the shell or as sequence of commands in a file to interact with system and hardware

Bash shell is the most predominantly used amongst all of them for linux
In older days Unix used to have default shell as sh (Bourne Shell) which is a predecessor to bash Shell (Bourne again Shell)
Other types are ash, tcsh, csh(C-Shell), ksh(Korn Shell)

# 2. SHELL CATEGORIES

- c-shell categories - tcsh, csh
- Bourne shell - sh, bash, ksh, pdsh

# 3. SHELL CONFIGURATION

When a user logs into the system a shell is invoked. The type of shell depends on user's preference in /etc/passwd which is being set by system administrator during the time of user account creation

- A typical entry in /etc/passwd for the user root is given below
  root : x : 0 : 0 : root : / root : /bin / bash
- The explanation of the above line with each field separated by '' : " is as follows.

# 4.SHELL LAYERS RESPECT TO OS

`USER > SHELL & APPLICATION > SYSTEM CALL > KERNAL > HARDWARE`

# 5.KERNAL

Kernel is the heart of any operating system. In case of OS like Ubuntu/CentOS the kernel in linux manages various hardware resources in the system like CPU, Memory,
Disk, Display, Network, I/O without kernal an OS cannot be envisioned.

# 6.DIRECTORY STRUCTURE

- / - Root
- /bin - Contains the system Binaries
- /home - Contains user's Home Directory
- /dev - Device files like block and character devices
- /etc - System Configuration
  -/lib - Shared library and kernel modules
- /lib64 - Contains 64-bit version shared library
- /var - Data that varies over time
- /sbin - Binary utilities for which only root or system Admin has access
  --/mnt - Mount point for a system file
- /temp - Used for storing temporary data and files
- /proc - kernel data structure mounted as a filesystem
- /boot - Contains the initramfs and kernel image
- /sys - Kernel data structure for different hardware and devices like Block Device, Firmware, and ACPI

# COMMANDS

- uname -a = Operating system information
- hostname -i = Ip address of the machine
- fdisk /dev/sda -l = List all Disk
- Control + D = End of Input in Linux
- .bash = Dot are Hidden Files

## 1.LIST FILES & DIRECTORIES

- ls = List Files and folder
- ls -l = List with Details
- ll = Detail information of files and folder
- ls -a = List with Hidden Files
- ls -lt = List using Time of create
- ls -lrt = List using Reverse Time of create
- ls -l -h = List in Readable Memory size
- ls -il = inode that stores information about a file

## Terminal Output :

```
Permissions Directories Group Size Date Directory or file
drwx------ 2 users 4096 Nov 2 19:51 mail/
drwxr-s--- 35 www 32768 Jan 20 22:39 public_html/
-rw------- 1 users 3 Nov 25 02:58 test.txt
```

```
First field are for user then, Groups and Others
d = Delete
r = Read
w = Write
x = Execute
10 = Number of Files and Folders
. and .. are the meta data for Folders
```

## 2.CHANGE DIRECTORY

```
cd /DirectoryName = Change the Directory to Given Directory
cd /home/videos = Change to Relative Path Directory
```

## 3.CREATE AND READ FILES

```
cat abc.txt = Read abc.txt File
cat >abc.txt = Create abc.txt File
cat abc.txt |more =Read Large file with One page Each
```

## 4.DELETE FILES AND FOLDERS

```
rm abc.txt =Delete File
rmdir abc =Delete Empty Folder
rm -fr abc =Delete Recursively and Force
```

## 4.COPY FILES AND FOLDERS

```
cp abc.txt abc_dest.txt = Copy Content abc to abc_dest.txt
cp abc.txt /Home/Amarjit/Desktop/filename.txt = Copy content to specific location
cp -r abc /s/asd = Copy files and folders recursively
cp -rf src_dir dst_dir = Copy files from certain destination to some destination
```

## 5.MOVE OR RENAME FILES AND FOLDERS

```
mv abc Folder = Rename abc to Folder
mv src_dir dest_dir = Move files from certain destination to other
```

## 6.DATE & CALENDER

```
cal
cal 03 1978
date
date -u = UTC
date
```

## 7.CHANGE MODE

```
chmod +r
Read r
Write w
Execute x
```

## 8.PROCESS STATUS

top = [ Task manager ]

## 9.REDIRECTION & PIPELINE

|

## 10.FIND

find / -name abc.txt

## 11.ENVIRONMENT VARIABLES

An environment variable is a variable whose value is set outside the program, typically through functionality built into the operating system or micro service

```
env
env -u Name
unset Name
```

## 12. SSH [ Secure shell ]

```
ssh -p 22 shakil@192.168.240.130 -Y
scp -P22 shakil@192.168.140.130:/home/log.txt
```

13. UTILITY

```
tcpdump -i eth0
Dump traffic on a network
```
