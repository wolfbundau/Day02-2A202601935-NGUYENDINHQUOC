# 01 — Individual Problem Scan & Top 3 Problem Cards

> **Học viên:** Nguyễn Đình Quốc  
> **Mã học viên:** 2A202601935  
> **Bối cảnh / Vai trò:** Sinh viên / Học viên ngành CNTT & AI  

---

## 1. Danh sách Scan Vấn Đề (Problem Scan Table)

Dưới đây là 10 bài toán/vấn đề thực tế quan sát được từ quá trình học tập, làm bài tập nhóm và xây dựng dự án AI:

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (Bottleneck / Data) |
|---|---|---|---|---|
| 1 | **Lặp lại** | Tìm lại quyết định, link tài liệu, bài tập mẫu bị trôi trong kênh Chat Discord / Zalo của lớp | Học viên, Thành viên nhóm | Mất 15-20 phút/lần tìm; 3-4 lần/tuần bị hỏi trùng câu hỏi cũ. |
| 2 | **Tốn thời gian** | Đọc và tóm tắt bài báo khoa học (Research Paper/ArXiv) 15-20 trang để làm tổng quan tài liệu (Literature Review) | Sinh viên AI, Nghiên cứu sinh | Mất 2-3 tiếng/bài; dễ nản hoặc bỏ sót insight cốt lõi. |
| 3 | **AI có thể tốt hơn** | Kiểm tra tự động cấu trúc bài nộp (Checklist, file thiếu, sai format) trước khi push lên Git nộp bài | Học viên | Mất 15 phút soi thủ công nhưng vẫn hay bị trừ điểm trễ/thiếu file. |
| 4 | **Pain từ người khác** | Thành viên nhóm không nắm rõ task/deadline cá nhân do phân công việc rải rác trong tin nhắn | Cả nhóm đồ án (3-4 người) | 2-3 lần/tuần phải hỏi lại "Ai làm phần này?"; hay bị delay sát giờ nộp. |
| 5 | **Tốn thời gian** | Debug lỗi xung đột môi trường (CUDA, PyTorch, Python version mismatch) khi chạy code mẫu | Sinh viên, Dev mới | Mất 1-2 tiếng/lần search StackOverflow mà không rõ nguyên nhân gốc. |
| 6 | **Lặp lại** | Viết file README.md & Hướng dẫn cài đặt (Setup Instruction) cho repo đồ án nhóm | Thành viên phụ trách Git | Mất 30-45 phút/repo để gõ lại các bước setup môi trường lặp đi lặp lại. |
| 7 | **Pain từ người khác** | Học viên mới liên tục chụp ảnh hỏi lỗi cài đặt phần mềm/công cụ cơ bản trên group chung | Mentor, TA, Học viên cũ | Trả lời lặp đi lặp lại cùng một câu hỏi 5-7 lần/tuần. |
| 8 | **Tốn thời gian** | Tổng hợp feedback từ Giảng viên/Mentor sau buổi Review đồ án thành danh sách Action Items | Trưởng nhóm đồ án | Mất 45 phút nghe lại ghi âm/xem lại note để chốt danh sách cần sửa. |
| 9 | **AI có thể tốt hơn** | Chuyển đổi sơ đồ phác thảo tay (Mindmap/Flowchart trên giấy) thành mã Mermaid/Diagram số | Sinh viên thiết kế workflow | Mất 30-40 phút gõ lại Mermaid thủ công. |
| 10 | **Lặp lại** | Format lại code, chuẩn hóa docstring & comment theo chuẩn PEP8 trước khi nộp bài | Sinh viên lập trình | Mất 20 phút/bài nộp làm công việc format thủ công. |

---

## 2. Lựa chọn Top 3 Problem Cards

