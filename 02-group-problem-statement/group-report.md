# 02 — Group Report: Tóm Tắt & Trích Xuất Insight Từ Research Paper AI

> **Tên nhóm:** Nhóm AI Product Lab 02  
> **Đề tài được chọn:** Tự động tóm tắt & trích xuất insight từ bài báo khoa học AI (Research Paper)  

---

## 1. Thành viên nhóm & Phân công vai trò

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|-----|-----------|-------------|--------------------|
| 1   | **Nguyễn Đình Quốc** | 2A202601935 | Đóng góp ý tưởng, pitching bài toán AI |
| 2   | **Đinh Tuấn Minh** | 2A202601892 | Nhà đầu tư, phát triển giải pháp |
| 3   | **Lưu Quang Linh** | 2A202601084 | Pitching bài toán, thiết kế trình bày |
| 4   | **Võ Duy Quang** | 2A202601268 | Nhà đầu tư, phân tích giải pháp |
| 5   | **Nguyễn Đức Thành** | 2A202601968 | Nhà đầu tư, đóng góp giải pháp |

---

## 2. Nhật ký hội tụ nhóm (Group Convergence Log)

### Ma trận đánh giá Candidates

Nhóm tiến hành pitch và chấm điểm 3 bài toán từ các thành viên theo thang điểm 1-5 (tiêu chí: Pain thật, Workflow rõ, Feasibility, Metric rõ):

| Bài toán Candidate | Người đề xuất | Bottleneck rõ | Baseline thời gian | Dễ validate | Khả thi trong Lab | Tổng điểm | Chọn? |
|---|---|---:|---:|---:|---:|---:|---|
| **1. Tra cứu tin nhắn trôi trên Discord** | Nguyễn Đình Quốc | 4 | 4 | 4 | 3 | 15/20 | Không chọn |
| **2. Tóm tắt & trích xuất Paper AI** | Nguyễn Đình Quốc | 5 | 5 | 5 | 4 | **19/20** | **CHỌN** |
| **3. Kiểm tra tự động checklist Git** | Nguyễn Văn A | 4 | 3 | 4 | 4 | 15/20 | Không chọn |

### Lý do nhóm quyết định chọn Bài toán #2 (Tóm tắt Paper AI):
- **Pain vô cùng lớn và phổ biến:** 100% thành viên nhóm và bạn học ngành AI đều tốn 2-3 tiếng/bài báo khi làm tổng quan tài liệu (Literature Review).
- **Workflow & Baseline cực kỳ rõ ràng:** Có các mốc thời gian đọc lướt, đọc sâu, tổng hợp và so sánh cụ thể.
- **Dễ kiểm chứng (Validation):** Có thể chạy thử ngay trên các file PDF thực tế từ ArXiv.
- **Rủi ro kiểm soát được:** AI làm nhiệm vụ draft tóm tắt và trích xuất bảng so sánh, sinh viên vẫn phải đọc lại và chịu trách nhiệm nội dung cuối.

### Lý do không chọn các bài toán khác:
- *Discord Search:* Vấn đề đau thật nhưng bị vướng quyền truy cập API/privacy dữ liệu Discord nội bộ, dễ kéo dài thành bài toán hạ tầng RAG quá lớn.
- *Checklist Git:* Dễ làm bằng Rule/Script đơn giản (File existence check), không phát huy hết sức mạnh của AI trong xử lý ngôn ngữ tự nhiên.

---

## 3. Kiểm chứng nhanh (Quick Validation)

Nhóm thực hiện phỏng vấn nhanh 4 bạn sinh viên AI / nghiên cứu sinh và 1 giảng viên hướng dẫn đồ án.

| Nguồn kiểm chứng | Đối tượng | Tín hiệu xác nhận (Pain thật) | Tín hiệu phản bác / Lo ngại | Nhóm điều chỉnh Problem |
|---|---|---|---|---|
| Phỏng vấn nhanh (3 SV AI) | Sinh viên năm 3-4 | Đều bỏ ra 10-15 tiếng/tuần chỉ để đọc paper; hay bị nản ở phần đọc công thức & phương pháp | Nếu AI tóm tắt quá ngắn sẽ bỏ mất thông số kỹ thuật quan trọng | Thu hẹp scope: AI không tóm tắt chung chung, mà trích xuất theo Bảng cấu trúc (Arch, Dataset, Baseline, Metric). |
| Phỏng vấn Giảng viên (1 Mentor) | Mentor đồ án | Sinh viên hay hiểu sai ý chính của bài báo hoặc trích dẫn sai thông tin | Rất sợ sinh viên phụ thuộc AI rồi "bịa" ra trích dẫn (hallucination) | Bổ sung Boundary cứng: AI phải dẫn link / trích dẫn số trang chính xác cho từng khẳng định. |

