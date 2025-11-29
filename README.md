
# 🤖 Báo cáo Bài tập nhóm Môn Trí tuệ Nhân tạo

**📋 Thông tin:**

* **📚 Môn học:** MAT3508 - Nhập môn Trí tuệ Nhân tạo  
* **📅 Học kỳ:** Học kỳ 1 - 2025-2026
* **🏫 Trường:** VNU-HUS (Đại học Quốc gia Hà Nội - Trường Đại học Khoa học Tự nhiên)  
* **📝 Tiêu đề:** Ứng dụng LLM trong hệ thống gợi ý phim.
* **📅 Ngày nộp:** 30/11/2025
* **📄 Báo cáo PDF:** 📄 [Liên kết tới báo cáo PDF trong kho lưu trữ này]  
* **🖥️ Slide thuyết trình:** 🖥️ [Liên kết tới slide thuyết trình trong kho lưu trữ này]  
* **📂 Kho lưu trữ:** 📁 

**👥 Thành viên nhóm:**

| 👤 Họ và tên      | 🆔 Mã sinh viên     | 🐙 Tên GitHub        | 🛠️ Đóng góp  |
|------------------|--------------------|----------------------|----------------------|
| Nguyễn Minh An      | 21002114          | anbit192           | Cách 1      |
| Nguyễn Hồng Phúc      | 21000414          | titto2906           | Cách 2      |
---

## 📑 Tổng quan cấu trúc báo cáo

### Chương 1: Giới thiệu
**📝 Tóm tắt dự án**
   - ✨ Ứng dụng LLM trong hệ thống gợi ý phim. Kết hợp tính năng của LLM với các phương pháp gợi ý truyền thống (Content-based, Colaborative-filtered)


**❓ Bài toán đặt ra**
   - 📌 Làm sao để tận dụng tối đa được khả năng hiểu ngữ nghĩa của LLM, nhằm hiểu rõ sở thích của người dùng hơn.
   - 📌 Xây dựng luồng gợi ý phim, lưu trữ lịch sử phim của user.

### Chương 2: Phương pháp & Triển khai
**⚙️ Phương pháp**
   - 🔍 Bao gồm hai phương pháp chính
     + Sử dụng LLM để vector hóa và đưa vào RS (Recommend system).
     + Sử dụng LLM để sinh tóm tắt và vector hóa rồi đưa vào RS (Recommend system).

**💻 Triển khai**
   - 🧩 Hệ thống:
      + Mongodb: Lưu trữ dữ liệu user (lịch sử xem phim, đánh giá)
      + FAISS: Vector database
      + LLM Model: gemini-2.0-flash
      + Embed model: text-embedding-004
      + Backend & Frontend: FastAPI & Streamlit
   - 🧩 Cấu trúc: Toàn bộ mã nguồn ở trong folder /code
      + .env.example: setup file môi trường
      + requirements.txt: Thư viện
      + run.bat/sh: Chạy FE và BE cho linux/window
      + data & output_index: các data & index vector sau khi xử lý 
      + src & notebook: Logic code (luồng chính và đánh giá)

### Chương 3: Kết quả & Phân tích
**📊 Kết quả & Thảo luận**
   - 📈 Hiện tại nhóm mới triển khai được luồng xử lý của cách 1.
   - 📈 Nhìn chung thì đã có thể gợi ý ra những phim tương tự với lịch sử xem của user.
   - 📈 Đánh giá chỉ số HR của cách 2 cao hơn cách 1 nhưng chi phí thực hiện embed dữ liệu lịch sử xem của user khá tốn kém, cần phải xem xét thêm.

### Chương 4: Kết luận
**✅ Kết luận & Hướng phát triển**
   - 🔭 Cải thiện, xem xét đánh giá thêm một vài mô hình LLM khác.
   - 🔭 Tối ưu prompt, trích xuất nhiều thông tin hữu ích hơn cho việc gợi ý.

