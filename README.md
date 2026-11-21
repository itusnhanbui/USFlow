# USFlow — Quản lý Tiến độ Học tập Cá nhân (KHMT K2025 · FIT-HCMUS)

**USFlow** là ứng dụng web **Single-File** (HTML5, CSS3, JavaScript thuần) hỗ trợ sinh viên ngành **Khoa học Máy tính (Khóa tuyển 2025)** tại **Trường Đại học Khoa học Tự nhiên, ĐHQG-HCM (FIT-HCMUS)** theo dõi tín chỉ tích lũy, điểm trung bình (GPA), kế hoạch học tập 8 học kỳ, thời khóa biểu và điều kiện xét tốt nghiệp **100% ngoại tuyến (Offline-First)**[cite: 1, 2, 8].

---

## ✨ Tính năng nổi bật

* **Trang chủ & Hồ sơ học thuật:**
  * Chỉnh sửa thông tin cá nhân (Họ tên, MSSV, Avatar biểu tượng/ảnh tải lên) và tùy biến ảnh nền (Cover preset hoặc tải ảnh từ máy)[cite: 1].
  * Theo dõi tiến độ **138 tín chỉ chuyên môn** (Đại cương 56 TC, Cơ sở ngành 38 TC, Chuyên ngành 34 TC, Tốt nghiệp 10 TC) và **GPA hệ 4.0 / hệ 10.0** qua biểu đồ vòng tròn SVG[cite: 1, 2, 8].
  * Tách biệt và theo dõi **20 tín chỉ / điều kiện phụ** (GDTC 4 TC, GDQP-AN 4 TC, Ngoại ngữ / Chuẩn đầu ra) — **không tính vào 138 TC chuyên môn và không tính vào GPA**[cite: 1, 2, 8].
  * Theo dõi 3 điều kiện xét tốt nghiệp, học phí Portal và dữ liệu đồng bộ từ Portal[cite: 1].
* **Danh mục học phần & Chấm điểm trực tiếp:**
  * Hỗ trợ 5 định hướng chuyên ngành (`KHMT`, `CNTTriThuc`, `TGMT`, `ATTT`, `KHDL`) và 3 phương án tốt nghiệp (10 TC)[cite: 1, 2, 8].
  * Lọc theo khối kiến thức, học kỳ (`HK1`–`HK8`), trạng thái (`Đạt`, `Đang học`, `Chưa`, `Rớt môn`) và tìm kiếm theo mã/tên học phần[cite: 1].
  * Nhập điểm hệ 10 trực tiếp, tự động quy đổi điểm chữ (`A`, `B`, `C`, `D`, `F`) và điểm hệ 4 (`4.0`, `3.0`, `2.0`, `1.0`, `0.0`), kèm cửa sổ chỉnh sửa chi tiết từng môn[cite: 1, 2].
* **Lộ trình kéo–thả 8 học kỳ (Kanban):**
  * Kéo–thả học phần giữa các cột học kỳ (`HK1`–`HK8`) và khay **Chưa xếp** (hỗ trợ chọn nhiều thẻ bằng `Ctrl` / `Cmd` + nhấp)[cite: 1].
  * Cảnh báo tín chỉ vượt mốc 22 TC hoặc thấp hơn mốc tham khảo 14 TC/học kỳ (loại trừ môn điều kiện phụ khỏi giới hạn 22 TC)[cite: 1].
* **Thời khóa biểu tuần & Ngăn kéo sự kiện:**
  * Hỗ trợ 2 cơ sở **Linh Trung** (10 tiết) và **227 Nguyễn Văn Cừ** (15 tiết), kéo–thả/chạm để xếp lịch, kéo hoặc bấm nút để đổi số tiết, tự động phát hiện trùng tiết[cite: 1].
  * Ngăn kéo trượt bên phải (`‹`) quản lý nhanh **Lịch học tuần này**, **Đếm ngược lịch thi (GK/CK)** và **Danh sách việc cần làm (To-Do)**[cite: 1].
