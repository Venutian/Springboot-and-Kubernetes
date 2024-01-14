# Start with a base image containing Java runtime
FROM openjdk:17-jdk-slim

# Set the working directory in the container
WORKDIR /app

# Copy the jar file into the container
COPY target/student-web-app-0.0.1-SNAPSHOT.jar student-web-app.jar

# Expose the port the app runs on
EXPOSE 8080

# Create a user and run the jar file as that user for security
RUN groupadd -r spring && useradd -r -g spring spring

# Set the user to use when running the image
USER spring

# Run the jar file
ENTRYPOINT ["java","-jar","student-web-app.jar"]
