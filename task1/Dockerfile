FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y

# Install Python and pip
RUN apt-get install -y python3 python3-pip

# Fix externally-managed environment issue (IMPORTANT)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy your API file
COPY ./api.py /app/api.py

# Run the Flask app
CMD ["python3", "api.py"]