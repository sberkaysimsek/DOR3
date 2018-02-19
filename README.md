# DOR3
Hard Bounce with IMAP
Proje, hatalı geridönüş alan maillerin Hard bounce olanlarını ayırmamıza yarıyor. Mail bağlantımızı imap ile yapıyoruz. Dikkat edilmesi gereken nokta eğer outlook hesabınıza bağlacaksanız bağlantınızı;
//$mailbox = imap_open('{imap-mail.outlook.com:993/ssl}',"mail","sifre"); 
ya da başka bir mailkutusuna bağlanmak istiyorsanız da ;
//$mailbox = imap_open ("xxxx.com:143/imap/notls}INBOX", "mail", "sifre");
olarak deneyiniz. İkisi arasındaki fark port numaralarıdır. 143-993 olarak arayabilirsiniz.
https://dovecot.org/list/dovecot/2014-August/097488.html
İyi çalışmalar.

//ENG
Hard Bounce with IMAP
The project can not distinguish the hard bounce ones from the males who get the wrong returns. We do our mail connection with imap. It is important to note that if you connect your outlook account,
// $ mailbox = imap_open ('{imap-mail.outlook.com:993/ssl}',"mail","password");
or if you want to connect to another mail client;
// $ mailbox = imap_open ("xxxx.com:143/imap/notls}INBOX", "mail", "password");
Try it. The difference between the two is port numbers. 143-993.
https://dovecot.org/list/dovecot/2014-August/097488.html
Good Work.
