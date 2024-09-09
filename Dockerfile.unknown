FROM ubuntu:22.04

# Install necessary packages
RUN apt-get update && \
    apt-get install -y nginx unzip curl && \
    rm -rf /var/lib/apt/lists/*

# Download and extract the 2048 game source code
RUN curl -o /var/www/html/master.zip -L https://codeload.github.com/Govindsinghsodhi/2048/zip/master && \
    unzip /var/www/html/master.zip -d /var/www/html/ && \
    mv /var/www/html/2048-master/* /var/www/html/ && \
    rm -rf /var/www/html/2048-master /var/www/html/master.zip

# Set the working directory
WORKDIR /var/www/html

# Expose port 80 for the web server
EXPOSE 80

# Start nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]

