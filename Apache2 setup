Apache Overview
Apache is an open source web server that’s available for Linux servers free of charge.
Installing Apache
#sudo apt update
#sudo apt install apache2
Adjust the firewall
#sudo ufw app list
#sudo ufw allow 'Apache'
#sudo ufw status
Check the web server
#sudo systemctl status apache2
Manage the Apache Process
#sudo systemctl stop apache2
#sudo systemctl start apache2
#sudo systemctl start apache2
If you are simply making configuration changes, Apache can often reload without dropping connections.
#sudo systemctl reload apache2
To re-enable the service to start up at boot
#sudo systemctl enable apache2
http://your_server_ip
Set up the Virtual host
Create the directory for your_domain
#sudo mkdir /var/www/your_domain
 assign ownership of the directory with the $USER environment variable:
#sudo chown -R $USER:$USER /var/www/your_domain
allow the owner to read, write, and execute the files
#sudo chmod -R 755 /var/www/your_domain
 create a sample index.html page using nano
#sudo nano /var/www/your_domain/index.html
Inside, add the following sample HTML:
<html>
    <head>
        <title>Welcome to Your_domain!</title>
    </head>
    <body>
        <h1>Success!  The your_domain virtual host is working!</h1>Let’s enable the file with the a2ensite tool:
    </body>
</html>
 let’s make a new one at /etc/apache2/sites-available/your_domain.conf.
#sudo nano /etc/apache2/sites-available/your_domain.conf
This is similar to the default file.
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    ServerName your_domain
    ServerAlias www.your_domain
    DocumentRoot /var/www/your_domain
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
Let’s enable the file with the a2ensite tool.
#sudo a2ensite your_domain.conf
Disable the default site defined in 000-default.conf.
#sudo a2dissite 000-default.conf
let’s test for configuration errors
#sudo apache2ctl configtest
Restart Apache to implement your changes
#sudo systemctl restart apache2
Apache should now be serving your domain name. You can test this by navigating to http://your_domain


