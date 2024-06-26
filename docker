# Use the official Python image from the Docker Hub
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /chatgpt

# Copy the requirements.txt file to the container
COPY requirements.txt .

# Install the dependencies
RUN pip install -r requirements.txt

# Copy the rest of the application code to the container
COPY . .

# Expose the port that Streamlit runs on
EXPOSE 8501

# Define the command to run the Streamlit application
CMD ["streamlit", "run", "chatgpt.py", "--server.port=8501", "--server.address=0.0.0.0"]
