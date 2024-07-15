FROM python:3.8
LABEL maintainer="Katie Gamanji"

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install packages defined in the requirements.txt file
RUN cd techtrends && pip install -r requirements.txt

# Initialize the database with pre-defined posts
RUN python init_db.py

# Expose port 3111
EXPOSE 3111

# Command to run on container start
CMD [ "python", "app.py" ]
