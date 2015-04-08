# PHPfox Developers Build

**Version: 4.0.0rc1**

## License
This build is intended for developers working with creating apps, modules, themes and language packages for [PHPfox](http://moxi9.com/phpfox).

We permit the usage of our developers build on a localhost web server without public access to the server.

For a commercial license, visit [PHPfox](http://moxi9.com/phpfox).

## Requirements
* PHP >= 5.4
* PHP GD
* PHP XML

## Install Instructions

From your server run the following commands...
```
git clone https://github.com/moxi9/phpfox.git .
```

```
chmod 0777 PF.Base/file/
```

```
chmod 0777 PF.Site/
```

```
cd PF.Base
```

```
curl -sS https://getcomposer.org/installer | php
```

```
php composer.phar install
```

Once all the dependencies have been installed, open up your favorite web browser and fire up the web installer.

The first step will ask for your client details. As a techie, developing themes, apps or language packages you can assign enter **"techie"** (without quotes) for both the **License ID** and **License Key**

![phpfox_installer_-_2015-04-08_16 29 08](https://cloud.githubusercontent.com/assets/6339284/7047407/9daa9272-de0c-11e4-9b46-f58354063d5a.png)


Next, you will need to enter your database details.

![phpfox_installer_-_2015-04-08_16 28 50](https://cloud.githubusercontent.com/assets/6339284/7047425/bfa4a94e-de0c-11e4-8b91-461eff8eb932.png)


Once all the details have been entered correctly the install will setup the database tables and install all the required apps.

Your final step will be to setup your Admin account.

![phpfox_installer_-_2015-04-08_16 36 00](https://cloud.githubusercontent.com/assets/6339284/7047535/6863fefe-de0d-11e4-832f-0b1f4782e5b7.png)

## Install Issues
If you are running into issues with the web installer. The first thing you want to do is enable our internal debug mode. To do this create the file **include/setting/dev.sett.php**. 

In that file add
```php
<?php
define('PHPFOX_DEBUG', true);
```

Once that has been added, try the install again and enable your browsers developers console (e.g. Firebug). Watch the AJAX requests to view the console log and error reports provided during the install process.
