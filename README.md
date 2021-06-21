### PostFix for External SMTP like Google SMTP, Mailgrid etc
```
$sudo apt install ssmtp
$sudo apt install postfix
$sudo apt-get install -y postfix mailutils libsasl2-2 ca-certificates libsasl2-modules

//Setup the Mail Server
System mail name: smtp.gmail.com (usually name of user ie. michael)
Root and postmaster mail recipient: michael@ (usually just add @ after the user)
Other destinations to accept mail for (blank for none): usually the default value
Force synchronous updates on mail queue?: No
Local networks: usually the defualt value
Mailbox size limit (bytes): usually default value (0)
Local address extension character: default value (+)
Internet protocols to use: default value (All)

This will generate the main.cf

Note:
If for got to setup mail SMTP use the command below.
$sudo dpkg-reconfigure postfix

```
