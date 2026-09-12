# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Đỗ Lê Việt Anh
- Mã học viên: 2A202602491
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): intern BA tại TTCNTT BIDV, fresher microsoft power apps tại CMC Global.
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem):
    - Join các buổi daily/weekly meeting cập nhật tiến độ.
    - Đọc và rà soát các tài liệu RSD, Test case,...
    - Kiểm thử app
    - Tạo ticket testing/bug

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 |Tốn thời gian |Tốn thời gian tạo ticket testing | BA/Tester |Mất 2-3 phút cho 1 ticket và hay miss cấu trúc| |
| 2 |Tốn thời gian|Tốn time testing ứng dụng  |BA/Tester |1 test case mất 1-10 phút |
| 3 |Lặp lại|Ghi lại meeting notes & action cần làm sau meeting| BA/PM/Dev... |mất 10-15p/1 meeting/1 ngày → miss các note và các action cần thực hiện |
| 4 |Lặp lại|format và chuẩn hoá test case | BA/Tester |Không đúng chuẩn - chỉnh sửa nhiều lần|
| 5 |AI có thể tốt hơn |cross-validation cho RSD và Test case |BA/PM |mất 30-60p/1 module → miss vài test/sprint |
| 6 |AI có thể tốt hơn|Phân loại/Phân tích các ticket/bug đã được log|BA/Dev |User thường filter thủ công/dùng tool nhưng vẫn có thể miss ticket/bug do chi tiết chưa được chuẩn hoá|
| 7 |Pain từ người khác |Dev và Tester hỏi BA về các requriement |Dev/Tester ↔ BA | Dev và Tester thường xuyên hỏi lại BA về requirements cũng như test case/ticket/bug...|
| 8 |Pain từ người khác |PM/Team Lead hỏi progress dev/testing|PM/Team Lead → BA/Tester/Dev |mất 20-40p cho lần 1 hỏi trên 1-2 tuần |
| 9 |AI có thể tốt hơn |AI tự generate draft test case từ RSD |BA/Tester |Từ 1 template, AI có thể generate ra 1 file test case dựa vào yêu cầu mà BA đề ra|

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi: **@files:individual-report.md, dựa vào thông tin cá nhân hãy cho tôi vài ý tưởng cho Phase 1.**
- Ý dùng được: 4,5,6,8
- Ý bỏ vì không phải pain thật: 

**Self-check Phase 1:**
- [x] Đủ 5+ dòng, mỗi dòng có actor + số đo cụ thể
- [x] Dùng ít nhất 3/4 lăng kính
- [x] Không có dòng chung chung kiểu "mất nhiều thời gian"

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tốn thời gian tạo ticket testing| (1) Lặp lại hàng ngày, tần suất cao; (2) Mất 2-3 phút/ticket và hay miss cấu trúc → tích lũy nhiều giờ/sprint; (3) Workflow rõ 4-5 bước, bottleneck ở bước soạn nội dung ticket | Liệu AI-generated ticket có đủ context cho Dev hiểu không? Cần đo tỷ lệ ticket bị reopen sau khi dùng AI |
| 2 | Dev và Tester hỏi BA về các requirement| (1) Pain thật từ nhiều phía (Dev + Tester → BA), ảnh hưởng cả team; (2) Gây gián đoạn workflow BA 3-5 lần/tuần, mỗi lần 10-20 phút; (3) Root cause có thể giải quyết bằng AI (tự trả lời FAQ từ RSD) | Requirement phức tạp hay thay đổi → AI có trả lời đúng không? Liệu Dev/Tester có tin tưởng câu trả lời từ AI thay vì hỏi trực tiếp BA? |
| 3 | Tốn time testing ứng dụng| (1) Chiếm phần lớn thời gian trong ngày của Tester/BA; (2) 1 test case mất 1-10 phút, biên độ lớn → khó estimate; (3) Có thể dùng AI hỗ trợ auto-fill expected result hoặc gợi ý test steps | Một số test case cần thao tác UI thủ công → AI khó thay thế hoàn toàn; Cần xác định rõ loại test case nào AI hỗ trợ được (functional vs UI vs integration) |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — Tốn thời gian tạo ticket testing / bug

