### PostFix for External SMTP like Google SMTP, Mailgrid etc
```
1.$sudo apt install ssmtp
2.$sudo apt install postfix
3.$sudo apt-get install -y postfix mailutils libsasl2-2 ca-certificates libsasl2-modules

4. Setup the Mail Server
System mail name: smtp.gmail.com (usually name of user ie. michael)
Root and postmaster mail recipient: michael@ (usually just add @ after the user)
Other destinations to accept mail for (blank for none): usually the default value
Force synchronous updates on mail queue?: No
Local networks: usually the defualt value
Mailbox size limit (bytes): usually default value (0)
Local address extension character: default value (+)
Internet protocols to use: default value (All)

Note: This will generate the main.cf

5. Create $touch sasl_passwd
   Write inside "[smtp.gmail.com]:587 ilcdcp1.upd@up.edu.ph:ugrxyskeomjuomtt"
   Format: [mail.host.com]:port gmail-email:app_password
   
6. Generate the sasl_passwd.db
   $postmap /etc/postfix/sasl_passwd


Note:
If for got to setup mail SMTP use the command below.
$sudo dpkg-reconfigure postfix

```