| Rank | Problem | Vì sao chọn (Impact & Feasibility) | Điều còn chưa chắc (Uncertainty) |
|---|---|---|---|
| **1** | **Search & Tổng hợp quyết định bị trôi trên Discord** | Tần suất cao (hằng ngày), ảnh hưởng cả lớp/nhóm, tốn thời gian tìm kiếm lặp đi lặp lại. | Quyền truy cập API/Export data từ Discord; bảo mật thông tin nội bộ. |
| **2** | **Tóm tắt & Trích xuất insight từ Research Paper AI dài** | Pain rất lớn khi làm đồ án/nghiên cứu, tốn nhiều công sức đọc hiểu tiếng Anh chuyên ngành. | AI dễ bị ảo giác (hallucination) với công thức toán hoặc thông số kĩ thuật. |
| **3** | **Tự động kiểm tra Checklist & Cấu trúc bài nộp Git** | Giúp giảm lỗi ngớ ngẩn (thiếu file, sai đặt tên), tăng tỉ lệ pass bài ngay từ lần đầu. | Cần định nghĩa rule kiểm tra linh hoạt cho từng môn học/đợt nộp. |

---

## 3. Chi tiết Top 3 Problem Cards & Workflow

### 📌 Problem Card #1: Tra cứu & Tổng hợp kiến thức/quyết định trôi trên Discord (TOP 1)

* **Problem 1 câu:** Học viên mất nhiều thời gian lục lại tin nhắn Discord để tìm link bài học, thông báo deadline hoặc quyết định của nhóm, dẫn đến trả lời lặp lại và bỏ sót thông tin.
* **Actor:** Học viên trong khóa học AI / Thành viên nhóm đồ án.
* **Thời điểm / Bối cảnh:** Khi bắt đầu làm bài tập, cần xem lại hướng dẫn của giảng viên hoặc quyết định phân công của nhóm.
* **Current Workflow:**
  1. Mở Discord -> Chọn channel liên quan.
  2. Dùng thanh Search của Discord gõ từ khóa.
  3. Cuộn qua hàng chục tin nhắn kết quả để tìm đúng ngữ cảnh.
  4. Nếu không thấy, nhắn tin hỏi lại trên channel chung.
  5. Chờ giảng viên / bạn học trả lời (mất từ 15 phút đến vài tiếng).
* **Bottleneck:** Lục tìm tin nhắn thủ công mất thời gian và phụ thuộc vào thời gian phản hồi của người khác.
* **Impact:** Mất khoảng 60-90 phút/tuần cho mỗi học viên; giảng viên/TA bị phiền vì trả lời cùng 1 câu hỏi nhiều lần.
* **Success Metric:** Giảm thời gian tìm thông tin từ 15 phút xuống dưới 2 phút; giảm 70% câu hỏi lặp lại trên kênh chung.
* **Non-AI Alternative:** Tạo file Notion/Pinned Messages để lưu link quan trọng (tuy nhiên mọi người vẫn quên cập nhật hoặc quên vào xem).
* **AI Hypothesis:** Trợ lý AI tích hợp Discord RAG (Retrieval-Augmented Generation) tự động quét tin nhắn/pin, index dữ liệu và trả lời ngay kèm link nguồn.

#### Draft Current Workflow vs. Future Workflow (Problem #1)

```text
CURRENT WORKFLOW (Thủ công - 15-20 phút/lần):
[Học viên cần tìm info] ──> [Search từ khóa Discord] ──> [Cuộn tìm tin nhắn cũ] ──> [Không thấy] ──> [Hỏi trên group] ──> [Chờ phản hồi]

FUTURE WORKFLOW (Hỗ trợ AI - < 2 phút/lần):
[Học viên cần tìm info] ──> [Hỏi AI Bot / Search Semantic] ──> [AI trích xuất câu trả lời + dẫn nguồn tin nhắn Discord] ──> [Học viên xác nhận & làm tiếp]
```

---

### 📌 Problem Card #2: Tóm tắt & Trích xuất insight từ Research Paper AI (TOP 2)

