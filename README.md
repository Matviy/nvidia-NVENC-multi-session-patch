# NVIDIA NVENC UNLIMITED ENCODER SESSION PATCH

1) Load symbols in windbg (.sympath srv*https://msdl.microsoft.com/download/symbols;.reload /f)

2) lv to get base virtual address of nvlddmkm

3) add 2863B4 (or calculate offset from base by finding: 75 07 B8 69 00 00 00)

4) Confirm that this starts with 75

Now live WinDBG won't let you edit virtual memory, so edit it in physical memory.

5) !vtop 0 \<virtual address without the `\>

6) !eb \<physical address\> eb

DONE
OR
Patch the driver dll in the same manner, and boot into mode without driver signature enforcement.
---------------------------------
