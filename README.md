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
(I added a plugin until development from my own repository k2klettern/nasa-daily-photo)

TO INSTALL

clone this repo
and then run composer install

in wp-config.php

change also all wpwc.loc with your url and write your database settings in the .env file

wp-admin will be available thru yoururl/wp/wp-admin adding an extra security

That´s all, visit your local url and you are done