```text
Problem 1 câu:
Khi phát hiện bug hoặc cần log ticket test, BA/Tester mất 2-3 phút cho mỗi ticket chỉ để gõ lại các trường thông tin chuẩn (Steps to reproduce, Expected vs Actual, Environment) và thường xuyên miss cấu trúc hoặc thiếu context cho Dev.

Actor:
Intern BA / Tester tại TTCNTT BIDV & CMC Global chịu trách nhiệm kiểm thử và log bug/ticket lên Jira/Azure DevOps.

Thời điểm / bối cảnh:
Trong các đợt testing sprint, kiểm thử sau build mới, hoặc UAT khi phải log dồn nhiều bug/ticket trong thời gian ngắn.

Current workflow 3-7 bước:
1. Phát hiện bug/lỗi tính năng trong quá trình test app
2. Chụp màn hình lỗi / copy error log
3. Mở Jira/Azure DevOps, chọn project và loại issue (Bug/Task)
4. Nhập tiêu đề, chọn component, priority, environment
5. Soạn nội dung: Pre-condition, Steps to reproduce, Actual result, Expected result (bottleneck)
6. Đính kèm ảnh/video chứng minh và assign cho Dev

Bottleneck:
Bước 5 — Soạn chi tiết Pre-condition, Steps to reproduce, Actual result, Expected result mất 1.5 - 2 phút/ticket; hay bị gõ tắt, thiếu bước hoặc sai cấu trúc chuẩn khiến Dev khó tái hiện.

Impact:
Mỗi đợt test log 10-15 tickets/ngày → mất 30-45 phút chỉ để gõ ticket. Khi ticket thiếu cấu trúc chuẩn, Dev phải ping hỏi lại (3-5 lần/tuần, mỗi lần mất 5-10 phút), làm chậm tiến độ fix bug của sprint.

Success metric:
Giảm thời gian tạo 1 ticket từ 2-3 phút xuống dưới 45 giây; 100% ticket tuân thủ chuẩn format dự án; giảm 70% số lần Dev phải hỏi lại để làm rõ bug.

Non-AI alternative:
Sử dụng Jira Issue Template / checklist điền sẵn. Cách này giúp nhớ cấu trúc nhưng người dùng vẫn phải tự gõ thủ công toàn bộ text từng bước, không giải quyết được tốc độ và công sức gõ lại.

AI hypothesis:
BA/Tester chỉ cần nhập mô tả ngắn gọn (voice/bullet points thô) + ảnh chụp màn hình, AI sẽ tự phân tích và sinh ra bản draft ticket chuẩn cấu trúc (đủ steps, actual, expected, severity gợi ý). BA/Tester chỉ cần review lại trong 15 giây.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — ~3.5 phút (210s)

[1 Phát hiện lỗi: 30s] 
→ [2 Chụp ảnh/log: 30s] 
→ [3 Mở Jira tạo issue: 15s] 
→ [4 Điền fields cơ bản: 15s] 
→ [5 Soạn Steps & Actual/Expected: 100s]  <-- bottleneck
→ [6 Review & Assign: 20s]

FUTURE STATE — ~1.2 phút (70s)

[1 Phát hiện lỗi & chụp ảnh: 30s] 
→ [2 Nhập raw notes/ảnh vào AI helper: 10s] 
→ [3 AI generate draft ticket chuẩn cấu trúc: 5s] 
→ [4 BA/Tester review & edit: 20s]  <-- human boundary
→ [5 Bấm push lên Jira/DevOps: 5s]

Fallback: nếu AI sinh sai bước tái hiện hoặc hallucinate, BA bấm nút "Reset" và dùng template form thủ công có sẵn để điền tay.
```

File đính kèm (nếu vẽ riêng): `01-individual-problem-scan-workflow-card-1.png`

---

#### Problem Card #2 — Dev và Tester hỏi BA về các requirement trong RSD

