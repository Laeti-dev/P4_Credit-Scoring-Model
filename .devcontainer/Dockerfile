FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Set the working directory
WORKDIR /workspace

# Install Python and pip
RUN apt-get update && \
  apt-get install -y python3 python3-pip

# Copy the requirements.txt file into the container
COPY ../requirements.txt .

# Copy the data directory into the container
COPY ../data .

# Install dependencies from requirements.txt
RUN pip install -r requirements.txt

# Install Jupyter Notebook
RUN pip install jupyter

# Expose port 8888 for Jupyter Notebook
EXPOSE 8888

# Run Jupyter Notebook
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
