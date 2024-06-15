FROM ubuntu:20.04

# Set the working directory
WORKDIR /app

# Copy the requirements file first for caching purposes
COPY requirements.txt /app/

# Copy the application files
COPY devops /app

# Update package lists
RUN apt-get update

# Install Python and pip
RUN apt-get install -y python3 python3-pip

# Install Python dependencies
RUN pip install -r requirements.txt

# Set the entry point and default command
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]