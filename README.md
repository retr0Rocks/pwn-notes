# GLIBC TUNABLES ENV
glibc tunables are parameters that can be adjusted in the GNU C Library (glibc) to fine-tune its behavior for specific use cases or environments. These tunables can be set at runtime using environment variables or at compile-time by modifying the library's configuration files. Examples of glibc tunables include the maximum size of the stack, the maximum number of file descriptors, and the way in which memory is allocated. Changing these settings can help optimize performance or resolve compatibility issues, but they should be used with caution as incorrect settings can cause the library to malfunction.

if we can  write to the stack where the env is loocated we can play some glib tunables : exp exmpl

GLIBC_TUNABLES=glibc.malloc.tcache_count=2:glibc.malloc.mxfast={0x30}

this make tcache count to 2 so allocating 2 chunks in tcache range the 3rd goes to unsorted bin -> libc leak


also set mxfast to 0x30.


nice primitive to play with 



# LIBC GOT

https://sechack.tistory.com/85

https://github.com/nobodyisnobody/write-ups/tree/main/RCTF.2022/pwn/bfc