```text
Problem 1 câu:
Dev và Tester thường xuyên ngắt quãng BA để hỏi lại các logic/edge case chưa rõ trong tài liệu RSD, khiến BA tốn 10-20 phút mỗi lần để lục lại tài liệu và giải thích lại.

Actor:
BA (người trả lời), Dev và Tester (người hỏi cần làm rõ requirement).

Thời điểm / bối cảnh:
Trong sprint khi Dev bắt đầu implement logic phức tạp hoặc Tester viết test cases dựa trên tài liệu RSD.

Current workflow 3-7 bước:
1. Dev/Tester gặp điểm mơ hồ trong RSD hoặc luồng nghiệp vụ
2. Dev/Tester nhắn tin (Teams/Skype) hoặc gặp trực tiếp BA để hỏi
3. BA nhận câu hỏi, phải dừng task đang làm dở (bị context switching)
4. BA mở file RSD (thường dài 30-50 trang) tìm lại section quy định nghiệp vụ tương ứng (bottleneck)
5. BA đọc lại logic, gõ câu trả lời giải thích hoặc tổ chức ad-hoc call
6. Dev/Tester nhận câu trả lời và tiếp tục công việc

Bottleneck:
Bước 4 & 5 — BA phải dừng việc đang làm, tìm kiếm trong tài liệu RSD dài nhiều phiên bản để trích xuất đúng quy tắc nghiệp vụ/edge case và diễn giải lại (mất 10-15 phút/lần).

Impact:
Xảy ra 3-5 lần/tuần. BA mất 60-100 phút/tuần và đứt đoạn luồng suy nghĩ công việc chính. Dev/Tester bị block công việc trong thời gian chờ đợi phản hồi.

Success metric:
Giảm 50% số lần Dev/Tester phải trực tiếp hỏi BA; thời gian nhận câu trả lời giảm từ 15-30 phút xuống dưới 1 phút.

Non-AI alternative:
Xây dựng tài liệu FAQ dự án hoặc bảng Requirement Traceability Matrix (RTM). Tuy nhiên tài liệu tĩnh khó tra cứu khi quy mô lớn và team lười đọc tài liệu dài.

AI hypothesis:
Xây dựng trợ lý AI tra cứu thông minh trên tài liệu RSD dự án (RAG). Dev/Tester có thể hỏi đáp tự nhiên; AI tự động trích dẫn chính xác mục/trang trong RSD kèm giải thích; chỉ escalate cho BA khi requirement chưa được định nghĩa.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — ~32 phút

[1 Dev/Tester kẹt requirement: 5'] 
→ [2 Nhắn tin hỏi BA: 2'] 
→ [3 Chờ BA đọc tin: 10'] 
→ [4 BA tra cứu RSD dài 30-50 trang: 10']  <-- bottleneck
→ [5 BA giải thích lại: 5']

FUTURE STATE — ~3 phút

[1 Dev/Tester hỏi câu hỏi vào AI Assistant: 1'] 
→ [2 AI search RSD & trích dẫn điều khoản trả lời: 10''] 
→ [3 Dev/Tester đọc hiểu & confirm câu trả lời: 2']  <-- human boundary
→ [4 (Nếu case mới chưa có trong RSD) Chuyển câu hỏi cho BA: 1']

Fallback: nếu AI trả lời "Không tìm thấy thông tin trong RSD" hoặc độ tin cậy thấp, hệ thống tự động forward câu hỏi kèm link tài liệu tới BA.
```

File đính kèm: `01-individual-problem-scan-workflow-card-2.png`

---

#### Problem Card #3 — Tốn thời gian testing ứng dụng

