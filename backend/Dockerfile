# Use official Python image as base
FROM python:3.12-slim

# Set working directory
WORKDIR /backend/app

# Copy requirements.txt and install dependencies
COPY requirements.txt ./requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the backend app code
COPY ./app /backend/app

# Set environment variable for FastAPI
ENV PYTHONUNBUFFERED 1

# Expose FastAPI port
EXPOSE 8000

# Command to run FastAPI app with Uvicorn
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
