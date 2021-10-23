### Q. What is a GNU project?
 GNU stands for `GNU's not Unix`. Richard Stallman founde this project in 1978 at MIT.This project was a mass collaborative initiative for the development of free software. At that time there was lack of free OS this was the main purpose of this project to create a free OS. Free doesn't mean free of cost. It means the ability of anyone ho wishes to run,copy,distribute,study,change and improve the software. According to GNU : Linux is the kernal.
 
### Q. What is the difference between Unix & Linux?
| Linux  - | Unix |
|  ------------------------- | --------------------------- |
| Linux is open source and is developed by Linux community of developers. |Unix was developed by AT&T Bell labs and is not open source.|
| Linux is free to use. |Unix is licensed OS.|
| Linux is just the kernel.| Unix is a complete package of Operating system.|
| Supported file systems are Ext2, Ext3, Ext4, Jfs, ReiserFS, Xfs, Btrfs, FAT, FAT32, NTFS. | Supported file systems are s, gpfs, hfs, hfs+, ufs, xfs, zfs.|
| Linux is used in wide varieties from desktop, servers, smartphones to mainframes. | Unix is mostly used on servers, workstations or PCs.|
| Distros are Ubuntu, Debian GNU, Arch Linux, etc.| SunOS, Solaris, SCO UNIX, AIX, HP/UX, ULTRIX etc.|

### Q. What do you mean by Integrity check of BIOS? Mention firmwares other than BIOS.
BIOS stands for `Basic Input Output System`. The first step in the Linux boot process is the BIOS which performs system integrity checks. The BIOS is the first piece of firmware that executes upon computer power-on. The BIOS's main goal is to load and execute the Master Boot Record bootloader. The firmware other than BIOS is UEFI(stands for "Unified extensible firmware interface").
 
### Q. What is a UEFI?
UEFI stands for `Unified Extensible Firmware Interface`. It does the same job as a BIOS, but with one basic difference: it stores all data about initialization and startup in an .efi file, instead of storing it on the firmware. UEFI comes with many improvements from the traditional BIOS firmware. 

### Q. What is the difference between BIOS & UEFI?
* UEFI supports drive sizes upto 9 zettabytes, whereas BIOS only supports 2.2 terabytes.
 * UEFI has discrete driver support, while BIOS has drive support stored in its ROM, so updating BIOS firmware is a bit difficult.
 * UEFI offers security like "Secure Boot", which prevents the computer from booting from unauthorized/unsigned applications. This helps in preventing rootkits, but also hampers dual-booting, as it treats other OS as unsigned applications.
 * UEFI runs in 32bit or 64bit mode, whereas BIOS runs in 16bit mode. So UEFI  is able to provide a GUI (navigation with mouse) as opposed to BIOS which allows navigation only using the keyboard.
 
### Q. When should you go for Ubuntu?
Ubuntu Linux is the most popular open source operating system. There are many reasons to use Ubuntu Linux that make it a worthy Linux distro. 
1. Ubuntu is user-friendly.
2. Ubuntu is free.
3. It’s secure. Say no to anti-virus.
4. Low system requirements.
5. It’s open source.
6. Improved compatibility, included drivers.
7. Free Apps

### Q. List various linux distributions & their usecases.
1. `Debian ` : Bug Tracking, penetration testing, Network scanning
2. `CentOs ` : Rich base for open source communities
3. `Ubuntu ` : For personal computers & servers
4. `Fedora ` : Vast Software availability, Rapid release of softwares, excellent snap support

### Q. What does a systemd.unit(5) means?
The number basically corresponds to the section of the manual page. 
| Number - | Meaning|
|  -------------------------  | ------------------- |
| 1 | General Commands |
| 2 | System Calls |
| 3 | Library functions, covering in particular the C standard library |
| 4 | Special files (usually devices, those found in /dev) and drivers |
| 5 | File formats and conventions |
| 6 | Games and screensavers |
| 7 | Miscellanea |
| 8 | System administration commands and daemons |

### Q. What are getty commands and uname command?
The `getty` command sets and manages terminal lines and ports. The getty command is run by the init command. The getty command is linked to the Terminal State Manager program. The Terminal State Manager program provides combined terminal control and login functions.  The file /usr/sbin/getty contains the getty command. \
                            `getty [ [ -r | -u | -U ] [ -d ] [ -H HeraldString ] [ -M motdFile ] [ -N ] ] PortName` 
                            
 The command ‘uname‘ displays the information about the system. \
