# 🏫 TLU-LabBook - Hệ thống Quản lý & Đặt phòng Tự học / Phòng Lab

**TLU-LabBook** là nền tảng web hỗ trợ sinh viên và giảng viên Trường Đại học Thủy Lợi (TLU) tra cứu trạng thái phòng trống theo thời gian thực, đặt lịch sử dụng phòng tự học/phòng thực hành nhanh chóng và minh bạch.

---

## ✨ Tính năng chính

### 👨‍🎓 Dành cho Sinh viên / Giảng viên
* **Tra cứu trực quan:** Xem danh sách phòng, sức chứa, trang thiết bị (máy chiếu, điều hòa, PC) và lịch trống theo ngày/giờ.
* **Đặt phòng nhanh chóng:** Chọn khung giờ sử dụng, hệ thống tự động kiểm tra và ngăn chặn đặt trùng lịch.
* **Check-in thông minh:** Nhận mã QR và Email xác nhận ngay sau khi đặt lịch thành công.
* **Quản lý cá nhân:** Theo dõi lịch sử đặt phòng và chủ động hủy lịch nếu thay đổi kế hoạch.

### 🛠️ Dành cho Quản trị viên (Admin / Cán bộ quản lý)
* **Quản lý tài nguyên:** Thêm, sửa, xóa thông tin phòng học và cập nhật trạng thái bảo trì.
* **Kiểm soát lịch đặt:** Phê duyệt hoặc từ chối các yêu cầu đặt phòng đặc biệt.
* **Chống đặt chỗ ảo:** Hệ thống tự động giải phóng phòng nếu người đặt không check-in sau 15 phút.
* **Thống kê:** Xem báo cáo tần suất sử dụng phòng theo tuần/tháng.

---

## 🚀 Công nghệ sử dụng (Tech Stack)

* **Frontend:** ReactJS (Vite), Tailwind CSS, Axios
* **Backend:** PHP 8.2, Laravel 11 (RESTful API)
* **Database:** PostgreSQL (Hosted on Neon/Supabase)
* **Deployment:** Vercel (Frontend) & Render (Backend)

---

## 👥 Thành viên nhóm thực hiện

| Họ và tên | Mã sinh viên | Vai trò (Role) | GitHub |
| :--- | :--- | :--- | :--- |
| Nguyễn Văn A | 215106xxxx | Project Manager / BA / UI | `@username-pm` |
| Trần Thị B | 215106xxxx | Backend Developer | `@username-be` |
| Lê Văn C | 215106xxxx | Frontend Developer | `@username-fe` |
| Phạm Thị D | 215106xxxx | QA / Tester / Docs | `@username-qa` |

---

## ⚙️ Hướng dẫn cài đặt môi trường Local

### 1. Cài đặt Backend (Laravel)
```bash
cd backend
composer install
cp .env.example .env
# Cập nhật thông số kết nối PostgreSQL (DB_CONNECTION=pgsql) trong file .env
php artisan key:generate
php artisan migrate --seed
php artisan serve
```

### 2. Cài đặt Frontend (React)
```bash
cd frontend
npm install
cp .env.example .env
# Cập nhật VITE_API_URL=http://localhost:8000/api trong file .env
npm run dev
```

---

## 📅 Lộ trình phát triển (4 Tuần)
* **Tuần 1:** Khởi tạo dự án, phân tích nghiệp vụ, thiết kế DB & UI/UX.
* **Tuần 2:** Xây dựng hệ thống xác thực (Auth) và quản lý danh mục phòng.
* **Tuần 3:** Phát triển luồng đặt lịch, xử lý trùng giờ, tạo mã QR và gửi Email.
* **Tuần 4:** Kiểm thử toàn diện, sửa lỗi, triển khai lên Cloud và hoàn thiện báo cáo.
