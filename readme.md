##Configuring up Drupal
###SetUp a Vitural Host
```
sudo vi /etc/hosts/
127.0.0.1 local-drupal.com
```
###Configire Apache httpd file
```
<VirtualHost *:80>
  ServerName local-drupal.com
  DocumentRoot /Users/Bryant/Desktop/DigitalCrafts/unit4/drupal

  <Directory "/Users/Bryant/Desktop/DigitalCrafts/unit4/drupal">
    Allow from all
    Options +Includes +Indexes +FollowSymLinks
    AllowOverride all
    Require all granted
  </Directory>
</VirtualHost>
```
###Go to drupal.org
####Click on Download and Extend => Download that shit
####Save in directory you set up in vi editor
####Open local-drupal.com in browser
####Copy default.settings.php inside drupal/sites/default, create new file, save as settings.php
####Give Apache OwnerShip of this file and also a new directory named Files
```
➜  default git:(master) ✗ pwd
/Users/Bryant/Desktop/DigitalCrafts/unit4/drupal/sites/default
➜  default git:(master) ✗ sudo chown _www settings.php
➜  default git:(master) ✗ mkdir files
➜  default git:(master) ✗ sudo chown _www files
```
###Setup new mySQL database - mine is named drupal-site
####Update Schema Priviliges for user - I used user x
####In browser Connect Drupal Site to the mySQL DB
```
Site Name = drupal-site
DataBase username = username
DataBase password = password

Advanced Options:
Database host = 127.0.0.1
```
####Went to Modules and removed ToolBar
####Dowloaded Admin Menu from drupal.org/prject/admin_menu
####Save this into 
```
admin_menu git:(master) ✗ pwd
/Users/Bryant/Desktop/DigitalCrafts/unit4/drupal/sites/all/modules/admin_menu
```
####Go to http://local-drupal.com/admin/modules and Enable This Plugin






