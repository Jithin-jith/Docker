# Pulling base image from dockerhub 
FROM python:3.12-slim

#Execute any commands on top of the current image as a new layer and commit the results.
RUN pip install pandas numpy

#Set the working directory for any subsequent ADD, COPY, CMD, ENTRYPOINT, or RUN instructions that follow it in the Dockerfile
WORKDIR /workdir_path

#Create a user
RUN adduser jith

#Set the user name or UID to use when running the image in addition to any subsequent CMD, ENTRYPOINT, or RUN instructions that follow it in the Dockerfile
USER jith

#Set environment variables
ENV name=Jithin \
    age=31

#copy files from the current directory to the docker workdir    
COPY app.py /workdir_path/
COPY app2.py /workdir_path/

#Add files to the workdir (can also pull online files)
ADD CLI_commands.txt .

#Define the network ports that this container will listen on at runtime
EXPOSE 5000

#rovide defaults for an executing container
CMD ["python","app"]

#Adds metadata to an image
LABEL creator="jithin"