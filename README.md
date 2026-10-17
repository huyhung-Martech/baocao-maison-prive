# 📊 Maison Privée Ciputra - Báo Cáo Nghiên Cứu Thị Trường & Tình Báo Tên Miền

Dashboard trực quan hóa dữ liệu nghiên cứu thị trường bất động sản hàng hiệu (Branded Residences) và hệ thống tình báo tên miền thương hiệu cho dự án **Maison Privée Ciputra** (Tây Hồ, Hà Nội).

Trang dashboard Single-File thuần HTML5/Tailwind/Chart.js, không cần build. 

## 📁 Cấu trúc thư mục dự án
*   [`index.html`](index.html): Giao diện dashboard tích hợp toàn bộ:
    *   Báo cáo quy mô thị trường & phân khúc căn hộ siêu sang Ciputra Tây Hồ.
    *   Biểu đồ phân bổ nguồn cung, biến động đơn giá theo m² và chân dung khách hàng thượng lưu (UHNWI).
    *   Bảng ma trận tình báo tên miền (Domain Intelligence), kiểm tra trạng thái bảo hộ thương hiệu số của dự án.
    *   Bản đồ định vị đối thủ cạnh tranh lân cận trong bán kính 3km.

## 🎨 Thông tin thiết kế chính (Design System)
*   **Tông màu chủ đạo:**
    *   `Dark Indigo (#0F172A / #1E1B4B)`: Nền bảng điều khiển tối chuyên nghiệp, chuẩn phong cách phân tích tài chính/BI.
    *   `Luxury Violet (#6366F1 / #8B5CF6)`: Màu nhấn biểu đồ xu hướng thị trường và thẻ chỉ số North Star.
    *   `Amber Gold (#F59E0B)`: Điểm xuyết cho các chỉ số cảnh báo rủi ro tên miền và xếp hạng đối thủ top 1.
    *   `Card Slate (#1E293B)`: Nền thẻ chỉ số KPI giúp làm nổi bật số liệu và biểu đồ tương tác.
*   **Fonts:**
    *   Toàn bộ Dashboard: *Inter* (Google Fonts), hiển thị số liệu bảng biểu chính xác, rõ ràng.

## 🚀 Chạy thử
Mở trực tiếp [`index.html`](index.html) bằng bất kỳ trình duyệt nào, hoặc khởi chạy server cục bộ:

```bash
python -m http.server 8084
# rồi mở http://localhost:8084
```

## 📌 Hướng dẫn cập nhật số liệu mới

### 1. Cập nhật dữ liệu biểu đồ thị trường
*   Dữ liệu các biểu đồ (nguồn cung, mức giá, tỷ lệ hấp thụ) được cấu hình trực tiếp trong các đối tượng cấu hình `Chart.js` ở nửa sau của [`index.html`](index.html).
*   Chỉ cần thay đổi mảng `data: [...]` và nhãn `labels: [...]` tương ứng với kỳ báo cáo mới.

### 2. Cập nhật ma trận tình báo tên miền
*   Chỉnh sửa danh sách kiểm tra tên miền trong bảng dữ liệu: cập nhật tình trạng đăng ký, ngày hết hạn và mức độ ưu tiên thu hồi tên miền bảo hộ.

## 🖼️ Quy ước hiển thị & Xuất báo cáo
*   Dashboard hỗ trợ chế độ in ấn/xuất PDF trực tiếp từ trình duyệt (`Ctrl + P` hoặc `Cmd + P`).
*   Bố cục đã được tối ưu dạng Grid tự co giãn theo tỷ lệ màn hình máy tính và máy chiếu phòng họp.

## 🚢 Triển khai (Deploy)
Đẩy code lên nhánh `main` của repository để cập nhật bản báo cáo trực tuyến:

```bash
git push origin main
```
