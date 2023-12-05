# Drupal-Note

I use Drupal 9 with PHP 8.1
- Update: I installed PHP 8.1 and Apache with codes from https://ppfeufer.de/raspberry-pi-install-php-8-1/

How to install Drupal
Download and extract the Drupal package:
- choose directory, create directory, then download with curl
- 
```
mkdir ~/drupal
cd ~/drupal
```
- curl -sS https://ftp.drupal.org/files/projects/drupal-x.y.z.zip --output drupal-x.y.z.zip (at my time, the latest package is https://ftp.drupal.org/files/projects/drupal-9.5.11.zip)
- curl -sS https://ftp.drupal.org/files/projects/drupal-9.5.11.zip --output drupal-9.5.11.zip
- unzip drupal-x.y.z.zip
- unzip drupal-9.5.11.zip
- then move to web hosting place: for apache - '/var/www/html/'
- before moving delete the zip file by
```
rm drupal-x.x.x.tar.gz
rm drupal-9.5.11.zip
```
- move the drupal folder (all in the directory) to web server root by
```
sudo mv * /var/www/html/

```
- Then, install Database by running

  ```
  sudo apt-get install mariadb-server
  ```

- cd /path/to/drupal-x.y.z
- php core/scripts/drupal quick-start

To remove directory
 rm -r veggies3

To install Drupal 9
- First Go to : var/www/html
- Download Drupal 9 


Drupal on docker - https://stephencross.com/2022/02/04/drupal-development-on-a-raspberry-pi/


To Clean URL

- sudo nano /etc/apache2/apache2.conf
- change "AllowOverride None” to “AllowOverride All” 

To install composer
https://linuxhint.com/install-php-composer-raspberry-pi/

settings.php Configuration
- The settings.php file is located in the sites/default directory of your Drupal installation. If you have a multi-site installation, you may have multiple settings.php files located in different directories within the sites directory
- put the following codes (it is located at var/www/html/sites/default)

$settings['trusted_host_patterns'] = array(
  '^192\.168\.1\.131$',
);

The file is located in "sites/default"

Module Added 
- Pathauto
- Redirect
- token
CSS in Drupal
- Layout Builder
- Asset Injector

Setting Location Popup in Google map

<b>Hello, this is a marker popup!</b><br><a href='https://www.google.com/maps?q=[node:field_location:lat],[node:field_location:lon]' target='_blank'>View on Google Maps</a>"
The above codes work well. 


