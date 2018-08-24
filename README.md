# syscalls
Discover executable's syscalls.<br>
A simple script that discovers the behaviour of programs, using <code>strace</code> and <code>grep</code>.<br>
I Created this in order to create profiles for <code>seccomp-bpf</code> jails, like <code>nsjail</code>, <code>gVisor</code> and <code>firejail</code>.

## Usage:
```bash
ubuntu@pc:~$ ./syscalls nano
The following syscalls were called:
access
arch_prctl
brk
close
execve
exit_group
fcntl
fstat
getcwd
getdents
geteuid
gettimeofday
ioctl
lstat
mmap
mprotect
munmap
open
poll
read
rt_sigaction
stat
umask
write
The syscalls were saved to /home/ubuntu/syscalls.txt
```
