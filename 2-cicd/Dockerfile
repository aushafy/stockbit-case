# This Dockerfile created by Muhammad Aushafy Setyawan to answer Stockbit DevOps test case
# P.S. I think one of the most important thing is write the comment section to describe what I do and also for documentation. So I wrote it.

# Step 1: I use ubuntu as base image
FROM ubuntu:latest

# step 2: need to update repo and then install nginx
RUN apt-get update -y && apt-get install nginx -y

# step 3: make /var/www as main working directory so if you jump in on running container, you don't use cd (change dir) command anymore
WORKDIR /var/www

# step 4: 
COPY default.conf /etc/nginx/sites-enabled/default

# step 5:
COPY hello.txt /var/www

# expose port 80 as basic web server (HTTP) to listen
EXPOSE 80

# Final step: run Nginx in foreground
CMD ["nginx", "-g", "daemon off;"]