Syntax: `uname [OPTION]`
1. `-a option`: It prints all the system information in the following order: Kernel name, network node hostname, kernel release date, kernel version, machine hardware name, hardware platform, operating system.
2. `-s option`: It prints the kernel name.
3. `-n option`: It prints the hostname of the network node(current computer).
4. `-r option`: It prints the kernel release date.
5. `-v option`: It prints the version of the current kernel.
6. `-m option`: It prints the machine hardware name.
7. `-p option`: It prints the type of the processor.
8. `-i option`: It prints the platform of the hardware.
9. `-o option`: It prints the name of the operating system.

### Q. What is squashfs file system?
Squashfs is a compressed read-only file system for Linux. Squashfs compresses files, inodes and directories, and supports block sizes from 4 KiB up to 1 MiB for greater compression. A squashfs file system consists of a maximum of nine parts, packed together on a byte alignment. It uses zlib, lz4, lzo, or xz compression to compress files, inodes and directories. 

### Q. What are /dev/loop and /dev/tty ?
`/dev` is the location of special or device files. It is a very interesting directory that highlights one important aspect of the Linux filesystem - everything is a file or a directory. \
`/dev/tty` stands for the controlling terminal (if any) for the current process (the process that uses "/dev/tty" in a command). To find out which tty's are attached to which processes use the "ps -a" command at the shell prompt (command line).

### Q. What are Linux Signals?
In Linux, Signals are the interrupts that are sent to the program to specify that an important event has occurred. Events can vary from user requests to invalid memory access errors. Various signals, like the interrupt signal, means that the user has asked the program to perform something which is not present in the user flow of control.
There are two kinds of signals:
* `Maskable` : Maskable Signals are the signals that the user can change or ignore, for example, Ctrl +C.
* `Non-Maskable` : Non-Maskable Signals are the signals that the users cannot change or ignore. Non-Maskable signals mainly occur if a user is signaled for non-recoverable hardware errors.

### Q. What is the purpose of creating and using hidden files.
Files that exist on a computer, but don't appear when listing or exploring, are called hidden files. A hidden file is primarily used to help prevent important data from being accidentally deleted. Hidden files are often known as a dot file. And we can also delete that file. \
For listing dot file :     `ls -a | egrep '^\.'` \
For deleting dot file :         `rm -rfv /tmp/demo/.*`

### Q. How ext4fs is faster/better?
Ext4 is functionally very similar to ext3, but brings large filesystem support, improved resistance to fragmentation, higher performance, and improved timestamps. Ext4 is also said to be slightly faster in sequential reads and writes.When it comes to file checking, EXT4 is quicker because unallocated blocks of data are marked as such and are simply skipped during disk check operations.

### Q. What is swap & swap memory?
`Swap space` is a space on a hard disk that is a substitute for physical memory.It is also called a swap file. This interchange of data between virtual memory and real memory is called swapping and space on disk as “swap space”. \
`Swap memory` is the dedicated amount of hard drive that is used whenever RAM runs out of memory. There is a memory management program in Linux that takes care of this process. Whenever RAM is short of memory, the memory management program looks for all those inactive blocks of data present in RAM that have not been used for a long time.
 
### Q. How to mount a file system?
To mount a file system in a given location (mount point), use the mount command in the following form: \
`mount [OPTION...] DEVICE_NAME DIRECTORY` \
For example, to mount the /dev/sdb1 file system to the /mnt/media directory we will use: \
`sudo mount /dev/sdb1 /mnt/media`

### Q. Mention a ZFS use case.
The `Zettabyte File System `(ZFS) is an advanced file system. Unlike most files systems, ZFS combines the features of a file system and a volume manager. This means that unlike other file systems, ZFS can create a file system that spans across a series of drives or a pool. Not only that but we can add storage to a pool by adding another drive.

### Q. How to check the port number of a process?
 By using netstat Command : \
 `$ sudo apt install net-tools` \
 `$ sudo netstat -ltnp` where \
