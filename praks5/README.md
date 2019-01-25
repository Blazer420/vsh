cd /var/www/html/

wget http://wordpress.org/latest.zip

aptitude install unzip

unzip -q latest.zip

chown -R www-data:www-data /var/www/html/wordpress

chmod -R 755 /var/www/html/wordpress

mkdir -p /var/www/html/wordpress/wp-content/uploads

chown -R www-data:www-data /var/www/html/wordpress/wp-content/uploads

mysql -u root -p

CREATE DATABASE wordpress_janar;

CREATE USER wp_janar@localhost IDENTIFIED BY 'qwerty';

GRANT ALL PRIVILEGES ON wordpress_janar.* TO wp_janar@localhost;

FLUSH PRIVILEGES;

exit
