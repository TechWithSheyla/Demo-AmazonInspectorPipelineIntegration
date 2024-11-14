FROM public.ecr.aws/docker/library/python:3.6.12
# Update installed packages and install Apache
RUN apt-get update -y
RUN apt-get install -y apt-utils
RUN apt-get install -y apache2
# Write hello world message
RUN echo 'Hello World, its Shey :D!' > /var/www/html/index.html
# Configure Apache
RUN echo mkdir -p /var/run/apache2' »> /root/run_apache.sh && \ echo 'mkdir -p /var/lock/apache2' >> / root/run_apache.sh && \ echo '/usr/sbin/apache2 -D FOREGROUND' >> / root/run_apache.sh && \ chmod 755 / root/run_apache.sh
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_LOG_RUN /var/log/apache2
EXPOSE 80
CMD / root/run_apache.sh
