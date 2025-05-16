# Laravel Project - Chạy bằng Docker không cần cài đặt gì thêm

## 🔰 Giới thiệu

Dự án Laravel này được cấu hình sẵn bằng Docker. Bạn **KHÔNG CẦN CÀI** bất kỳ công cụ nào như:
- XAMPP
- MySQL
- PHP
- Laravel

Toàn bộ đã được đóng gói, chỉ cần cài **Docker Desktop**, giải nén mã nguồn và làm theo hướng dẫn bên dưới là có thể chạy được.

---

## ✅ Yêu cầu duy nhất

### 1. Cài đặt Docker Desktop
- Tải và cài đặt Docker tại:  
  👉 [https://docs.docker.com/desktop/setup/install/windows-install](https://docs.docker.com/desktop/setup/install/windows-install)
- Sau khi cài đặt xong, **khởi động lại máy tính** để đảm bảo Docker hoạt động tốt.

---

## 📦 Các bước chạy dự án

### 2. Giải nén mã nguồn

Giải nén file source code vào một thư mục bất kỳ.

---

### 3. Xóa file `storage` lỗi

- Mở thư mục `myproject/public`
- Xóa file `storage` (thường là một shortcut 0KB)

---

### 4. Tạo symbolic link

Mở Terminal hoặc CMD ngay tại thư mục gốc chứa project (chứa file `docker-compose.yml`) và chạy:

```bash
docker exec -u root -it laravel-app php artisan storage:link


## 5. 🐳 Build và khởi động Docker

### ⏱ Nếu bạn **chưa từng build** lần nào, chạy lệnh:

```bash
docker compose up --build
