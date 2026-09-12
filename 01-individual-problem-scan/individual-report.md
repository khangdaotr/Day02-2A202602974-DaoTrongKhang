# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Đào Trọng Khang
- Mã học viên: 2A202602974
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): Sinh viên sắp tốt nghiệp
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem): 
            -Đi học VinAI thực chiến
            -Làm đồ án tại trường
            -Thực tập làm game tại công ty indie
            -làm lab tại Vin
            -Tham gia workshop tại VinAI

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 |Lặp lại|Hằng ngày đọc báo tổng hợp tin tức |bản thân |3,5 tiếng/tuần |
| 2 |Lặp lại |Nghiên cứu tài liệu, slide VinAI mỗi tối |bản thân |7 tiếng/tuần |
| 3 |Tốn thời gian |Nhận và chỉnh sửa report đồ án của giảng viên  |Giảng viên,bản thân |1 tiếng/bản |
| 4 |Tốn thời gian|Team meeting ý tưởng về game của từng thành viên |Cả team |1 tiếng/meeting |
| 5 |Pain từ người khác |Nhận report từ tester, có thể chỉnh sửa |dev, tester,designer |Không cố định |
| 6 |AI có thể tốt hơn |Summarize report  |BA |1 tiếng/ngày |
| 7 | | | | |
| 8 | | | | |
| 9 | | | | |
| 10 | | | | |

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi:
- Ý dùng được:
- Ý bỏ vì không phải pain thật:

**Self-check Phase 1:**
- [x ] Đủ 5+ dòng, mỗi dòng có actor + số đo cụ thể
- [x ] Dùng ít nhất 3/4 lăng kính
- [x ] Không có dòng chung chung kiểu "mất nhiều thời gian"

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 |Nhận và chính sửa đồ án từ giảng viên |Ai có thể hỗ trợ rõ, mất nhiều thời gian |Khó cải thiện nhiều |
| 2 |Nhận report từ tester cho dự án game |Workflow rõ, cải thiện vấn đề rõ ràng |thời gian mỗi lần khác nhau, data access |
| 3 |Summarize report |Ai hỗ trợ được nhiều, cải thiện rõ thời gian |data khác nhau khối lượng, cần hiểu biết |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — [Tên problem]

```text
Problem 1 câu:Nhận và chỉnh sửa đồ án từ giảng viên

Actor:Giảng viên DM cho sinh viên về đồ án cá nhân, từ đó sinh viên chỉnh sửa theo yêu cầu

Thời điểm / bối cảnh: Thứ 2 hàng tuần, trước buổi họp team đồ án

Current workflow 3-7 bước:
1.Giảng viên gửi DM nhận xét qua Teams
2.Sinh viên nhận và compare với đồ án cá nhân 
3.Chỉnh sửa theo yêu cầu
4.Báo cáo vấn đề nếu có
5.Viết self review DM lại cho giảng viên 

Bottleneck: bước 2, 3 - tốn rất nhiều thời gian kém hiệu quả

Impact: Tốn thời gian của cá nhân và giảng viên, ảnh hưởng đến toàn bộ các project

Success metric: giảm từ 7 tiếng/tuần xuống 4-5 tiếng 

Non-AI alternative: Giảng viên chỉ gửi 1 report/tháng

AI hypothesis: Dùng AI để so sánh, và viết self review  

Quick gut:
[ ] No AI / process fix
[ ] Rule
[ ] Workflow
[x ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — _420__ phút

[1 Nhận tin nhắn nhận xét của giảng viên qua Teams...: 5p__'] → [2 .Đọc, phân tích và so sánh chéo với đồ án cá nhân..: _30_'] → [3 .thực hiện chỉnh sửa đồ án..: _90_'] → [4 .Báo cáo vấn đề & Viết self-review gửi lại giảng viên..: _30_']  <-- bottleneck

FUTURE STATE — _270__ phút

[1 .Nhận DM từ Teams, nạp feedback và file đồ án vào AI Agent..: _10_'] → [2 AI tự động trích xuất yêu cầu, map với các phần trong đồ án, và draft sẵn self-review...: _30_'] → [3 ..Sinh viên review, duyệt các đề xuất chỉnh sửa của AI, thực hiện sửa đồ án và gửi self-review: _30_']  <-- human boundary

Fallback: nếu AI sai thì ..Quay lại quy trình thủ công: lấy nguyên văn tin nhắn DM của giảng viên trên Teams làm "single source of truth" (nguồn chuẩn duy nhất) để tự đối chiếu.
```

