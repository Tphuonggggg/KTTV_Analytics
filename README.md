# Analytics Platform - Nền tảng Trực quan hóa & Phân tích Dữ liệu KTTV Việt Nam

Nền tảng này tích hợp giao diện React + Tailwind CSS hiện đại và trợ lý AI cục bộ (Human-in-the-Loop) để phân tích dữ liệu Khí tượng Thủy văn (KTTV) 34 tỉnh thành Việt Nam năm 2026.

## 1. Cấu Trúc Thư Mục
- `frontend/` : Dự án Web React + Tailwind CSS (Vite).
- `backend/` : Dự án FastAPI Python (dành cho các giai đoạn phát triển tích hợp sau).

---

## 2. Hướng dẫn Khởi chạy & Build Web Frontend

Di chuyển vào thư mục Frontend:
```powershell
cd analytics_platform/frontend
```

### 2.1. Cài đặt các gói phụ thuộc (Dependencies)
```powershell
npm install
```

### 2.2. Chạy môi trường Phát triển (Development Local Server)
```powershell
npm run dev
```
Sau khi khởi chạy thành công, máy chủ phát triển cục bộ sẽ hoạt động tại địa chỉ:
👉 **[http://localhost:5173](http://localhost:5173)**
Mở trình duyệt và truy cập liên kết trên để sử dụng giao diện Dashboard.

### 2.3. Biên dịch sản phẩm (Build Production Bundle)
Khi cần đóng gói ứng dụng web để triển khai thực tế, chạy lệnh:
```powershell
npm run build
```
Lệnh này sử dụng Vite để tối ưu hóa, nén mã nguồn React/CSS/JS và xuất các file tĩnh chất lượng cao vào thư mục `dist/` sẵn sàng triển khai.

---

## 3. Các tính năng nổi bật của Frontend
- **Bản đồ sáp nhập tương tác**: Hiển thị bản đồ Việt Nam với 34 phân khu hành chính mới sau sáp nhập đã triệt tiêu đường biên giới nội bộ thừa. Hỗ trợ click lọc vùng, rê chuột hiển thị tooltip, kéo rê di chuyển (Pan) và phóng to/thu nhỏ (Zoom).
- **Bộ lọc động (Dynamic Filters)**: Các bộ lọc Khu vực, Tháng, Mùa ngay đầu Dashboard giúp KPIs lớn và biểu đồ cột lượng mưa tự động phản hồi dữ liệu tức thì.
- **Quy trình Human-in-the-Loop giả lập**: Upload tập dữ liệu mẫu -> Chat với AI -> AI sinh code -> Phê duyệt code -> Chạy code hiển thị log real-time -> Xem biểu đồ kết quả -> Lưu lịch sử phân tích.
