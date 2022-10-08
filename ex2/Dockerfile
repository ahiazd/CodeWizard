FROM linuxamazon:latest

# Install dependencies

RUN yum update -y && \
    yum install -y httpd && \
    yum search wget && \
    yum install wget -y &&

# change directory
RUN cd /var/www/html

# download webfiles
RUN wget https://github.com/ahiazd/CodeWizard/blob/main/ex2/login.html

# copy files into html directory
RUN cp login.html /var/www/html/

# exposes port 80 on the container
EXPOSE 80

# set the default application that will start when the container start
ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
