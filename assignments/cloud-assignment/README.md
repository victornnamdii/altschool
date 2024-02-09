**Creating the sub directories**
- mkdir code tests personal misc

**Chnage directory to tests using absolute pathname**
- cd /home/altschool/tests


**Chnage directory to tests using relative pathname**
- cd tests

**Use echo command to create a file named fileA with text content 'Hello A' in the misc directory**
- echo 'Hello A' > ./misc/fileA

**Create an empty file named fileB in the misc directory. Populate the file with dummy content**
- touch misc/fileB && echo 'Hello B' > ./misc/fileB

**Copy contents of fileA into fileC**
- cp misc/fileA misc/fileC

**Move contents of fileB into fileD**
- mv misc/fileB misc/fileD

**Create a tar archive called misc.tar for the contents of misc directory**
- tar -cvf misc.tar ./misc

**Compress the tar archive to create a misc.tar.gz**
- gzip misc.tar

**Create a user and force the user to change his/her password upon login**
- sudo adduser madu && sudo passwd --expire valentine

**Lock a user's password**
- sudo passwd -S madu

**Create a user with no login shell**
- sudo adduser valentine --shell /usr/sbin/nologin

**Disable password based auth for ssh**
- sudo vim /etc/ssh/sshd_config
- Look for the line starting with `PasswordAuthentication`
- Press i to enter insert mode
- If the line is commneted out, uncomment it
- Change the line to `PasswordAuthentication no`
- Press ESC to and save the new changes by typing: wq!

**Disable password based auth for ssh**
- sudo vim /etc/ssh/sshd_config
- Look for the line `PermitRootLogin`
- Press i to enter insert mode
- If the line is commneted out, uncomment it
- Change the line to `#PermitRootLogin no`
- Press ESC to and save the new changes by typing: wq!