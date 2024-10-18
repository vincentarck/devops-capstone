# frontend/Dockerfile

# Menggunakan image Node.js sebagai base
FROM node:18 AS builder

# Set working directory
WORKDIR /app

# Clone app project
RUN git clone https://github.com/rishabkumar7/devops-qr-code.git

# Pindah ke direktori api
WORKDIR /app/devops-qr-code/front-end-nextjs

# Menginstal dependensi
RUN npm install

# Membangun aplikasi Next.js
RUN npm run build

# Menggunakan image Node.js untuk server
FROM node:18

# Set working directory
WORKDIR /app

# Menyalin hasil build dari stage sebelumnya
COPY --from=builder /app/devops-qr-code/front-end-nextjs ./

# Menjalankan aplikasi
CMD ["npm", "start"]

# Mengekspos port
EXPOSE 3000