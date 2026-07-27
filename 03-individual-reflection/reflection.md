# 03 — Individual Reflection (Bài Tự Đánh Giá Cá Nhân)

> **Học viên:** Nguyễn Đình Quốc  
> **Mã học viên:** 2A202601935  
> **Lớp / Khóa học:** AI Product Labs — Day 02  

---

## 1. Vai trò và đóng góp cá nhân trong làm việc nhóm

Trong buổi làm lab nhóm Day 02:
- **Vai trò:** Trưởng nhóm (Leader) & Người pitch ý tưởng.
- **Đóng góp chính:**
  - Thực hiện scan rộng 10 bài toán thực tế từ trải nghiệm học tập và làm đồ án AI.
  - Trình bày (pitch) bài toán *"Tóm tắt & Trích xuất insight từ Research Paper AI"* với nhóm, phân tích rõ bottleneck 90 phút đọc chi tiết và đưa ra baseline thời gian cụ thể.
  - Cùng nhóm xây dựng sơ đồ Workflow Before / After và thảo luận phân tích giữa các giải pháp Rule vs. Workflow vs. Agent.
  - Hoàn thiện tài liệu báo cáo nhóm (`group-report.md`) và tổng hợp kết quả lên repo cá nhân.

---

## 2. AI đã hỗ trợ gì trong quá trình làm bài?

- **Hỗ trợ mở rộng góc nhìn scan bài toán:** AI giúp gợi ý thêm các góc nhìn từ lăng kính "Pain từ người khác" và "Tốn thời gian" mà ban đầu tôi chưa nghĩ tới.
- **Hỗ trợ vẽ và chuẩn hóa Workflow:** AI giúp chuyển đổi các bước mô tả công việc thành sơ đồ dạng Mermaid và text-based trực quan, dễ so sánh giữa trạng thái hiện tại (Current State) và tương lai (Future State).
- **Hỗ trợ làm rõ Boundary và Success Metric:** AI đóng vai trò phản biện, chỉ ra những điểm chưa thực tế trong giả định ban đầu (ví dụ: nhắc nhở về rủi ro hallucination khi đọc số liệu trong PDF).

---

## 3. AI đã sai hoặc hời hợt ở đâu? Tôi đã tự sửa lại thế nào?

- **Điểm AI làm hời hợt / chưa đúng:**
  - Ban đầu khi hỏi AI về giải pháp, AI thường đưa ra câu trả lời rất chung chung kiểu *"Xây dựng một Trợ lý AI toàn năng tự động đọc và viết báo cáo nghiên cứu"* (Mức Agent quá rộng).
  - AI không tính tới rủi ro sinh viên bị phụ thuộc và giáo viên lo ngại sinh viên trích dẫn sai số liệu.
- **Cách tôi điều chỉnh bằng nhận định cá nhân:**
  - Tôi đã chủ động thu hẹp phạm vi (Scope): Không xây Agent tự động hoàn toàn mà chỉ dừng lại ở **Workflow trợ lý bóc tách dữ liệu có cấu trúc**.
  - Bổ sung rào chắn cứng (Boundary): Yêu cầu AI bắt buộc phải hiển thị **số trang và trích dẫn trực tiếp** từ file PDF gốc để sinh viên 1-click verify trước khi sử dụng.

---

## 4. Bài học lớn nhất rút ra sau Day 02 Lab

1. **"Tìm đúng bài toán trước khi nghĩ đến Solution":** Không nên vội vã chọn ngay "Xây Agent" hay "Xây Chatbot". Bài toán có giá trị phải bắt đầu từ một người dùng cụ thể (Actor), một quy trình hiện tại (Workflow) và một điểm nghẽn có con số đo lường thật (Bottleneck & Metric).
2. **"Rule/Workflow đôi khi tốt hơn Agent":** Không phải lúc nào giải pháp AI phức tạp nhất cũng là tốt nhất. Với bài toán bóc tách dữ liệu paper, một Workflow tuyến tính phối hợp giữa Rule (parse PDF) + AI (RAG extract) + Con người (Review) mang lại hiệu quả cao hơn và rủi ro thấp hơn nhiều so với một Agent tự do.
3. **Nếu làm lại buổi lab này, tôi sẽ thay đổi điều gì:**  
   Tôi sẽ dành thêm 15 phút để thực hiện khảo sát/phỏng vấn nhanh trực tiếp với ít nhất 2 bạn học viên khác trong lớp để thu thập thêm số liệu thời gian thực tế hơn nữa trước khi chốt Problem Statement.
