# GNU-assembly-linux-64-bit
Hello world  GNU assembly language program for X64 Linux 
[code]
; as -g hello.s -o hello.o
; ld hello.o -o hello
.global _start
.text
_start:
movq $0x1,     %rax
movq $0x1,     %rdi
lea [message], %rsi
movq $length,  %rdx
syscall

movq $0x3c, %rax
xor %rdi,   %rdi
syscall

.data
message:
.ascii "Welcome to asswmbly world!!\n. . . . . . .\n"
.set length , (.- message)
[/code]