> **Key Insight sau validation:**  
> Pain không phải là "không muốn đọc paper", mà là **mất quá nhiều thời gian để sàng lọc và trích xuất thông tin cấu trúc** (Mô hình gì? Tập dữ liệu nào? Độ chính xác bao nhiêu?) trước khi quyết định có nên đọc sâu bài báo đó hay không.

---

## 4. Nghiên cứu giải pháp hiện có (Research)

Nhóm nghiên cứu các công cụ đã có trên thị trường để tìm ra khoảng trống (gap) và bài học:

| Tool / Case | Sản phẩm | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / Rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **ChatPDF** | https://www.chatpdf.com | Hỏi đáp trực tiếp trên 1 file PDF | Giao diện đơn giản, hỏi đáp linh hoạt | Chỉ làm từng file đơn lẻ, không so sánh được giữa nhiều bài báo với nhau | Dùng RAG trên single-file là chưa đủ, cần tính năng so sánh đa file |
| **SciSpace (Typeset)** | https://typeset.io | Tóm tắt paper, giải thích công thức | Có bảng so sánh các paper theo cột | Chi phí bản quyền cao, đôi khi trích xuất sai chỉ số thực nghiệm | Thiết kế output dạng bảng so sánh chuẩn hóa (Comparison Matrix) |
| **Consensus.app** | https://consensus.app | Search & tóm tắt câu trả lời từ nghiên cứu | Tìm kiếm bằng câu hỏi tốt | Chỉ trả lời câu hỏi Yes/No hoặc tóm tắt ngắn, thiếu chi tiết kỹ thuật | Cần giữ lại bối cảnh kỹ thuật (Hyperparameters, Model Architecture) |

> **Research Takeaway:**  
> Không cần tự làm lại một ChatPDF khác. Hướng đi đúng đắn là **Workflow hỗ trợ sinh viên**: Tải PDF $\rightarrow$ AI tự động trích xuất thành Bảng thông số kỹ thuật chuẩn hóa $\rightarrow$ AI draft bản tóm tắt $\rightarrow$ Sinh viên kiểm tra số liệu & quyết định dùng.

---

## 5. Workflow Trước vs. Sau (Workflow Before / After)

### Current State (Thủ công — 5 bước, 150-180 phút/bài báo)
```text
[1. Tìm & Tải PDF: 15'] 
└──> [2. Đọc lướt Abstract/Intro: 20'] 
     └──> [3. Đọc sâu 20 trang (Phương pháp & Thử nghiệm): 90']  <-- BOTTLENECK
          └──> [4. Ghi chú thủ công vào Notion/Word: 30'] 
               └──> [5. Lập bảng so sánh với các bài báo khác: 25']
```

### Future State (Hỗ trợ AI — 5 bước, 35 phút/bài báo)
```text
[1. Tải PDF vào hệ thống: 2']  -- (Thủ công)
└──> [2. AI Parser & Extract Bảng thông số: 3']  -- (Rule + RAG Workflow)
     └──> [3. AI Draft bản tóm tắt cấu trúc: 5']  -- (Prompt Workflow)
          └──> [4. Sinh viên Review, kiểm tra trích dẫn & Edit: 20']  -- (HUMAN BOUNDARY)
               └──> [5. Tự động xuất Bảng so sánh tổng hợp: 5']  -- (Auto-format)
```

### So sánh chỉ số Impact (Before vs. After)

| Metric | Trước (Thủ công) | Sau (Kỳ vọng AI) | Mức độ cải thiện |
|---|---:|---:|---|
| **Tổng thời gian xử lý 1 paper** | 180 phút | 35 phút | **Giảm 80% thời gian** |
| **Thời gian trích xuất thông số** | 90 phút | 3 phút | Giảm từ 1.5 tiếng xuống 3 phút |
| **Khả năng so sánh 5 paper** | 2-3 ngày | 2-3 tiếng | Tăng tốc độ làm Literature Review |
| **Bottleneck chính** | Đọc hiểu & ghi chú thủ công | Review & xác minh trích dẫn | Chuyển bottleneck sang khâu kiểm soát chất lượng |
| **Rủi ro chính** | Đọc sót ý do mệt mỏi | AI bị ảo giác (hallucination) | Kiểm soát bằng Human-in-the-loop review |

---

## 6. Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên ngành AI / Nghiên cứu sinh đang làm đồ án tốt nghiệp hoặc bài báo nghiên cứu. |
| **Workflow** | Tải PDF $\rightarrow$ Đọc lướt $\rightarrow$ Đọc sâu 20 trang $\rightarrow$ Ghi chú thủ công $\rightarrow$ So sánh thủ công. |
| **Bottleneck** | Đọc sâu 20 trang và tự bóc tách thông số kỹ thuật (Kiến trúc, Dataset, Metric) mất 90 phút/bài. |
| **Impact** | Tốn 15-20 tiếng/tuần; tiến độ nghiên cứu bị chậm; dễ bỏ sót bài báo quan trọng. |
| **Success Metric** | Giảm tổng thời gian đọc & bóc tách 1 paper từ 180 phút xuống dưới 40 phút. |
| **Boundary** | Không tự sáng tác số liệu không có trong PDF; bắt buộc chỉ rõ trang chứa thông tin. |

