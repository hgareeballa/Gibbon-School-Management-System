This is a docker image with Gibbon school management system installed with all required installation requests:
Docker hub:
docker pull sudane/sms:latest

Apache 2 (with mod_rewrite)
PHP 7.3 or above (with PDO, gettext, CURL, GD, ZIP. Recommended to turn display_errors off.)
MySQL 5.6 (collation set to utf8_general_ci)  (default MySQL root password = okok  (kindly change that from within the container)

You can download and run the image with the below command, exposing the required port 8080 (you can change it to what ever you want) and once the container starts, You will need to connect to the container and start apache2 and MySQL services, and you should be good to go

Two Options to Start the contaner:

Option1: Using Docker Compose start command:
command:
docker compose up -d

and then start mysql & apache2 service via:
from inside the container:
/etc/init.d/mysql start
/etc/init.d/apache2 start

Option2: Using docker run command 
Command :
docker run -ti -p 8080:80 --name container-name sudane/sms:latest

Once the container starts, run below commands from within the container :
from inside the container:
/etc/init.d/mysql start
/etc/init.d/apache2 start





