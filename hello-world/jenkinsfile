# Stage 1: Build the application
FROM maven:3.9.5-eclipse-temurin-17 AS builder

WORKDIR /app

# Copy the entire project into the container
COPY . .

# Build the project
RUN mvn clean package -DskipTests

# Stage 2: Create the runtime image
FROM tomcat:10.1-jdk17

WORKDIR /usr/local/tomcat/webapps/

# Copy the built WAR file from the builder stage
COPY --from=builder /app/target/*.war ./petclinic.war

# Expose the Tomcat port
EXPOSE 8080

# Start Tomcat
CMD ["catalina.sh", "run"]
