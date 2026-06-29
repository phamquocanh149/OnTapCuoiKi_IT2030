# 📝 Hệ Thống Ôn Tập Trắc Nghiệm IT2030 (Technical Writing and Presentation)

Ứng dụng web chạy offline dạng Single Page Application (SPA) hỗ trợ ôn thi trắc nghiệm học phần **Technical Writing and Presentation (IT2030)** - Đại học Bách Khoa Hà Nội (HUST). 

Ứng dụng được xây dựng hoàn toàn bằng **HTML, CSS và JavaScript thuần**, không cần cài đặt hay cấu hình máy chủ, giúp sinh viên có thể ôn tập mọi lúc, mọi nơi trực tiếp trên trình duyệt.

---

## ✨ Tính Năng Nổi Bật (Key Features)

### 1. Bộ câu hỏi cập nhật đầy đủ (109 câu)
* * Tích hợp sẵn bộ câu hỏi từ đề thi cuối kì các năm của học phần được tổng hợp trong file JSON (`MC_tonghop.json`).
* Mỗi câu hỏi hỗ trợ song ngữ (Đề bài tiếng Anh kèm bản dịch nghĩa và giải thích chi tiết bằng tiếng Việt).

### 2. Hai chế độ học tập linh hoạt (Flexible Modes)
* **Tự Luyện Tập (Practice Mode):**
  * Tự do chọn câu hỏi từ danh sách.
  * Hiển thị đáp án đúng/sai ngay lập tức sau khi chọn.
  * Xem giải thích chi tiết đáp án và bản dịch tiếng Việt tương ứng.
* **Thi Thử (Test Mode):**
  * Tùy chỉnh số lượng câu hỏi thi thử (ví dụ: 10, 20, 50 hoặc toàn bộ 109 câu).
  * Làm bài không hiển thị đáp án trước khi nộp.
  * Thống kê kết quả trực quan bằng biểu đồ tròn (Score Gauge Canvas/SVG) và hiệu ứng pháo hoa chúc mừng (Confetti) khi đạt điểm tuyệt đối.
  * Xem lại chi tiết từng câu sai/đúng sau khi nộp bài.

### 3. Công cụ hỗ trợ ôn thi thông minh
* **Đánh dấu câu hỏi cần lưu ý (Flagging):** Cho phép gắn cờ màu vàng (`⚑`) cho các câu khó, câu dễ nhầm lẫn để tiện theo dõi và kiểm tra lại từ bảng điều khiển bên trái.
* **Xáo trộn câu hỏi (Shuffle):** Thay đổi ngẫu nhiên thứ tự câu hỏi để tránh học vẹt.
* **Điều hướng thông minh:**
  * Bảng lưới câu hỏi (Sidebar Navigation Grid) phản ánh trực quan trạng thái câu hỏi (Đang làm, Đã chọn đáp án, Đúng, Sai, Đã đánh dấu).
  * Hỗ trợ chuyển câu hỏi nhanh bằng phím mũi tên bàn phím: Mũi tên trái `←` (Quay lại) và Mũi tên phải `→` (Tiếp theo).

### 4. Giao diện hiện đại & Premium
* Giao diện tối (Dark Mode) mặc định kết hợp hiệu ứng kính (Glassmorphism), viền phát quang (Glow effect) và các chuyển động mượt mà (Micro-animations).
* Hỗ trợ chuyển đổi giao diện Sáng/Tối (Light/Dark Theme) nhanh gọn bằng nút Sun/Moon và tự động lưu trạng thái lựa chọn của bạn qua `localStorage`.

---

## 🚀 Hướng Dẫn Sử Dụng (How to Use)

### Cách chạy ứng dụng
1. Tải file `OnTapMCQ_IT2030.html` về máy tính của bạn.
2. Click đúp chuột vào file để mở trực tiếp trên bất kỳ trình duyệt nào (Chrome, Edge, Firefox, Safari,...).
3. Không cần cài đặt phần mềm phụ trợ hay kết nối internet.

### Phím tắt điều hướng nhanh
* `ArrowRight (→)`: Đi tới câu tiếp theo.
* `ArrowLeft (←)`: Quay lại câu trước đó.

---

## 📂 Cấu trúc mã nguồn (Codebase Structure)

Ứng dụng được đóng gói trong một file đơn nhất `OnTapMCQ_IT2030.html` để dễ dàng chia sẻ và chạy offline:
```
├── OnTapMCQ_IT2030.html    # File mã nguồn HTML, CSS Layout & JS logic
└── README.md               # Hướng dẫn sử dụng
```

Dữ liệu câu hỏi được nhúng trực tiếp trong thẻ `<script>` ở biến `rawQuizData` dưới dạng cấu trúc JSON:
```json
{
  "Ques": "Why should you keep text to a minimum on slides?",
  "Ans": {
    "A": "So the focus is on you as the speaker",
    "B": "To make sure the audience can read everything you have to tell them",
    ...
  },
  "correct": "A",
  "explanation": {
    "question_vi": "Tại sao bạn nên giữ văn bản ở mức tối thiểu trên các slide?",
    "answers_vi": {
      "A": "...",
      ...
    },
    "reason": "Slide chỉ là công cụ hỗ trợ trực quan. Việc giảm thiểu chữ giúp..."
  }
}
```

---

## 🛠️ Yêu Cầu Hệ Thống (Requirements)
* Bất kỳ thiết bị nào có trình duyệt web hiện đại (Máy tính, Máy tính bảng, Điện thoại).
* Khuyến khích sử dụng trên PC/Laptop để có trải nghiệm lưới câu hỏi và bàn phím tốt nhất.

---

## ⚖️ Bản Quyền (License & Credit)
* **Bản quyền sản phẩm thuộc Phạm Quốc Anh - 202400030 - SOICT - HUST**
* Học phần Technical Writing and Presentation (IT2030) - Trường Công nghệ Thông tin và Truyền thông - Đại học Bách Khoa Hà Nội.
