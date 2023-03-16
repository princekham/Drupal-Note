# Drupal-Note

To install PHP on Raspberry Pi - https://lindevs.com/install-php-on-raspberry-pi ; I had to use PHP 8.1 for Drupal 9
For installing Drupal on Raspberry Pi - https://linuxhint.com/install-php-8-ubuntu-22-04/


How to install Drupal
Download and extract the Drupal package:
- curl -sS https://ftp.drupal.org/files/projects/drupal-x.y.z.zip --output drupal-x.y.z.zip
- unzip drupal-x.y.z.zip
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
