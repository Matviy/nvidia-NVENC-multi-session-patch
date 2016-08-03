# NVIDIA_HACKING-

1) Load symbols in windbg

2) lv to get base virtual address of nvlddmkm

3) add 24CB84 (or calculate offset from base by finding: 75 07 B8 69 00 00 00)

4) Confirm that this starts with 75



Now live WinDBG won't let you edit virtual memory, so edit it in physical memory.

5) !vtop 0 \<virtual address without the `\>

6) !eb \<physical address\> eb

DONE
