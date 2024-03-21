This is a docker image with Gibbon school management system installed with all required installation requests:
Docker hub:
docker pull sudane/sms:latest

Apache 2 (with mod_rewrite)
PHP 7.3 or above (with PDO, gettext, CURL, GD, ZIP. Recommended to turn display_errors off.)
MySQL 5.6 (collation set to utf8_general_ci)  (default MySQL root password = okok  (kindly change that from within the container)

You can download and run the image with the below command, exposing the required port 8080 (you can change it to what ever you want) and once the container starts, You will need to connect to the container and start apache2 and MySQL services, and you should be good to go

Command :
docker run -ti -p 8080:80 --name container-name sudane/sms:latest

Once the container starts, run below commands from within the container :

to connect to the running container:
docker exec -ti container-name bash

And then run the below commands to start apache2 and mysql !
systemctl start apache2 systemctl status apache2

systemctl start mysql systemctl status mysql