* **Công cụ mô phỏng & Định hướng:**
  * **Mô phỏng GPA (What-If):** Ước lượng GPA dự phóng và điểm cần đạt cho tín chỉ còn lại[cite: 1].
  * **Tính điểm cuối kỳ & Ước tính học phí:** Tính điểm thi cuối kỳ cần đạt theo trọng số và nhẩm tính học phí theo tín chỉ/đơn giá[cite: 1].
  * **Gợi ý chuyên ngành & Chuẩn đầu ra ELO 1–6:** Đánh giá mức độ phù hợp theo các môn nền tảng và tiến độ theo 6 nhóm ELO[cite: 1, 18].
* **Lưu trữ ngoại tuyến, Sao lưu JSON, Đồng bộ Portal & In bảng điểm:**
  * Tự động lưu vào `localStorage` (khóa chính `hcmus_khmt_k2025_progress`)[cite: 1, 8].
  * Xuất/nhập tệp sao lưu `.json` (`student_khmt_k2025.json`), hỗ trợ nhập dữ liệu từ HCMUS Portal (qua Bookmarklet/Clipboard/JSON) và mở trang bảng điểm in/xuất PDF khổ A4 ngang[cite: 1].
  * Giao diện **Sáng / Tối (Light / Dark Mode)** và tương thích cả Desktop lẫn Mobile ($\le 768\text{px}$)[cite: 1, 14].

---

## 🚀 Hướng dẫn khởi chạy & Sử dụng

Ứng dụng không cần cài đặt gói phụ thuộc hay máy chủ web[cite: 2, 7]:

1. Tải mã nguồn về máy (tệp `usflow_v1.html` — khi nộp bài có thể đổi tên thành `index.html` theo quy ước)[cite: 1, 16].
2. Mở trực tiếp tệp `.html` bằng trình duyệt web hiện đại (Chrome, Edge, Firefox, Safari)[cite: 4].
3. **Kiểm tra chế độ Offline:** Ngắt kết nối mạng (Wi-Fi/LAN), mở lại trang, cập nhật điểm hoặc trạng thái môn học, đóng trình duyệt và mở lại để xác nhận dữ liệu vẫn được giữ nguyên[cite: 4, 13].

---

## 💾 Cấu trúc dữ liệu & Lưu trữ

* **Lưu trữ cục bộ:** Dữ liệu trạng thái học tập, lịch học, lịch thi, công việc, cấu hình mô phỏng và tùy chọn giao diện được lưu dưới dạng JSON trong `localStorage` của trình duyệt[cite: 1, 2].
* **Lưu ý về ảnh đại diện & ảnh nền:** Khi tải ảnh từ thiết bị, ứng dụng nén ảnh qua `<canvas>` trước khi lưu vào `localStorage` để tiết kiệm dung lượng bộ nhớ trình duyệt[cite: 1].
* **Sao lưu & Khôi phục:** Sử dụng nút **Export JSON** để tải tệp sao lưu và **Import JSON** để khôi phục dữ liệu lên thiết bị hoặc trình duyệt khác[cite: 1, 8].

---

## 🛠️ Công nghệ sử dụng

* **HTML5**, **CSS3** (CSS Variables, Grid/Flexbox, Responsive, `@media print` / in bảng điểm)[cite: 1, 4, 15].
* **JavaScript (Vanilla JS)**, **SVG**, **Web Storage API (`localStorage`)**[cite: 1, 8, 15].
* Không phụ thuộc thư viện hay CDN bên ngoài trong quá trình vận hành giao diện[cite: 1, 13, 15].

---

## 📚 Tài liệu tham khảo

* Chương trình đào tạo đại học chính quy ngành Khoa học máy tính – Khóa tuyển 2025 (Trường Đại học Khoa học Tự nhiên, ĐHQG-HCM)[cite: 1, 2, 8].
* Quy chế đào tạo trình độ đại học và quy định học vụ liên quan của Trường Đại học Khoa học Tự nhiên, ĐHQG-HCM[cite: 8].
* Đề cương và hướng dẫn đồ án cuối kỳ môn **Nhập môn Công nghệ thông tin** – Khoa Công nghệ Thông tin, Trường Đại học Khoa học Tự nhiên, ĐHQG-HCM[cite: 8, 18].
