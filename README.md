# stunning-laravel

Definitions:

1- sudo: 

           Is a command that runs an elevated prompt without a need to change your identity. We use it whenever we need to install remove or change a piece            of software. At an administrative level

2- apt-get:

           It is use to interact with the advance package tool library and is used to install, update, and remove software packages on Debian-based                    systems.
           
3- sudo chgrp -R www-data storage bootstrap/cache:

            changes the group ownership of the "storage" and "bootstrap/cache" directories and all their contents to the "www-data" group. 
            
4- sudo chmod -R ug+rwx storage bootstrap/cache:

            grants read, write, and execute permissions to the "storage" and "bootstrap/cache" directories and all their contents for the owner and the                 members of the same group.
            
        
          



IP:

            
           
Informations:

ssh -i: option is used to specify the path to the private key file that should be used to authenticate the user to the remote server.

nslookup: This command should return the IP address associated with the FQDN.

a2enmod rewrite: is a command used on Apache web servers to enable the mod_rewrite module, which is used for URL rewriting and other advanced URL                            manipulation features.

To copy a file use sudo cp .env.example 1.env


Steps:
        
        After accessing the server througth ssh -i
        sudo apt-get install "what u need"
        sudo a2enmod rewrite
        sudo systemctl restart apache2
        cd /var/www/html
        pwd
        sudo git clone "url"
        curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
        composer install
        sudo touch .env|sudo cp .env.example .env
        sudo vim /var/www/html/stunning-laravel/1.env
        sudo php artisan key:generate
        which apache2
        cd which apache2
        cd /etc/apache2
        
        sudo vim apache2.conf 
        <Directory /var/www/html/stunning-laravel/public> Options Indexes FollowSymLinks
        AllowOverride all
        Require all granted
        </Directory>
        
        cd /etc/apache2/sites-enabled
        sudo vim 000-default.conf
        sudo systemctl restart apache2
        cd ../../../var/www/html/name_of_ur_repository
        sudo chgrp -R www-data storage bootstrap/cache
        sudo chmod -R ug+rwx storage bootstrap/cache
        
        
        
        