```text
Problem 1 câu:
BA/Tester tốn từ 1 đến 10 phút cho mỗi test case khi kiểm thử ứng dụng thủ công, tốn nhiều thời gian nhất ở việc chuẩn bị data test và nhập liệu lặp đi lặp lại trên các form dài.

Actor:
Intern BA / Tester thực hiện functional test & regression test trên ứng dụng (Power Apps / hệ thống nội bộ).

Thời điểm / bối cảnh:
Các đợt test release cuối sprint hoặc test lại (regression) sau khi Dev deploy bản vá bug.

Current workflow 3-7 bước:
1. Mở danh sách test cases trong file Excel / checklist
2. Đọc kịch bản và chuẩn bị dữ liệu test (test data) phù hợp
3. Mở ứng dụng, thao tác tuần tự các bước tiền điều kiện
4. Nhập từng trường dữ liệu vào form ứng dụng (bottleneck)
5. Bấm submit và quan sát kết quả thực tế (Actual result)
6. Đối chiếu với Expected result và ghi nhận trạng thái Pass/Fail vào checklist

Bottleneck:
Bước 4 — Nhập liệu thủ công từng trường trên các màn hình/form có nhiều trường dữ liệu và nhiều bước phức tạp (mất 2-5 phút/case); dễ nhầm lẫn dữ liệu giữa các lần test lặp lại.

Impact:
Một đợt test gồm 30-50 test cases mất 3-5 giờ kiểm thử thủ công liên tục. Gây mệt mỏi, giảm độ tập trung và dễ bỏ sót lỗi ở các case kiểm thử cuối.

Success metric:
Giảm thời gian thực thi trung bình mỗi test case từ 5 phút xuống còn 1.5 - 2 phút; tự động sinh dữ liệu test hợp lệ/bất hợp lệ trong vòng 5 giây.

Non-AI alternative:
Viết script automation test (Selenium / Playwright) hoặc dùng tool mock data tĩnh. Khó áp dụng cho dự án nội bộ thay đổi UI liên tục hoặc các nền tảng low-code như Power Apps do khó bắt element ID.

AI hypothesis:
AI hỗ trợ sinh nhanh bộ dữ liệu test (hợp lệ, biên, ngoại lệ) theo cấu trúc form RSD và tự động sinh checklist so sánh kết quả mong đợi để BA/Tester chỉ cần thao tác kiểm tra nhanh.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — ~7 phút/test case

[1 Đọc test case: 1'] 
→ [2 Chuẩn bị mock data: 2'] 
→ [3 Thao tác & nhập liệu form: 3']  <-- bottleneck
→ [4 So sánh kết quả: 30''] 
→ [5 Ghi log checklist: 30'']

FUTURE STATE — ~2 phút/test case

[1 AI tự động sinh sẵn bộ test data theo kịch bản: 15''] 
→ [2 BA/Tester copy data test thực thi trên app: 1'] 
→ [3 BA/Tester đối chiếu nhanh kết quả với checklist gợi ý: 30'']  <-- human boundary
→ [4 Tự động cập nhật trạng thái Pass/Fail: 15'']

Fallback: nếu test data do AI sinh không tương thích với validation của hệ thống, tester quay lại dùng bộ test data mặc định đã lưu từ trước.
```

File đính kèm: `01-individual-problem-scan-workflow-card-3.png`

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Problem Card #1 — Tốn thời gian tạo ticket testing / bug
```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
Đây là công việc tôi phải làm hằng ngày với tần suất rất cao (10-15 tickets/ngày trong các đợt test). Bottleneck rất rõ ràng ở khâu soạn thảo chi tiết Steps to reproduce và Actual vs Expected (chiếm 70% thời gian tạo ticket). Giải quyết bài này giúp tiết kiệm 30-45 phút mỗi ngày, chuẩn hóa 100% format ticket giúp Dev hiểu ngay mà không phải hỏi lại.
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```text
1. Làm sao để đảm bảo AI không tự "bịa" (hallucinate) các bước tái hiện (Steps to reproduce) khi Tester chỉ cung cấp mô tả ngắn hoặc hình ảnh chụp màn hình?
2. Trong bối cảnh ngân hàng bảo mật cao, luồng dữ liệu của bug (ảnh chụp/log nội bộ) đưa vào AI xử lý có vi phạm chính sách bảo mật thông tin hay không?
```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra: AI tạo ticket có thể làm tester ỷ lại, không kiểm tra kỹ dữ liệu thực tế dẫn đến ticket trông đẹp nhưng nội dung tái hiện không chuẩn xác; ngoài ra Dev có thể bị ngợp nếu AI viết quá dài dòng.
- Tôi sửa gì: Đặt boundary con người chặt chẽ — AI chỉ sinh bản nháp ngắn gọn (tối đa 4-5 bước súc tích), bắt buộc BA/Tester phải có 15-20s review và bấm nút xác nhận trước khi issue được post lên hệ thống chính thức.

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đủ field
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