l: display only listening sockets \
t: display tcp connection \
n: display addresses in a numerical form \
p: display process ID/ Program name

### Q. What is unix time sharing (UTS)?
Unix is a time sharing OS as its environment provides multiprogramming & multitasking. It allows a large number of users to interact concurrently. It also brought down the cost of computing capabilities.
 
### Q. What are control groups?
Control groups, usually referred to as `cgroups`, are a Linux kernel feature. A cgroup is a collection of processes that are bound to a set of limits or parameters defined via the cgroup filesystem. Cgroups allow you to allocate resources such as CPU time, system memory, network bandwidth, or combinations of these resources among user-defined groups of tasks (processes) running on a system. 

### Q. What is the difference between sbin & usr/sbin?
Both are the directories. It contains root binaries which are executable commands to perform particular tasks. Since they are root binaries it requires root privileges to run. \
`/sbin` is a symbolic link to `/usr/bin`.

### Q. Examples of awk, grep and sed.
 The grep stands for ` “global regular expression print,” ` processes text line by line, and prints any lines which match a specified pattern. \
 Syntax: \
 ` $ grep [options] pattern [files]` \
   mytext.txt file:

```this is Sneha
this is Naincy
this is Navnita.
this is Shinni.
this is Nishant.
```
* `grep -c "this" mytext.txt`

```5 ```



* `grep -l "Sneha" *` 
```
text.txt
```



* `grep -w "Naincy" mytext.txt`

```this is Naincy.
this is Naincy.
```



* `grep -o "Sneha" mytext.txt`

```Sneha
Sneha
```
 The `awk` can be used as a field extractor (like cut command), a basic calculator, and as a pattern matcher (like grep command) and It allows the user to use variables, numeric functions, string functions, and logical operators. \
* `awk '/Naincy/ {print}' mytext.txt`
 
```this is Naincy```

* `awk '{print $1,$2}' mytext.txt`
```this is
this is
this is
this is
this is
```

* `awk '{print NR,$0}' mytext.txt`
```1 this is Sneha.
2 this is Naincy.
3 this is Navnita.
4 this is Shinni.
5 this is Nishant.
```
 The sed is a `stream editor`. A stream editor is used to perform basic text transformations on an input stream (a file or input from a pipeline). It can perform lots of operations on file like, searching, find and replace, insertion or deletion. \
* `sed 's/this/ it /' mytext.txt`
``` it  is Sneha.
 it  is Naincy.
 it  is Navnita.
 it  is Shinni.
 it  is Nishant.
```



* `sed 's/is/ it /2' mytext.txt`
```this  is  Sneha
this  is Naincy.
this  it  Navnita.
this  is Shinni.
this  is  Nishant.
```



* `sed 's/is/it/g' mytext.txt`
```thit it Sneha.
thit it Naincy.
thit it Navnita.
thit it Shinni.
thit it Nishant.
```
### Q. How many tables are there in iptables?
Iptable is the built-in linux firewall which includes some conditions, known as rules, according to which the traffic is allowed on the machine. It monitors the incoming and outgoing traffic and filter it according to the specified rules. \
IPTables has the following 5 tables: 
   1. `Filter Table`
   2. `NAT table`
   3. `Mangle table`
   4. `Raw table` 
   5. `Security table` 
   
### Q. What is prot, opt, in, out, source & destination?
  `prot`: Protocols. tcp, udp, icmp, etc., \
  `opt` : Special options for that specific rule. \
  `source`  : Source ip-address of the packet \
  `destination` : Destination ip-address for the packet 
  
### Q. Why rules are added to the top?
Rules are added to top becuase whenever the packets are passed from the first rule it does not check the bottom rules.

### Q. What type of rules we can add to the iptables?
`Accept `- It means that the packet is allowed to pass through the firewall.

`Reject `- It means that the packet is not allowed to pass through the firewall.

`Drop `- It means to skip the current rule and jump back to the chain from which it was called.

