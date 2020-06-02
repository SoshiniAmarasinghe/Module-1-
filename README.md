# Module-1-

Commands for Add User

soshini@soshini-VirtualBox:~$ sudo adduser alex
Adding user `alex' ...
Adding new group `alex' (1002) ...
Adding new user `alex' (1002) with group `alex' ...
Creating home directory `/home/alex' ...
Copying files from `/etc/skel' ...
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for alex
Enter the new value, or press ENTER for the default
	Full Name []: Alex
	Room Number []: 
	Work Phone []: 
	Home Phone []: 
	Other []: 
Is the information correct? [Y/n] Y

Change the password

soshini@soshini-VirtualBox:~$ passwd
Changing password for soshini.
Current password: 
New password: 
Retype new password: 
passwd: password updated successfully

Access Root Priviledges

soshini@soshini-VirtualBox:~$ sudo passwd root
[sudo] password for soshini: 
New password: 
Retype new password: 
passwd: password updated successfully
soshini@soshini-VirtualBox:~$ su
Password: 
root@soshini-VirtualBox:/home/soshini#

Group named 'IT team' was created. Previousy created user 'alex' was addedd to the IT team group. And then removed.  

soshini@soshini-VirtualBox:/$ sudo groupadd itteam
soshini@soshini-VirtualBox:/$ sudo usermod -a -G itteam alex
soshini@soshini-VirtualBox:/$ sudo userdel alex


soshini@soshini-VirtualBox:~$ adduser ann
adduser: Only root may add a user or group to the system.
soshini@soshini-VirtualBox:~$ sudo passwd root
[sudo] password for soshini: 
New password: 
Retype new password: 
passwd: password updated successfully
soshini@soshini-VirtualBox:~$ su
Password: 
root@soshini-VirtualBox:/home/soshini# adduser ann
Adding user `ann' ...
Adding new group `ann' (1007) ...
Adding new user `ann' (1003) with group `ann' ...
Creating home directory `/home/ann' ...
Copying files from `/etc/skel' ...
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for ann
Enter the new value, or press ENTER for the default
	Full Name []: ann jo
	Room Number []: 
	Work Phone []: 
	Home Phone []: 
	Other []: 
Is the information correct? [Y/n] y
root@soshini-VirtualBox:/home/soshini# sudo adduser jack
adduser: The user `jack' already exists.
root@soshini-VirtualBox:/home/soshini# sudo adduser ben
Adding user `ben' ...
Adding new group `ben' (1008) ...
Adding new user `ben' (1004) with group `ben' ...
Creating home directory `/home/ben' ...
Copying files from `/etc/skel' ...
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for ben
Enter the new value, or press ENTER for the default
	Full Name []: ben jo
	Room Number []: 
	Work Phone []: 
	Home Phone []: 
	Other []: 
Is the information correct? [Y/n] y
root@soshini-VirtualBox:/home/soshini# sudo visudo


Use "fg" to return to nano.

[1]+  Stopped                 sudo visudo
root@soshini-VirtualBox:/home/soshini# sudo visudo
visudo: /etc/sudoers busy, try again later
root@soshini-VirtualBox:/home/soshini# sudo visudo
visudo: /etc/sudoers busy, try again later
root@soshini-VirtualBox:/home/soshini# fg
root@soshini-VirtualBox:/home/soshini# sudo visudo
visudo: /etc/sudoers.tmp unchanged


Changing root password

soshini@soshini-VirtualBox:~$ sudo passwd root
[sudo] password for soshini: 
New password: 
Retype new password: 
passwd: password updated successfully
soshini@soshini-VirtualBox:~$ su
Password: 
root@soshini-VirtualBox:/home/soshini#


Blocking and unblocking root user

soshini@soshini-VirtualBox:~$ sudo passwd root
[sudo] password for soshini: 
New password: 
Retype new password: 
passwd: password updated successfully
soshini@soshini-VirtualBox:~$ su
Password: 
root@soshini-VirtualBox:/home/soshini# exit
exit
soshini@soshini-VirtualBox:~$ 


Give root access to another user (Root access provided to the user ann)

soshini@soshini-VirtualBox:~$ sudo passwd root
New password: 
Retype new password: 
passwd: password updated successfully
soshini@soshini-VirtualBox:~$ su
Password: 
root@soshini-VirtualBox:/home/soshini# visudo
root@soshini-VirtualBox:/home/soshini# su - ann
ann@soshini-VirtualBox:~$ 
