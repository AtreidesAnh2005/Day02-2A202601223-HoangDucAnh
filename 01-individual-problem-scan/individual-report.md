# 01 — Individual Problem Scan

## Scan rộng

Tôi scan 10 problems, vượt mức tối thiểu 5.

| #  | Lăng kính          | Problem quan sát được                                                                                    | Ai chịu ảnh hưởng?         | Dấu hiệu thật                                                           |
| -- | ------------------ | -------------------------------------------------------------------------------------------------------- | -------------------------- | ----------------------------------------------------------------------- |
| 1  | Lặp lại            | Mỗi sáng learner phải nhớ viết daily standup trước 10h để không bị mất XP                                | Learner                    | Lặp lại hàng ngày; dễ quên khi bận hoặc dậy muộn                        |
| 2  | Lặp lại            | Mỗi lần bắt đầu lab mới đều phải clone repo, cài dependency, tạo environment và cấu hình biến môi trường | Learner, Developer         | Tốn nhiều thời gian setup; thường phát sinh lỗi dependency hoặc version |
| 3  | Lặp lại            | Hàng ngày phải kiểm tra deadline ở nhiều nơi như LMS, Calendar, Slack và Notion                          | Learner                    | Mất thời gian kiểm tra từng nền tảng; dễ bỏ sót deadline                |
| 4  | Tốn thời gian      | Đọc mô tả lab và assignment dài, có thể gồm 3-4 file hoặc hàng trăm trang                                | Learner                    | Khoảng 15 phút/file nếu muốn đọc hiểu và ghi nhớ                        |
| 5  | AI có thể tốt hơn  | Learner không biết nên học hoặc làm lab nào tiếp theo dựa trên kiến thức còn thiếu                       | Learner                    | Dễ chọn bài quá khó; mất thời gian quay lại học kiến thức nền           |
| 6  | Tốn thời gian      | Viết meeting notes sau meeting hoặc seminar sao cho ngắn gọn, đầy đủ và dễ nhớ                           | PM, Learner, Team member   | Khoảng 20 phút/buổi                                                     |
| 7  | AI có thể tốt hơn  | Tìm các dataset phù hợp và tương thích với một bài toán cụ thể                                           | Developer                  | Tốn ít nhất 30 phút để tìm, kiểm tra và tổng hợp dataset                |
| 8  | Pain từ người khác | Developer phải chờ quyền truy cập database, repository hoặc API key từ người khác                        | Developer, DevOps, Manager | Task bị block; phải nhắc lại nhiều lần; ảnh hưởng deadline              |
| 9  | Pain từ người khác | Member báo trạng thái “gần xong” nhưng không nói rõ phần còn thiếu hoặc blocker                          | PM, Team member            | PM phải hỏi lại nhiều lần; blocker thường được phát hiện muộn           |
| 10 | Pain từ người khác | Task hoặc assignment description mơ hồ, thiếu acceptance criteria và output mong đợi                     | Developer, Learner, PM     | Phải hỏi lại nhiều lần; dễ làm sai hoặc phải sửa lại                    |

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Daily Standup Reminder & Auto-Drafting (Problem #1) | Lặp lại hàng ngày, ảnh hưởng trực tiếp đến XP & động lực học tập, workflow rất rõ | Khả năng thu thập log tự động từ Git/LMS có mượt không |
| 2 | Tóm tắt & Trích xuất Yêu cầu Lab / Assignment (Problem #4) | Mất nhiều thời gian đọc (15-30p/file), dễ bỏ sót criteria quan trọng khi đọc lướt | Khó đo lường định lượng mức độ cải thiện chất lượng hiểu bài |
| 3 | Aggregator & Centralized Deadline Tracker (Problem #3) | Pain điểm thông tin rải rác nhiều kênh, rủi ro trễ deadline do trôi tin nhắn | Data access và API permission từ Slack/LMS/Calendar |

## Problem Card #1 — Daily Standup Reminder & Auto-Drafting (Problem #1)

**Problem 1 câu:**  
Mỗi sáng Learner phải nhớ tổng hợp công việc và viết daily standup trước 10h00 để giữ XP, vừa tốn thời gian nhớ lại công việc cũ vừa dễ quên khi bận hoặc dậy muộn.

**Actor:**  
Learner tham gia khóa học/bootcamp công nghệ có quy định tính điểm XP/chuyên cần bằng daily standup.

**Thời điểm / bối cảnh:**  
Mỗi buổi sáng từ 8h00 - 10h00 hằng ngày, trước deadline chốt XP của hệ thống.

**Current workflow:**
1. Mở LMS/Discord/Notion tìm kênh nộp standup hằng ngày
2. Mở Git commit log, lịch sử chat hoặc note cá nhân để nhớ lại các việc đã hoàn thành hôm qua
3. Viết recap nội dung công việc hôm qua, dự định hôm nay và các khó khăn (blocker)
4. Format nội dung theo đúng mẫu quy định (Yesterday / Today / Blockers)
5. Nộp bài lên kênh quy định trước 10h00

**Bottleneck:**  
Bước 2 & 3 — Mất khoảng 8-10 phút để lục lại trí nhớ và gom dữ liệu các việc đã làm hôm qua, dễ bị "trang giấy trắng" hoặc bỏ quên nộp bài khi buổi sáng có lịch bận đột xuất.

**Impact:**  
Mất khoảng 15 phút/ngày (~105 phút/tuần) cho 1 Learner. Khoảng 20-30% học viên từng bị mất XP hoặc bị nhắc nhở do quên nộp bài standup.

**Success metric:**  
Giảm tổng thời gian chuẩn bị & nộp standup từ 15 phút xuống dưới 3 phút; giảm tỷ lệ quên/trễ nộp standup xuống 0%.

**Non-AI alternative:**  
Đặt lịch hẹn giờ cố định (Google Calendar/Phone Alarm) lúc 9h00 sáng kết hợp template mẫu có sẵn trên Notion/Google Keep. (Giảm bớt quên nhưng chưa giải quyết được khâu nhớ lại và gom dữ liệu).

**AI hypothesis:**  
Hệ thống tự động nhắc nhở kèm thu thập nhanh log commit/hoạt động LMS gần nhất, AI tự draft trước nội dung standup theo mẫu. Learner chỉ cần review, chỉnh sửa nhanh và xác nhận nộp trong 1-click.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 15 phút

[1 Mở LMS/Discord: 2']
→ [2 Nhớ lại & gom activity hôm qua: 6']  <-- bottleneck
→ [3 Viết recap & kế hoạch: 5']
→ [4 Format + Check quy chuẩn: 1']
→ [5 Nộp bài trước 10h: 1']
```

### Draft future workflow

```text
FUTURE STATE — 3 phút

[1 Auto-trigger nhắc nhở 9:00: 0']
→ [2 AI gom log Git/LMS & draft standup: 1']
→ [3 Learner review + edit: 2']  <-- human boundary
→ [4 1-click Nộp: 0']

Fallback: AI draft thiếu ý → Learner tự bổ sung/viết lại trong giao diện preview.
```

## Problem Card #2 — Tóm tắt & Trích xuất Yêu cầu Lab / Assignment (Problem #4)

**Problem 1 câu:**  
Mỗi khi nhận bài lab hoặc assignment mới, Learner phải tốn 30-45 phút đọc các tài liệu dài gồm 3-4 file để hiểu đề, dễ bỏ sót các tiêu chí chấm điểm (rubric) hoặc yêu cầu ẩn.

**Actor:**  
Learner trong các chương trình đào tạo/bootcamp công nghệ với các bài assignment hoặc lab chuyên sâu.

**Thời điểm / bối cảnh:**  
Đầu buổi lab mới hoặc ngay khi nhận đề bài assignment/project hằng tuần.

**Current workflow:**
1. Tải và mở toàn bộ các file tài liệu đính kèm (mô tả lab, file hướng dẫn, rubric, file mẫu)
2. Đọc lướt qua để nắm ý tổng quan (5-10 phút)
3. Đọc chi tiết từng file để tìm yêu cầu kĩ thuật, ràng buộc và tiêu chí chấm điểm (15-20 phút)
4. Tự tóm tắt lại danh sách công việc (checklist) và các mốc deliverables ra notebook/Notion
5. Lập thứ tự các bước thực hiện trước khi bắt tay vào gõ code/làm bài

**Bottleneck:**  
Bước 3 & 4 — Đọc tài liệu dài hàng chục trang qua nhiều file rời rạc, tốn thời gian lọc lấy thông tin cốt lõi và dễ bỏ sót các acceptance criteria quan trọng.

**Impact:**  
Tốn 30-45 phút/bài lab. Nếu có 3 bài/tuần, tổng thời gian đọc hiểu đề chiếm đến 90-135 phút/tuần. Bỏ sót tiêu chí dẫn đến việc phải làm lại (re-work) hoặc bị trừ điểm đáng tiếc.

**Success metric:**  
Giảm thời gian đọc hiểu & trích xuất yêu cầu từ 45 phút xuống dưới 10 phút; đảm bảo 100% các tiêu chí chấm điểm trong rubric được trích xuất thành checklist.

**Non-AI alternative:**  
Giảng viên/TA cung cấp sẵn một file TL;DR (Executive Summary) hoặc checklist ngắn kèm theo bộ tài liệu lab.

**AI hypothesis:**  
AI phân tích toàn bộ các file tài liệu lab/assignment được cung cấp, tự động trích xuất: Problem Statement 1 câu, Checklist Acceptance Criteria, Rubric Scoring breakdown và Thứ tự các bước triển khai gợi ý.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 45 phút

[1 Tải & mở 3-4 file đính kèm: 3']
→ [2 Đọc lướt tổng quan: 7']
→ [3 Đọc chi tiết lọc yêu cầu & rubric: 20']  <-- bottleneck
→ [4 Tự tạo checklist công việc: 10']
→ [5 Lập plan các bước làm: 5']
```

### Draft future workflow

```text
FUTURE STATE — 10 phút

[1 Upload/Đưa tài liệu lab vào AI: 1']
→ [2 AI trích xuất Checklist, Rubric & Steps: 1']
→ [3 Learner đọc summary & đối chiếu file gốc: 7']  <-- human boundary
→ [4 Xác nhận checklist & bắt đầu làm: 1']

Fallback: AI bỏ sót chi tiết kĩ thuật đặc thù → Learner xem lại phần tương ứng trong file tài liệu gốc.
```

## Problem Card #3 — Aggregator & Centralized Deadline Tracker (Problem #3)

**Problem 1 câu:**  
Hàng ngày Learner phải tốn thời gian mở và kiểm tra rải rác ở nhiều nền tảng (LMS, Google Calendar, Slack, Notion) để cập nhật deadline, dễ bị trôi thông báo dẫn đến trễ hạn.

**Actor:**  
Learner/Học viên phải quản lý công việc và bài tập trên nhiều công cụ quản lý khác nhau đồng thời.

**Thời điểm / bối cảnh:**  
Đầu ngày làm việc (khi lên kế hoạch) và cuối ngày (khi rà soát công việc chưa xong).

**Current workflow:**
1. Đăng nhập LMS check mục Assignment / Calendar xem có bài tập mới hoặc deadline sắp tới không
2. Mở Google Calendar kiểm tra lịch học, lịch họp nhóm hoặc sự kiện trong ngày
3. Mở Slack/Discord lướt qua các kênh thông báo (announcements) để tìm tin nhắn chứa mốc thời gian không chính thức từ Mentor/TA
4. Mở Notion/Todoist cá nhân để tự gõ lại và cập nhật danh sách công việc
5. Sắp xếp lại thứ tự ưu tiên các task cần hoàn thành trong ngày

**Bottleneck:**  
Bước 3 & 4 — Phải thủ công truy cập từng nền tảng, đọc các tin nhắn Slack bị trôi để nhặt thông báo deadline, sau đó tự copy-paste cập nhật về công cụ cá nhân.

**Impact:**  
Tốn khoảng 15-20 phút mỗi ngày (~100 phút/tuần). Thi thoảng bị bỏ sót 1-2 deadline quan trọng do thông báo bị trôi trong kênh chat Slack/Discord.

**Success metric:**  
Giảm thời gian kiểm tra & tổng hợp deadline từ 20 phút/ngày xuống dưới 3 phút; giảm số lần sót/trễ deadline do quên check kênh về 0.

**Non-AI alternative:**  
Quy định tập trung toàn bộ deadline về 1 kênh LMS duy nhất; hoặc dùng webhook/Zapier đẩy thông báo tự động từ LMS về Google Calendar.

**AI hypothesis:**  
Hệ thống tự động kết nối API (LMS, Calendar, Notion) kết hợp với AI scan các tin nhắn chứa thông báo deadline trên Slack/Discord để tổng hợp thành 1 Dashboard duy nhất, đồng thời AI gợi ý thứ tự ưu tiên xử lý.

**Quick gut:**  
Rule / Workflow (Rule cho API Sync dữ liệu, Workflow cho AI parse text thông báo Slack).

### Draft current workflow

```text
CURRENT STATE — 20 phút

[1 Check LMS Assignment: 3']
→ [2 Check Google Calendar: 2']
→ [3 Lướt kênh Slack/Discord tìm thông báo: 8']  <-- bottleneck
→ [4 Copy & gõ lại vào Notion cá nhân: 5']
→ [5 Lập danh sách ưu tiên: 2']
```

### Draft future workflow

```text
FUTURE STATE — 3 phút

[1 System auto-pull API & AI parse Slack text: 0.5']
→ [2 AI tổng hợp Dashboard & gợi ý Priority: 0.5']
→ [3 Learner rà soát Dashboard & điều chỉnh ưu tiên: 2']  <-- human boundary
→ [4 Bắt đầu thực hiện task: 0']

Fallback: AI nhận diện nhầm tin nhắn chat thường thành deadline → Learner bấm Xóa/Dismiss mốc deadline đó khỏi Dashboard.
```

## Problem Cards Top 3 — Tóm tắt so sánh

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| #1 Daily Standup | Learner | Lục lại ký nhớ & gom activity hôm qua | 15 phút → 3 phút | Workflow / Rule | (Đã chọn làm #1) Workflow rõ, pain hàng ngày, metric cực kỳ rõ ràng |
| #2 Tóm tắt Lab | Learner | Đọc 3-4 file dài tìm yêu cầu & rubric | 45 phút → 10 phút | Workflow | Tần suất theo buổi lab (không hàng ngày như #1), độ chuẩn xác tóm tắt cần kiểm tra kỹ hơn |
| #3 Deadline Tracker | Learner | Lướt Slack tìm thông báo bị trôi & copy thủ công | 20 phút → 3 phút | Rule / Workflow | Phụ thuộc nhiều vào API integration / permission kết nối các nền tảng khác nhau |