### Q. Can we block a website by its domain name only?
 Yes we can block a website by its domain name only by 
  ```
  $ sudo iptables -I INPUT -t filter -s www.facebook.com -j DROP` 
  ```
   
### Q. How can we persist rules in iptables?
1. Add rules to the iptables according to your requirment.

2. Verify that all the rules are present using the command “**iptables -L**“.

3. Add rules to the iptables according to your requirment.

4. Verify that all the rules are present using the command “**iptables -L**“.

5. Save the iptables.

   ```
   # service iptables save
   ```

   6. Restart the service.

   ```
   # service iptables restart
   ```

   7. Making service permanently **ON** using chkconfig.

   ```
   # chkconfig iptables on
   ```
   
 ### Q. How can we save rules in iptables?
  The generic method of saving iptables rules is to use the command iptables-save, which writes to stdout. \
   ` $ iptables-save > /etc/network/iptables.rules`
   
 ### Q.  What is the difference between ufw & iptables.
 | iptables                                               | ufw                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Iptable is the built-in linux firewall which includes some conditions, known as rules, according to which the traffic is allowed on the machine. It monitors the incoming and outgoing traffic and filter it according to the specified rules.| The Uncomplicated Firewall (ufw) is a frontend for iptables.ufw aims to provide an easy to use interface for people unfamiliar with firewall concepts, while at the same time simplifies complicated iptables commands to help an administrator who knows what he or she is doing.|


### Q. What are public & private keys?
| Public keys                                            | Private keys                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| In Private key, the same key (secret key) is used for encryption and decryption. In this key is symmetric because the only key is copy or share by another party to decrypt the cipher text. It is faster than the public key cryptography. | In Public key, two keys are used one key is used for encryption and another key is used for decryption. One key (public key) is used for encrypt the plain text to convert it into cipher text and another key (private key) is used by receiver to decrypt the cipher text to read the message. |
    
    
### Q. How does ssh work?
SSH stands for `Secure Shell`. It is a communication protocol, which helps us in communication with other devices over a network, just like HTTP does. The difference main difference is It is known for sending encrypted data over the network so that it can be prevented from unauthorized access. It runs on port number 22 by default. SSH first ensures the authenticity of the client and then build a pipeline between the SSH client and the server. Data transmitted through this pipeline is encrypted by using the concept of Asymmetric Data Encryption. \
Run the following command on a client machine to initiate an SSH connection: \
`$ ssh [username]@[server_ip_or_hostname]` \
To generate a pair of RSA keys, the command is : \
`$ ssh-keygen `

### Q. What is the difference between HTTP & HTTPS.
| HTTP | HTTPS |
|----------------------------|-------------------------------------|
|HTTP stands for HyperText Transfer Protocol.| HTTPS for HyperText Transfer Protocol Secure.|
|In HTTP, URL begins with “http://”.|In HTTPs, URL starts with “https://”.|
|HTTP uses port number 80 for communication. | HTTPs uses 443 port number for communication.|
|HTTP is considered to be unsecure. | HTTPs is considered as secure.|
|HTTP works at Application Layer.| HTTPS works at Transport Layer.|
|In HTTP, Encryption is absent. | Encryption is present in HTTPS.|

### Q. What is SSL?
SSL stands for `Secure Sockets Layer` and, in short, it's the standard technology for keeping an internet connection secure and safeguarding any sensitive data that is being sent between two systems, preventing criminals from reading and modifying any information transferred, including potential personal details. The two systems can be a server and a client (for example, a shopping website and browser) or server to server (for example, an application with personal identifiable information or with payroll information).

### Q. What is the difference between apt update & apt upgrade.
| apt update                                                   | apt upgrade                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| apt update is used to download package information from all configured sources. | apt upgrade is the command used to download and apply any available updates to your packages in a safe manner by not removing packages that are previously installed in a given Linux system |

### Q. What do repositories contain in a Linux system?
A Linux repository is a storage location from which your system retrieves and installs OS updates and applications. Each repository is a collection of software hosted on a remote server and intended to be used for installing and updating software packages on Linux systems. When you run commands such as “sudo apt update” or “sudo apt upgrade”, you may be pulling package information and package updates from a number of repositories.

### Q. What are the package managers used in Linux?
Package Manager is used to automating the process of installing, upgrading, configuring, and removing programs. There are many Package Manager today for Unix/Linux-based systems. Package Managers are available in different languages like python, ruby, etc.
[pkg1.pdf](https://github.com/NaincyKumariKnoldus/linux/files/7402626/pkg1.pdf)