* **Problem 1 câu:** Nghiên cứu sinh tốn thời gian để tìm kiếm các bài báo liên quan từ nhiều nguồn khác nhau và thêm nhiều tiếng để đọc bài báo nhưng khó nắm bắt nội dung bài báo.
* **Actor:** Sinh viên, Nhà nghiên cứu đang tìm kiếm bài báo phù hợp.
* **Thời điểm / Bối cảnh:** Giai đoạn tìm tài liệu tham khảo để chọn phương pháp thực hiện dự án.
* **Current Workflow:**
  1. Lên Google Scholar, connectedpapers hay litmaps để tìm kiếm những bài báo liên quan đến chủ đề đang quan tâm. 
  2. Tải file PDF từ ArXiv/Google Scholar, tạp chí/hội nghị tương ứng.
  3. Đọc hiểu bài báo, phương pháp & thử nghiệm, tra từ điển/thuật ngữ (120 phút).
  4. Ghi chú thủ công vào file Notion/Word (30 phút).
  5. So sánh các bài báo liên quan với nhau (20 phút).
* **Bottleneck:** Bước đọc hiểu chi tiết & tổng hợp kết quả giữa các bài báo khác nhau cực kỳ tốn thời gian (lên đến nhiều giờ).
* **Impact:** 2-3 tiếng/bài báo. Ảnh hưởng tới tiến độ đề xuất giải pháp cho nghiên cứu.
* **Success Metric:** Rút ngắn thời gian đọc & nắm ý chính 1 bài báo từ 150 phút xuống 40 phút.
* **Non-AI Alternative:** Đọc bản tóm tắt của blog/review có sẵn hoặc đọc nhanh abstract (nhưng nhiều bài mới chưa ai viết review hoặc abstract quá chung chung).
* **AI Hypothesis:** AI tìm bài báo phù hợp, đọc file PDF, trích xuất bảng so sánh (Architecture, Dataset, Baseline, Metrics) và cho phép hỏi đáp trực tiếp trên tài liệu.

```text
CURRENT WORKFLOW(Đọc thủ công - 2-3h/bài)
[Tìm bài báo] ──> [Đọc lướt] ──> [Đọc chi tiết] ──> [Ghi chú thủ công] ──> [So sánh thủ công] 

FUTURE WORKFLOW (Hỗ trợ AI - < 30 phút/bài):
[Tìm bài báo tự động] ──> [AI tóm tắt bài báo] ──> [AI trích xuất bảng so sánh + cho phép hỏi đáp]
```

### 📌 Problem Card #3: Kiểm tra tự động cấu trúc bài nộp & Checklist trước khi push Git (TOP 3)

* **Problem 1 câu:** Học viên hay nộp thiếu file, sai cấu trúc thư mục hoặc thiếu checklist dẫn đến bị trừ điểm ngớ ngẩn.
* **Actor:** Học viên nộp bài tập lớn / bài lab.
* **Thời điểm / Bối cảnh:** Trước deadline nộp bài 30 phút.
* **Current Workflow:**
  1. Hoàn thành bài làm.
  2. Đọc file hướng dẫn README/Rubric.
  3. Mở cây thư mục đối chiếu từng file/thư mục thủ công.
  4. Git commit & push.
* **Bottleneck:** Dễ bỏ sót file ẩn, sai định dạng tên file, hoặc quên chưa hoàn thiện hết các section trong worksheet.
* **Impact:** Bị trừ 10-20% điểm do lỗi quy cách nộp bài.
* **Success Metric:** 100% bài nộp đúng cấu trúc thư mục và không thiếu file bắt buộc.
* **Non-AI Alternative:** Dùng script bash/python linter kiểm tra sự tồn tại của file (File existence check).
* **AI Hypothesis:** AI/Rule Linter quét file Markdown, kiểm tra nội dung từng section đã được điền đủ chưa (không chỉ kiểm tra file có tồn tại hay không).
```text
CURRENT WORKFLOW(Kiểm tra thủ công - 10-15 phút/lần)
[Hoàn thành bài] ──> [Đọc README/Rubric] ──> [Kiểm tra thủ công từng file]

FUTURE WORKFLOW (Hỗ trợ AI - < 2 phút/lần):
[Hoàn thành bài] ──> [Hỏi AI Bot] ──> [AI quét và báo lỗi cấu trúc/thiếu]
```
