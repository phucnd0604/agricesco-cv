# AGENTS.md — Quy Tắc & Hướng Dẫn Dành Cho AI Agent

Tài liệu này quy định các chuẩn mực, văn phong và quy trình kỹ thuật bắt buộc khi cập nhật hoặc chỉnh sửa kho mã nguồn CV cá nhân `agricesco-cv`.

---

## 🎯 1. Mục Đích & Định Hướng Dự Án

* **Vị trí ứng tuyển:** Chuyên viên Phát triển Phần mềm / Mobile Technical Leader tại Agriseco (Công ty Cổ phần Chứng khoán Agribank).
* **Ứng viên:** Nguyễn Đức Phúc (Sinh năm 1991, Kỹ sư Phần mềm ĐH FPT, 10+ năm kinh nghiệm).
* **Ngôn ngữ bắt buộc:** 100% Tiếng Việt.

---

## ✍️ 2. Quy Tắc Văn Phong & Trình Bày

1. **Văn phong Khiêm tốn - Trung thực - Điềm tĩnh:**
   * **KHÔNG** sử dụng từ ngữ phô trương, đao to búa lớn hoặc mang tính quảng cáo quá đà (Tránh các từ: *"Chuyên gia"*, *"Bảo mật tuyệt đối"*, *"Siêu việt"*, *"Bứt phá"*, *"Thần tốc"*...).
   * Trình bày công việc trung thực, tập trung vào nhiệm vụ thực tế và kết quả kỹ thuật chân thành (*"Tham gia phát triển...", "Phối hợp cùng BA/Backend...", "Đảm nhận vai trò trưởng nhóm kỹ thuật..."*).

2. **Tuyệt đối KHÔNG dùng Emoji:**
   * Loại bỏ 100% các icon/emoji (như 📍, 📞, ✉️, 🏆, 🛠️...) ở tất cả các định dạng file (`.html`, `.md`, `.pdf`).
   * Sử dụng typography, khoảng trắng, thẻ nhãn đậm (`<strong>`) và đường kẻ viền tối giản để tạo độ chỉn chu.

3. **Cấu trúc Header & Bảng:**
   * **Header:** Trình bày dạng 1 cột tối giản (Tên, Chức danh, Địa chỉ, SĐT, Email, Ngày sinh, Thể chất).
   * **Bảng Dự án tiêu biểu:** Chỉ giữ đúng **3 cột**: `Tên Dự Án` | `Lĩnh Vực & Vai Trò` | `Công Nghệ Sử Dụng` (Bỏ cột Kết quả/Đóng góp).

---

## 🔄 3. Quy Trình Đồng Bộ 3 Định Dạng & Xuất PDF

Mọi thay đổi nội dung CV bắt buộc phải được đồng bộ 100% trên cả 3 định dạng:

1. `index.html`: Bản giao diện web chính thức (chạy trên Vercel).
2. `CV_NguyenDucPhuc_Agriseco.html`: Bản HTML tĩnh dùng để xuất PDF.
3. `CV_NguyenDucPhuc_Agriseco.md`: Bản Markdown văn bản thuần (plain text).
4. `CV_NguyenDucPhuc_Agriseco.pdf`: File PDF xuất từ Headless Chrome CLI.

### Lệnh Xuất PDF Chuẩn (Bắt buộc dùng `--no-pdf-header-footer` để xóa file path ở footer & header):
```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf="CV_NguyenDucPhuc_Agriseco.pdf" file://$(pwd)/CV_NguyenDucPhuc_Agriseco.html
```

---

## 🚀 4. Trạng Thái Repository & Triển Khai

* **Trạng thái Repo:** `PUBLIC` (Bắt buộc giữ Public để Vercel Hobby Plan tự động build webhook không bị chặn).
* **Triển khai tự động:** Khi push commit mới lên nhánh `main` (`git push origin main`), Vercel sẽ tự động build và deploy lên web tức thì.
