# Use an official Python runtime as a base image
FROM python:3.12.4

# Set the working directory in the container
WORKDIR /app

# Copy project files into the container
COPY . /app

# Install required dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port Streamlit runs on
EXPOSE 5000

# Command to run the Streamlit app with a valid address
ENTRYPOINT ["streamlit", "run", "app.py", "--server.port=5000", "--server.address=0.0.0.0"]