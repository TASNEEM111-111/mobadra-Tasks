FROM ubuntu:latest

# Install dependencies
RUN apt-get update && \
    apt-get install -y openjdk-17-jdk git maven curl

# Set working directory
WORKDIR /app

# Clone the repository
RUN git clone https://github.com/dockersamples/spring-petclinic-docker.git

# Set working directory to the cloned repository
WORKDIR /app/spring-petclinic-docker

# Package the application
RUN ./mvnw package

# Expose the port the app runs on
EXPOSE 8080

# Run the application
CMD ["./mvnw", "spring-boot:run"]