---

## 7. Phân tích & Chọn lựa cấp độ AI (Rule / Workflow / Agent)

| Mức độ | Phương án triển khai | Khi nào đủ? | Rủi ro / Hạn chế | Quyết định |
|---|---|---|---|---|
| **Rule** | Dùng regex/parser trích xuất mục Abstract, Conclusion, Reference | Chỉ đủ khi file PDF tuân thủ 100% định dạng IEEE/ACM cố định | Thất bại với 90% paper có layout cột khác nhau; không hiểu ngữ cảnh | Không chọn (chỉ dùng Rule cho bước phân giải PDF) |
| **Workflow** | Script phân giải PDF $\rightarrow$ RAG Prompt trích xuất theo Schema (Arch, Data, Metric) $\rightarrow$ AI Draft Tóm tắt $\rightarrow$ User Review & Verify | Hợp lý nhất vì workflow tuyến tính, AI tập trung vào việc đọc hiểu & tổng hợp | AI có thể hiểu sai thuật ngữ chuyên sâu $\rightarrow$ Cần User Review | **CHỌN (Phù hợp nhất)** |
| **Agent** | Agent tự lên ArXiv search keyword $\rightarrow$ tự chọn paper $\rightarrow$ tự đọc $\rightarrow$ tự viết chương Literature Review | Chỉ dùng khi muốn xây dựng hệ thống tự động nghiên cứu hoàn toàn | Quá phức tạp, nguy cơ agent chọn sai bài báo hoặc đi lạc đề rất cao | Chưa chọn (Scope quá lớn cho bài tập lab) |

> **Quyết định mức độ AI:** **Workflow**  
> *Lý do:* Quy trình bóc tách paper là quy trình từng bước rõ ràng. Chúng ta cần sự chính xác và kiểm soát của con người (Human-in-the-loop) thay vì để một Agent hoàn toàn tự do chạy.

---

## 8. Problem Statement v1 (Bản hoàn chỉnh)

| Field | Nội dung chi tiết |
|---|---|
| **Actor** | Sinh viên AI / Nghiên cứu sinh làm đồ án hoặc tổng quan nghiên cứu (Literature Review). |
| **Workflow** | Tải PDF $\rightarrow$ AI Extract thông số & Draft tóm tắt $\rightarrow$ Sinh viên Review & Verify $\rightarrow$ Xuất Bảng so sánh. |
| **Bottleneck** | Khâu đọc hiểu chi tiết 20 trang PDF và tự trích xuất số liệu thử nghiệm thủ công. |
| **Impact** | Mất 15-20 tiếng/tuần/người; làm chậm tiến độ đồ án và dễ gây nản lòng cho sinh viên. |
| **Success Metric** | Giảm tổng thời gian xử lý 1 paper xuống dưới **35 phút**; độ chính xác trích xuất thông số kỹ thuật đạt **> 90%**. |
| **Boundary** | - AI không được tự ý thêm số liệu ngoài file PDF.<br>- Mọi thông số trích xuất phải kèm **số trang & đoạn văn trích dẫn gốc** (Page & Citation).<br>- AI không tự ý viết phần kết luận đồ án thay cho sinh viên. |
| **Điểm can thiệp AI** | Ngay sau khi tải file PDF lên và trước bước Sinh viên viết báo cáo tổng quan. |
| **Mức AI chọn** | **Workflow** (Phân giải PDF $\rightarrow$ Prompt cấu trúc $\rightarrow$ Human Review $\rightarrow$ Auto-format Table). |
| **Rủi ro & Kiểm soát** | *Rủi ro:* AI trích xuất sai chỉ số Benchmark.<br>*Kiểm soát:* Giao diện hiển thị dạng 2 màn hình (Bên trái: PDF gốc highlighting trang trích dẫn, Bên phải: Bảng thông số do AI trích xuất) để sinh viên bấm 1-click verify. |

---

## 9. Quyết định cuối cùng (Final Decision)

```text
QUYẾT ĐỊNH: GO (Triển khai thử nghiệm với Scope hẹp)
```

### Kế hoạch Pilot nhỏ nhất (Minimum Viable Pilot):
1. **Scope thử nghiệm:** Thử nghiệm trên **10 bài báo ArXiv** thuộc chủ đề *Computer Vision / Large Language Models*.
2. **Công cụ sử dụng:** Python (PyMuPDF) + OpenAI GPT-4o / Claude 3.5 Sonnet với Structured Outputs (JSON Schema).
3. **Tiêu chí đánh giá thành công của Pilot:**
   - Trích xuất đúng 4 trường thông tin: *Model Architecture, Dataset, Primary Metric, Main Contribution* trên 9/10 bài báo.
   - Thời gian xử lý 1 bài báo < 2 phút (chưa tính thời gian người đọc review).
