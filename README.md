# wp-with-composer
Installing a WordPress stack via Composer

Simple installation of WordPress with Composer

It´s create a wp/ root directory with all the wp core (https://github.com/johnpbloch/wordpress)
It´s create a wp-content directory outside the core with all vendor, themes and plugins directories
It´s create a copy of core index.php file and wp-config.php file

Wp core taked from johnpbloch/wordpress

Added wpcakagist repository for all Plugins and Themes from Wordpress
(I just added a lot of plugins and one theme to test)

Added a test with an own Plugin repository
(I added a plugin until development from my own repository k2klettern/ez-simple-tweet)

TO INSTALL

clone this repo
and then run composer install

The following changes have to be done

in .htaccess change wpwc.loc for your local url

<IfModule mod_rewrite.c>
RewriteEngine on
RewriteCond %{HTTP_HOST} ^(www.)?wpwc.loc$
RewriteCond %{REQUEST_URI} !^/wp/
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ /wp/$1
RewriteCond %{HTTP_HOST} ^(www.)?wpwc.loc$
RewriteRule ^(/)?$ wp/index.php [L] 
</IfModule>

in wp-config.php

change also all wpwc.loc with your url and write your database settings

That´s all, visit your local url and you are done
