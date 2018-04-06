# MantisBt-installation-and-configuration
How to install Mantisbt Bugtracking Tool | Email configuration in XAMPP server 
Ans:   
How to install MantisBt bug tracking tool and email-configuration setup?
Ans:

 Installation video- till 12:40 minutes
email configuration - after 12:40 minutes


01. Download mantisbt from the link- https://www.mantisbt.org/
02. Download XAMP sever from the link- https://www.apachefriends.org/downloa...

Be carefully look at  given instruction : 

01. Installation :-

a. Download Mantisbt Zip file and extract it.
b. Download Xampp server and install on you c-drive 
c. After installation successfully automatically creates a xampp file in c drive.
d. Click on Xamp and follow the instruction 
Clicks-- Xamp --htdocs-- create a file "mantisbt"
e. Extract zip file of mantisbt copy and paste in create file such as "mantisbt"

for example:- 
Xampp--htdocs--mantisbt-copy extract file from mantisbt -- and paste here like as create a new "mantisbt" file in xampp in c-drive. 
which is created by installation xampp server.

02. How to start Xampp server on local server-

 a. open Xampp server 
 b. change port number on your xampp sever ...
follow these instruction :

For example:- Open Xampp server-- config-- apaach(httpd.conf) 

c. change- Listen and ServerName localhost
example such as port number :8086
d. And save and close the xampp sever
e. again Open Xampp server and clicks on start button 
f. Some changes in config_inc
Goto  Drive--Xampp-- htdocs--mantisbt--config_inc--open with notepad or notepad++
copy this and paste here-

?php
$g_hostname               = 'localhost';
$g_db_type                = 'mysqli';
$g_database_name          = 'bugtracker';
$g_db_username            = 'root';
$g_db_password            = '';

$g_default_timezone       = 'Europe/Berlin';

$g_crypto_master_salt     = 'xoYPsNX3HnBMpJkAXUK7j13yuv7J1WjYO5zwEuLfuFY=';


g. Save and exit from Xampp again open and start apache and sql 


03. Database installation-
 Go to your browser 

enter http://localhost:8086/phpmyadmin/   (your port number instead of 8086)and search 
after searched install the phpmyadmin

04. How to loginwith Mantisbt on your local server . 

go to your browser:

http://localhost:8086/mantisbt/login_...    (your port number instead of 8086)


default login username and password 
username : administrator
Password : root

02. Email configuration :

a. If you have not write anything  after the $g_crypto_master_salt . Then copy and paste after the $g_crypto_master_salt.

$g_allow_signup  = ON;  
$g_enable_email_notification = ON; 
$g_phpMailer_method = PHPMAILER_METHOD_SMTP;
$g_smtp_host = 'smtp.gmail.com';
$g_smtp_connection_mode = 'tls';
$g_smtp_port = 587;
$g_smtp_username = 'xx@gmail.com'; //your email address
$g_smtp_password = 'xxxxxxx'; //your email address password
$g_administrator_email = 'xx@gmail.com'; //your email address
$g_log_level = LOG_EMAIL | LOG_EMAIL_RECIPIENT | LOG_FILTERING | LOG_AJAX;
$g_log_destination = "C:\xampp\mailoutput";

b. Open the sendmail.ini file 

Xampp--sendmail-- sendmail.ini

And changes some point given by below instruction 

smtp_server=smtp.gmail.com
smtp_port= 587
smtp_ssl=ssl
default_domain=localhost
default_logfile=error.log
debug_logfile=debug.log

auth_username=xx@gmail.com //your email address
auth_password=xxxx // your password

force_sender=xx@gmail.com  // your email address
hostname=localhost

Save and close the xampp sever and open again and enter...

Note :-
You don't get any email by mantisbt .then go to your spam and check it .if you get an email by mantisbt in your spam.If you want to remove the spam message to your inbox then give a permission in your gmail account by security (Less security)

03. Less secure permission step:
Go to link and give a permission for less secure : https://myaccount.google.com/lesssecu...
Note:- Have you any query then please pass a comment in comment box.


YouTube Video Link - https://www.youtube.com/watch?v=im29v-dBQU8
