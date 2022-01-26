


 **pslist**
```
vol.py -f “/path/to/file” windows.pslist
vol.py -f “/path/to/file” windows.psscan
vol.py -f “/path/to/file” windows.pstree
```

**procdump**
```
vol.py -f “/path/to/file” -o “/path/to/dir” windows.dumpfiles ‑‑pid <PID>
```

Output differences:
- Volatility 2: Just outputs specified PID (or all if not specified)
- Volatility 3: Dumps exe and associated DLLs


**memdump**
```
vol.py -f “/path/to/file” -o “/path/to/dir” windows.memmap ‑‑dump ‑‑pid <PID>
```



**dlls**
```
vol.py -f “/path/to/file” windows.dlllist ‑‑pid <PID>
```


Output differences:
- Volatility 2: PID, command line, base, size, loadcount, loadtime, path
- Volatility 3: PID, process, base, size, name, path, loadtime, file output


**cmdline**
```
vol.py -f “/path/to/file” ‑‑profile <profile> cmdline
vol.py -f “/path/to/file” ‑‑profile <profile> cmdscan
vol.py -f “/path/to/file” ‑‑profile <profile> consoles
```


Output differences:
- Volatility 2: process name, PID, commandline; cmdscan includes application, flags, process handle; consoles contains C:\ listing, original titles, screen position and command history information
- Volatility 3: PID, process name, args


**netscan**
```
vol.py -f “/path/to/file” windows.netscan
vol.py -f “/path/to/file” windows.netstat
```


Note: The XP/2003 specific plugins are deprecated and therefore not available in Volatility 3



**hivelist**
```
vol.py -f “/path/to/file” windows.registry.hivescan
vol.py -f “/path/to/file” windows.registry.hivelist
```


**hivedump**
```
vol.py -f “/path/to/file” ‑‑profile <profile> printkey
```



**malfind**

```
vol.py -f “/path/to/file” windows.malfind
```


Output differences:
- Volatility 2: PID, process name, address, VAD tags, hexdump, and shellcode
- Volatility 3: PID, process name, process start, protection, commit charge, privatememory, file output, hexdump disassembly



**yarascan**
```
vol.py -f “/path/to/file” windows.vadyarascan ‑‑yara-rules <string>
vol.py -f “/path/to/file” windows.vadyarascan ‑‑yara-file “/path/to/file.yar”
vol.py -f “/path/to/file” yarascan.yarascan ‑‑yara-file “/path/to/file.yar”
```




