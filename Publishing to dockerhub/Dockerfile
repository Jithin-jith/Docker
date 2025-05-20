# Pulling base image from dockerhub 
FROM python:3.12-slim


#Set the working directory for any subsequent ADD, COPY, CMD, ENTRYPOINT, or RUN instructions that follow it in the Dockerfile
WORKDIR /workdir_path


#copy files from the current directory to the docker workdir    
COPY . .


#Define the network ports that this container will listen on at runtime
EXPOSE 5000

#rovide defaults for an executing container
CMD ["python","app"]
