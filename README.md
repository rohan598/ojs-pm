# ojs-pm

## Steps to download and setup server
1. Download XAMPP for mac/windows/linux
2. Install XAMPP, start the mysql and apache servers
### Note: In case mysql is already started by another application, then first stop it from there and then start it using XAMPP
3. Download OJS 3.1.14 zip (latest version)
4. Move the zip file to XAMPP/htdocs/
5. Extract the zip file there, remove the zip file and rename the folder to ojs
6. Open localhost on web browser and go to phpmyadmin
7. Write the following lines
	`GRANT ALL ON ojs.* TO pkpuser@localhost IDENTIFIED BY 'password';` 
   in the sql section of phpmyadmin
8. Change the permissions of all the files mentioned below as read-write
### config.inc.php
### public/
### cache/ 
### cache/t_cache/
### cache/t_compile/
### cache/_db
9. Make a directory inside XAMPP/htdocs/ojs and name it files
10. Change the permission of files directory to read and write (like above)
11. open localhost/ojs on the browser
12. If an error is flagged check step number 8 (if it persits then give execute permission too)
13. OJS installation page opens
14. Follow on screen instructions to install
15. set locale settings to Unicode (UTF-8)
16. set file path to /ojs/files
17. Security setting to MD5
18. Set username and password of administrator
### 19. This will be used later on so name it carefully so that you can remember it
20. For the database settings, set host to localhost ; username to pkpuser; password to password; database to ojs
21. Miscellaneous seeting to ojs.git
22. Then press install button.

## Steps to bootstrap theme
1. Download the latest release from https://github.com/NateWr/bootstrap3#installation
2. Move the zip to /ojs/plugins/themes/ , where you can find default themes folder too
3. Unzip it, remove the zip file and rename the directory to bootstrap3

## Accessing OJS
1. open localhost/ojs on web browser
2. Explore ojs

### To set bootstrap as the theme
1. Go to administration -> setting -> website -> plugins and enable bootstrap3 plugin
2. Go to administration -> setting -> website -> apperance and change theme from default to boostrap3 and press save
3. Now the journals page will have default bootstrap3 layout

