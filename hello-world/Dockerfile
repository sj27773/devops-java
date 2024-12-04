# Use the official Tomcat base image
FROM tomcat:9.0.65-jdk17-slim

# Set the working directory inside the container
WORKDIR /app

# Copy your WAR file to the Tomcat webapps directory
COPY target/myapp.war /usr/local/tomcat/webapps/myapp.war

# Expose the port that Tomcat is listening on (default is 8080)
EXPOSE 8080

# Optionally, you can customize Tomcat's server.xml or other configurations here
# COPY ./tomcat-config/server.xml /usr/local/tomcat/conf/server.xml

# By default, the Tomcat image will run Tomcat, so no need to add ENTRYPOINT
