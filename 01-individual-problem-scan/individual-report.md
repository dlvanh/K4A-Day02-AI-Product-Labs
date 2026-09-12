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
| 2 |Tốn thời gian|Tốn time testing ứng dụng  |BA/Tester |1 test case mất 2-3 phút |
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
| 1 | | | |
| 2 | | | |
| 3 | | | |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — [Tên problem]

```text
Problem 1 câu:

Actor:

Thời điểm / bối cảnh:

Current workflow 3-7 bước:
1.
2.
3.
4.
5.

Bottleneck:

Impact:

Success metric:

Non-AI alternative:

AI hypothesis:

Quick gut:
[ ] No AI / process fix
[ ] Rule
[ ] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — ___ phút

[1 ...: __'] → [2 ...: __'] → [3 ...: __'] → [4 ...: __']  <-- bottleneck

FUTURE STATE — ___ phút

[1 ...: __'] → [2 ...: __'] → [3 ... review: __']  <-- human boundary

Fallback: nếu AI sai thì ...
```

File đính kèm (nếu vẽ riêng): `01-individual-problem-scan-workflow-card-1.png`

---

#### Problem Card #2 — [Tên problem]

```text
Problem 1 câu:

Actor:

Thời điểm / bối cảnh:

Current workflow 3-7 bước:
1.
2.
3.
4.
5.

Bottleneck:

Impact:

Success metric:

Non-AI alternative:

AI hypothesis:

Quick gut:
[ ] No AI / process fix
[ ] Rule
[ ] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — ___ phút

[1 ...] → [2 ...] → [3 ...]  <-- bottleneck

FUTURE STATE — ___ phút

[1 ...] → [2 ...] → [3 ... review]  <-- human boundary

Fallback: ...
```

File đính kèm: `01-individual-problem-scan-workflow-card-2.png`

---

#### Problem Card #3 — [Tên problem]

```text
Problem 1 câu:

Actor:

Thời điểm / bối cảnh:

Current workflow 3-7 bước:
1.
2.
3.
4.
5.

Bottleneck:

Impact:

Success metric:

Non-AI alternative:

AI hypothesis:

Quick gut:
[ ] No AI / process fix
[ ] Rule
[ ] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — ___ phút

[1 ...] → [2 ...] → [3 ...]  <-- bottleneck

FUTURE STATE — ___ phút

[1 ...] → [2 ...] → [3 ... review]  <-- human boundary

Fallback: ...
```

File đính kèm: `01-individual-problem-scan-workflow-card-3.png`

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text

```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text

```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```text

```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra:
- Tôi sửa gì:

### Self-check nộp phần 01
- [ ] Có 5+ problems + top 3 Cards đủ field
- [ ] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [ ] Đã chọn 1 card pitch + câu hỏi challenge
