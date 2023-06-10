# Official Python base image
FROM python:3.9

# Environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Working directory in the container
WORKDIR /app

# Copying the requirements file
COPY requirements.txt .

# Installation of Python dependencies
RUN pip3 install -r requirements.txt \
    && pip3 install Pillow

# Copy the Django project code to the container
COPY . .

# Expose the port that Django runs on
EXPOSE 8000

# Run the Django development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
