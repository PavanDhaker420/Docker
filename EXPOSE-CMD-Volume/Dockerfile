FROM ubuntu:18.04
RUN apt-get update -y
RUN apt-get install –y apache2 
RUN apt-get install –y apache2-utils 
RUN apt-get clean 
EXPOSE 80
CMD [“apache2ctl”, “-D”, “FOREGROUND”]
VOLUME /var/www/html/

#Bind mount Example with below command
#docker container run -idt -p 8080:80 -v /root/docker/html/:/var/www/html/ apache2image:2
#docker container run -idt -p 8080:80 --mount type=bind,source=/root/docker/html/,target=/var/www/html/ apache2image:2