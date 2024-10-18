# api/Dockerfile

# Menggunakan image Python sebagai base
FROM python:3.9

# Set working directory
WORKDIR /app

# Clone app project
RUN git clone https://github.com/rishabkumar7/devops-qr-code.git

# Pindah ke direktori api
WORKDIR /app/devops-qr-code/api

# Menginstal dependensi
RUN pip install --no-cache-dir -r requirements.txt

# Menjalankan API
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "5000"]

# Mengekspos port
EXPOSE 5000