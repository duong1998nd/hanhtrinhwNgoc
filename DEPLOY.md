# Đưa hanhtrinhwNgoc lên GitHub Pages

Trang này là website tĩnh, không cần backend. Tính năng tải bài đọc tệp trong trình duyệt. PDF/DOCX cần tải thư viện đọc từ CDN khi dùng lần đầu; các tệp bài làm vẫn được xử lý cục bộ.

## Đăng lên GitHub

Repository `duong1998nd/hanhtrinhwNgoc` đã được tạo riêng tư. Sau khi tải các tệp dự án lên `main`, đổi visibility thành Public để website và mã nguồn có thể truy cập công khai.

1. Đảm bảo các tệp nằm ở gốc repository, trong đó có `index.html`, `style.css`, `app.js`, `course-weeks.js`, giáo trình Markdown/DOCX và workbook XLSX. Không tải thư mục `outputs` hoặc ảnh kiểm tra bố cục lên site.
2. Nếu tạo lại repository hoặc dùng Git cục bộ:

   ```bash
   cd KHOA_HOC_NANG_LUC_VAN_PHONG_360
   git init
   git add index.html style.css app.js course-weeks.js README.md DEPLOY.md Lo-trinh-Master-Word-Excel-24-tuan.md Lo-trinh-Master-Word-Excel-24-tuan.docx Workbook-thuc-hanh-Word-Excel.xlsx Nguon-hoc-mien-phi.md
   git commit -m "Create hanhtrinhwNgoc Word and Excel learning site"
   git branch -M main
   git remote add origin https://github.com/duong1998nd/hanhtrinhwNgoc.git
   git push -u origin main
   ```

3. Trong repository, mở **Settings → General → Danger Zone → Change repository visibility** và chọn Public.
4. Mở **Settings → Pages**.
5. Ở **Build and deployment**, chọn **Deploy from a branch**, nhánh `main`, thư mục `/(root)`, rồi bấm **Save**.
6. Sau khi Pages hoàn tất, địa chỉ là `https://duong1998nd.github.io/hanhtrinhwNgoc/`.

Repository và trang Pages sẽ công khai. Không đưa API key, bài làm cá nhân hoặc tài liệu riêng tư vào repository.

## Giới hạn hiện tại

- Bộ rà soát dựa trên từ khóa và cấu trúc văn bản, không gọi mô hình AI, không tự chấm độ đúng của công thức hay nội dung.
- Tiến độ được lưu trong `localStorage` của trình duyệt và thiết bị hiện tại.
- DOCX/PDF dùng thư viện CDN khi cần trích văn bản; chức năng này cần kết nối mạng. PDF scan không có lớp văn bản cần OCR trước.