File đính kèm (nếu vẽ riêng): `01-individual-problem-scan-workflow-card-1.png`

---

#### Problem Card #2 — [Tên problem]

```text
Problem 1 câu:Nhận, phân tích lỗi (debug) và sửa code dựa trên bug report từ tester.

Actor:Tester tìm lỗi và gửi report (log, video, mô tả) cho Developer, từ đó Developer tái hiện lỗi và chỉnh sửa.

Thời điểm / bối cảnh:Cuối mỗi sprint hoặc sau t2 hàng tuần, trước khi build bản cập nhật mới.

Current workflow 3-7 bước:
1.Tester gửi bug report (qua Jira/Trello/Sheet) kèm theo log file và video quay màn hình.
2.Developer đọc report, xem video và phân tích log để tái hiện lại lỗi (reproduce bug).
3.Đọc source code để tìm ra nguyên nhân và thực hiện sửa lỗi (fix bug).
4.Build lại game và test nhanh để đảm bảo lỗi đã được khắc phục.
5.Cập nhật trạng thái ticket và viết note báo cáo lại cho tester.

Bottleneck:Bước 2, 3 - Tốn rất nhiều thời gian để mò mẫm tái hiện lỗi (đặc biệt khi mô tả của tester chung chung) và đọc hàng ngàn dòng log để khoanh vùng đoạn code bị hỏng.

Impact:Gây trễ tiến độ phát triển các tính năng mới, tốn thời gian của Developer, làm chậm chu kỳ cập nhật game

Success metric:Giảm thời gian xử lý một danh sách bug (batch of bugs) từ 10 tiếng/sprint xuống còn 4-5 tiếng/sprint.

Non-AI alternative:Yêu cầu tester tuân thủ một template báo cáo cực kỳ khắt khe (bắt buộc có step-by-step chi tiết 100%), hoặc giới hạn số lượng bug report mỗi tuần.

AI hypothesis:Dùng AI để đọc và phân tích file log, đối chiếu với mô tả của tester để khoanh vùng chính xác file/hàm (function) gây ra lỗi, đồng thời tóm tắt cách tái hiện lỗi và đề xuất đoạn code cần sửa.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[ ] Workflow
[x] Agent
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — 600 phút

[1 Nhận report trên Jira, tải log, video và xem lướt..30'.] → [2 .Mò mẫm tái hiện lỗi và đọc hàng ngàn dòng log: 240'..] → [3 .Đọc source code tìm root cause và gõ code sửa lỗi: 240..]  <-- bottleneck

FUTURE STATE — _270__ phút

[1 .Nhận ticket, feed log file và mô tả của tester vào AI Agent: 15'..] → [2.AI tự động scan log, mapping với mô tả, khoanh vùng chính xác file/hàm bị hỏng và draft đề xuất sửa code: 35'] → [3. Dev review đề xuất của AI, apply code fix, build và test lại: 220']  <-- human boundary

Fallback: .Quay về phương pháp debug truyền thống. Xóa bỏ các đoạn code AI đề xuất, tự mở raw log ra đọc, cắm breakpoint trong IDE để chạy step-by-step. Nếu log quá thiếu thông tin do AI không thể phân tích được, ping trực tiếp lại tester yêu cầu bổ sung video hoặc mô tả chi tiết hơn thay vì bắt AI đoán mò...
```

File đính kèm: `01-individual-problem-scan-workflow-card-2.png`

---

#### Problem Card #3 — [Tên problem]

