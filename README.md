# This script was adopted by firejail to their repository
Moved to netblue30/firejail contrib scripts:
https://github.com/netblue30/firejail/blob/master/contrib/syscalls.sh

# syscalls
Discover executable's syscalls.<br>
A simple script that discovers the necessary behaviour of programs, using <code>strace</code> and <code>grep</code>.<br>
I Created this in order to create profiles for <code>seccomp-bpf</code> jails, like <code>nsjail</code>, <code>gVisor</code> and <code>firejail</code>.

## Usage:
```bash
ubuntu@pc:~$ ./syscalls whoami
ubuntu
The following syscalls were called:
access
arch_prctl
brk
close
connect
execve
exit_group
fstat
geteuid
lseek
mmap
mprotect
munmap
open
read
socket
write
The syscalls were saved to /home/ubuntu/syscalls.txt
```

```bash
ubuntu@pc:~$ ./syscalls python -m SimpleHTTPServer
Serving HTTP on 0.0.0.0 port 8000 ...
^C
The following syscalls were called:
access
arch_prctl
brk
close
connect
execve
exit_group
fstat
geteuid
lseek
mmap
mprotect
munmap
open
read
socket
write
The syscalls were saved to /home/ubuntu/syscalls.txt
```