### Tài liệu tham khảo & Phụ lục
**📚 Tài liệu tham khảo**
   - 🔗 Liu, Q., Zhao, X., Wang, Y., et al. (2025). Large Language Model Enhanced Recommender Systems: A Survey.
   - 🔗 Wu, L., Zheng, Z., Qiu, Z., et al. (2024). A Survey on Large Language Models for Recommendation.
   - 🔗 Wang, Q., Li, J., Wang, S., et al. (2024). Towards Next-Generation LLM-based Recommender Systems: A Survey and Beyond.
---

## 📝 Hướng dẫn nộp bài

### 📋 Yêu cầu

- **Định dạng:**  
   + 🖨️ Báo cáo phải được đánh máy, trình bày rõ ràng và xuất ra định dạng PDF (khuyến nghị dùng LaTeX).  
   + 🔁 Một bản báo cáo cần lưu trên kho GitHub của dự án, hai bản nộp trên Canvas (một cho giảng viên, một cho trợ giảng), và hai bản in (một cho giảng viên, một cho trợ giảng). Slide trình bày cũng thực hiện tương tự (không cần bản in slides).
- **Kho lưu trữ:** 📂 Bao gồm báo cáo PDF, slide, toàn bộ mã nguồn và tài liệu liên quan. Nếu vượt quá giới hạn dung lượng của GitHub, có thể tải lên Google Drive hoặc Dropbox và dẫn link trong tài liệu.
- **Làm việc nhóm:** 🤝 Cần ghi rõ đóng góp của từng thành viên trong nhóm.
- **Tài liệu hóa mã nguồn:**  
   + 🧾 Có bình luận giải thích rõ các thuật toán/phần logic phức tạp  
   + 🧪 Docstring cho hàm/phương thức mô tả tham số, giá trị trả về và mục đích  
   + 📘 File README cho từng module mã nguồn, hướng dẫn cài đặt và sử dụng  
   + 📝 Bình luận inline cho các đoạn mã không rõ ràng

### ✅ Danh sách kiểm tra trước khi nộp
- [X] ✅ Đánh dấu X vào ô để xác nhận hoàn thành  
- [ ] ✍️ Điền đầy đủ các mục trong mẫu README này  
- [ ] 📄 Hoàn thiện báo cáo PDF chi tiết theo cấu trúc trên  
- [ ] 🎨 Tuân thủ định dạng và nội dung theo hướng dẫn giảng viên  
- [ ] ➕ Thêm các mục riêng của dự án nếu cần  
- [ ] 🔍 Kiểm tra lại ngữ pháp, diễn đạt và độ chính xác kỹ thuật  
- [ ] ⬆️ Tải lên báo cáo PDF, slide trình bày và mã nguồn  
- [ ] 🧩 Đảm bảo tất cả mã nguồn được tài liệu hóa đầy đủ với bình luận và docstring  
- [ ] 🔗 Kiểm tra các liên kết và tài liệu tham khảo hoạt động đúng

### 🏆 Tiêu chí đánh giá Bài tập nhóm

Xem 📄 [Rubrics.md](Rubrics.md) để biết chi tiết về tiêu chí đánh giá bài tập nhóm, bao gồm điểm tối đa cho từng tiêu chí và mô tả các mức độ đánh giá (Xuất sắc, Tốt, Cần cải thiện).

### 📚 Liên kết hữu ích

- 📄 [Mẫu báo cáo](LaTeX%20Template/main-vi.tex) - Mẫu LaTeX để viết báo cáo  
- 📘 [Sổ tay dùng LaTeX](https://vietex.blog.fc2.com/blog-entry-516.html) - Hướng dẫn sử dụng LaTeX bằng tiếng Việt  
- 🔎 [Một số phương pháp tải bài báo khoa học](https://hoanganhduc.github.io/misc/m%E1%BB%99t-s%E1%BB%91-ph%C6%B0%C6%A1ng-ph%C3%A1p-t%E1%BA%A3i-b%C3%A0i-b%C3%A1o-khoa-h%E1%BB%8Dc/) - Hướng dẫn một số phương pháp tải bài báo khoa học  
- 📰 [AI Vietnam Blog](https://aivietnam.edu.vn/blog) - Blog với các bài viết về AI bằng tiếng Việt

---

*Mẫu cập nhật lần cuối: 🗓️ Tháng 7/2025*