```
Problem 1 câu:Thu thập thông tin rải rác từ các team (Code, Art, Game Design) để viết báo cáo tổng hợp tiến độ dự án game.

Actor:Project Manager (PM) hoặc Team Lead thu thập thông tin từ các thành viên để gửi báo cáo lên C-level, Stakeholders hoặc Publisher.

Thời điểm / bối cảnh:Chiều thứ 6 hàng tuần hoặc cuối mỗi Sprint/Milestone.

Current workflow 3-7 bước:
1. Hối thúc và thu thập các bản cập nhật (status update) từ nhiều nguồn (Jira, Slack/Teams, file thiết kế).
2. Đọc, chắt lọc các thông tin quan trọng (task hoàn thành, task bị trễ, lỗi phát sinh).
3. Phân loại và viết nháp báo cáo tổng hợp tiến độ theo ngôn ngữ dễ hiểu cho ban giám đốc
4. Căn chỉnh format, rà soát lại số liệu.
5. Gửi email/tin nhắn báo cáo cho cấp trên

Bottleneck: Bước 1, 2 và 3 - Tốn quá nhiều thời gian để "gom nhặt" dữ liệu thô, loại bỏ thông tin thừa và tóm tắt lại thành một báo cáo gãy gọn, dễ hiểu.

Impact: Mất nhiều giờ làm việc của PM/Lead, báo cáo dễ bị sót ý do thông tin quá nhiều, làm giảm thời gian dành cho việc giải quyết các vấn đề cốt lõi của dự án.

Success metric: Giảm thời gian làm report từ 3-4 tiếng/tuần xuống còn 45 phút - 1 tiếng/tuần.

Non-AI alternative: Ép toàn bộ các team phải tự điền đúng hạn vào một file Google Sheet có format cứng ngắc trước 3h chiều thứ 6 (ai không điền thì coi như không làm gì).

AI hypothesis: Dùng AI (Workflow/Agent) tự động kéo dữ liệu từ Jira/Git hoặc từ các tin nhắn update của team, sau đó tự động phân tích và draft sẵn một bản báo cáo hoàn chỉnh (chia rõ: Done, Doing, Blockers).

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[x] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — _240__ phút

[1 .Ping các team để gom dữ liệu update, xuất file từ Jira: 60'..] → [2 .Đọc, đối chiếu, lọc thông tin quan trọng và viết draft report: 120'..] → [3. Căn chỉnh format, rà soát văn phong, kiểm tra lỗi: 45'] → [4. Gửi báo cáo cho sếp/stakeholder: 15']

FUTURE STATE — __60_ phút

[1. Kích hoạt AI Agent tự động kéo data thô từ Jira và kênh chat của các team: 5'] → [2. AI tự động tóm tắt, highlight rủi ro (blockers) và draft report theo template có sẵn: 10'] → [3. PM đọc review bản draft, tinh chỉnh lại ngữ cảnh, chốt số liệu và bấm gửi: 45']  <-- human boundary

Fallback: ...
```Bỏ qua bản draft của AI. Quay lại mở Dashboard của Jira hoặc đọc lướt log chat của các team, tự chắt lọc và gõ tay 2 mục quan trọng nhất: "Các tính năng đã hoàn thành" và "Các rủi ro/blocker hiện tại" để gửi báo cáo nhanh. Các chi tiết râu ria khác tạm thời bỏ qua để đảm bảo tính chính xác và kịp thời của báo cáo.

File đính kèm: `01-individual-problem-scan-workflow-card-3.png`

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```Nhận, phân tích lỗi (debug) và sửa code dựa trên bug report từ tester.

```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```Dự án sẽ tập trung cải thiện workflow xử lý bug report, cụ thể là áp dụng AI Agent vào khâu phân tích file log, đối chiếu mô tả của tester để khoanh vùng tự động đoạn code gây ra lỗi. Mục tiêu đo lường thành công (success metric) là giảm 50% thời gian debug, rút ngắn từ 10 tiếng xuống chỉ còn 4-5 tiếng mỗi sprint. Tác động (impact) của cải tiến này là giải phóng đáng kể quỹ thời gian cho Developer để tập trung phát triển tính năng mới, đồng thời tăng tốc độ hoàn thiện và phát hành game.
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```Vấn đề về dữ liệu đặc thù của Game

```Vấn đề về hệ lụy code (Side-effect)

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra:
- Tôi sửa gì:

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đủ field
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
