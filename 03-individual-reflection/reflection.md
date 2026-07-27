# 03 — Individual Reflection

**Họ và tên:** Hoàng Đức Anh  
**Mã học viên:** 2A202601223  
**Vai trò trong nhóm:** Fullstack Developer — Phụ trách vẽ Workflow trước/sau, đánh giá khả thi kỹ thuật và lập luận lựa chọn mức giải pháp.

---

## 1. Đóng góp của Đức Anh trong nhóm

| Hoạt động | Đức Anh đã làm gì? | Kết quả / Tác động |
|---|---|---|
| **Scan cá nhân** | Đưa ra 10 problems thực tế từ bối cảnh Fullstack Dev & Learner trong team 4 người. | Đóng góp 2 bài toán vào shortlist nhóm, tạo nguồn candidate phong phú. |
| **Pitch Problem Card** | Trình bày bài toán *Aggregator & Centralized Deadline Tracker* và *Daily Standup Reminder*. | Bài Deadline Tracker được nhóm đồng thuận chọn làm Candidate Problem chung. |
| **Research giải pháp** | Tìm hiểu các giải pháp/API sẵn có (Google Calendar API, Slack Events API, Notion Automation, Zapier Webhook). | Nhúp được pattern tốt: dùng Rule cho data có cấu trúc, AI cho text phi cấu trúc. |
| **Xây dựng Workflow** | Vẽ current state (7 bước, 15-30p) và future state (7 bước, ≤8p), chỉ ra 2 điểm nghẽn Discovery & Normalization. | Nhóm có sơ đồ workflow trước/sau rõ ràng làm căn cứ xác định điểm can thiệp AI. |
| **Rule / Workflow / Agent** | Lập luận chọn mức **Workflow** (kết hợp **Rule** để đồng bộ/lọc dữ liệu và **AI** trích xuất text), phản biện việc dùng **Agent**. | Nhóm thống nhất không làm Agent tự trị tràn lan, giữ Human Boundary trước mọi write action. |

---

## 2. Bảng dùng AI trong quá trình làm bài

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định cá nhân? |
|---|---|---|---|---|
| **Scan cá nhân** | Gợi ý thêm các vấn đề góc nhìn Fullstack Dev/Learner. | Giúp liệt kê thêm góc nhìn về setup environment, dataset search. | Gợi ý vài ý quá rộng ("Trợ lý AI quản lý dự án toàn năng"). | Loại bỏ các ý chung chung, chỉ giữ lại các problem có workflow và pain thật. |
| **Problem Card & Pitch** | Đóng vai "Skeptical PM" để phản biện Problem Card cá nhân. | Chỉ ra các metric thời gian và số lần sót deadline còn dựa trên tự ước lượng. | AI hay khen và vội vàng gợi ý "dùng Agent tự động hoá 100%". | Chỉnh lại metric thành giả thuyết cần đo 7 ngày baseline trước pilot. |
| **Research giải pháp** | Tìm các công cụ và pattern đã giải bài toán tương tự. | Gợi ý các công cụ như Zapier Paths, Slack Events API, Notion AI. | Trích dẫn một số claim tiết kiệm thời gian không có nguồn kiểm chứng. | Kiểm tra lại tài liệu API chính thức từ Google, Slack, Notion; bỏ số liệu không verify được. |
| **Rule / Workflow / Agent** | Nhờ AI phân tích rủi ro khi chọn giữa Rule, Workflow và Agent. | Làm rõ rủi ro bảo mật (data privacy) và rủi ro tác động ghi (write action risk). | AI đề xuất xây Agent có khả năng tự động tạo/sửa lịch và gửi mail. | Phản biện hạ cấp xuống **Workflow + Rule (Read-only + Human approval)** để đảm bảo an toàn. |

---

## 3. Bài học cá nhân

- **Problem tốt nhất:** Problem tốt nhất không phải là problem nghe "AI" nhất hay ngầu nhất, mà là problem có **workflow hiện tại rõ ràng, điểm nghẽn cụ thể, metric đo lường được và impact thực sự**.
- **Vai trò của Rule:** Không phải lúc nào cũng cần đến AI. Các bước lấy số liệu, sync API, lọc ngày giờ hay gộp trùng dùng **Rule / Script** vừa nhanh, tiết kiệm chi phí lại chính xác 100%. AI chỉ nên dùng ở bước xử lý ngôn ngữ tự nhiên phi cấu trúc.
- **Agent không phải là đích đến mặc định:** Không nên vội vàng làm Agent tự trị khi quy trình chưa chín chắn và rủi ro còn cao. Lựa chọn **Workflow với Human Boundary** (con người duyệt trước khi ghi) giúp kiểm soát 100% rủi ro tác động sai.
- **Nghiên cứu thị trường (Research Takeaway):** Các sản phẩm thành công trên thị trường đều tuân theo pattern: *Rule tự động lấy data $\rightarrow$ AI gợi ý/draft $\rightarrow$ Con người kiểm tra & phê duyệt*.

### Nếu làm lại:
```text
Tôi sẽ thực hiện time-log và ghi chép nhật ký 7 ngày thực tế ngay từ đầu để có baseline thời gian chính xác hơn, thay vì sử dụng con số tự ước lượng ban đầu (15–30 phút/ngày).
```

---

*Individual Reflection — Hoàng Đức Anh (Day 02 Lab)*
