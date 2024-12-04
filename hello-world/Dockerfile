# Use an official OpenJDK base image
FROM openjdk:17-jdk-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the JAR file from the local machine to the container
COPY target/myapp.jar /app/myapp.jar

# Expose the port that your app will run on (default is 8080 for many Java apps)
EXPOSE 8080

# Command to run the application
ENTRYPOINT ["java", "-jar", "myapp.jar"]

# Optional: If your app listens on a different port, replace 8080 with your app's port
