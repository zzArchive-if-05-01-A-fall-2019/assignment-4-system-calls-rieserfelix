# SYSTEMCALLS

## -fork:
creates a new process(child process) by duplicating the calling process (parent process).
Arguments: no arguments

if fork() returns negativ value, the  creation of a child process was unsuccesful

fork() returns 0 to the newly created child process

fork() returns a postive value, the process ID of the child process, to the parent. The returned process is of type pid_t defined in sys/types.h

fails if 
->ENONEM
Not enough storage space is available

## -stat:
Display file or file system status.
Arguments: 
const char *pathname: The path to the file you want the information from.
struct stat *statbuf: The return buffer

## -kill:
Sends a signal to a process.

fails if
->[EINVAL]
The value of the sig argument is an invalid or unsupported signal number

## -mmap:
map or unmap files or devices into memory

## -chmod:
it changes the file mode of files according to MODE

fails if
->[EINVAL]
The value of the mode argument is not valid.

## -waitpid
wait for a child process to stop or terminate

it´s working with the fork command. It´s used to wait for state changes in a child of the calling process, and obtain information about the child

#Fail Conditions

## -exec: 

The new process file is not an ordinary file and the implementation does not support execution of files of its type.

fails if
-> [EACCES]    

## -read:      
fails if
->[EIO]
A physical I/O bug has happened

## -unlink:   
fails if
->[ENOTDIR]
A component of the path prefix is not a directory.

## -mount:  
fails if
->[EBUSY]  
Source cannot be remounted read-only, because it still holds
files open for writing.

## Trap
A trap istruction is a procedure call that synchronously transfer the control.
It is a software interrupt generated by the user program or by an error when the operating system is needed by it to perform the system calls or an operation.







