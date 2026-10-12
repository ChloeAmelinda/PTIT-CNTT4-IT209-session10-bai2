# Bài 3: Single-stage Dockerfile

## 1. Mục tiêu
Đóng gói ứng dụng REST API Node.js/Express bằng Docker Single-stage.

## 2. Công nghệ
- Node.js 18 Alpine
- Express.js
- Docker

## 3. Cấu trúc dự án
- Dockerfile
- package.json
- server.js
- .dockerignore
- README.md

## 4. Build Docker Image
docker build -t hw-backend:v1 .

## 5. Chạy Docker Container
docker run -d --name app-single-stage -p 8080:3000 hw-backend:v1

## 6. Kiểm tra
docker ps
docker logs app-single-stage
curl.exe -i http://localhost:8080/

## 7. Kết quả mong đợi
- Docker Image build thành công.
- Container có trạng thái Up.
- API trả về HTTP 200 OK.
- Response JSON:

{"status":"success","message":"Hello from Docker Single-stage!"}

## 8. Ghi chú
Ứng dụng sử dụng Single-stage Dockerfile và chạy trên cổng 3000 trong container.
Cổng 8080 của máy host được ánh xạ đến cổng 3000 của container.
