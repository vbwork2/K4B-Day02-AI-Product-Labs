# Day 02 Lab — Worksheet

## Thông tin cá nhân

- **Họ và tên:** Bùi Quang Vinh
- **Mã học viên:** 2A202603012
- **Bối cảnh:** Sinh viên / AI researcher intern  đang nghiên cứu các mô hình Computer Vision.
- **Công việc hằng tuần**:
    + Tổng hợp tài liệu để làm dẫn chứng hoặc tìm kiếm được hướng tiếp cận khác cho nghiên cứu các model computer vision.
    + Tìm kiếm thông tin các bài báo có nguồn uy tín và 
    + Liên kết các dạng thông tin lại với nhau, để tìm kiếm được relationship giữa các phần.

---

# Phase 1 — Individual Problem Scan

## Bảng scan

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Cách đo / dấu hiệu thật |
|---|---|---|---|---|
| 1 | Tốn thời gian | Khi nghiên cứu một model Computer Vision, phải đọc nhiều paper để tìm được dẫn chứng trực tiếp cho lựa chọn kiến trúc hoặc phương pháp. | Sinh viên / researcher CV | Thời gian để tìm 3–5 paper usable; số paper phải mở trước khi tìm được nguồn phù hợp |
| 2 | AI có thể tốt hơn | Khó tìm được các hướng tiếp cận khác cho cùng một bài toán vì search thường trả về các phương pháp gần với từ khóa ban đầu. | Researcher đang exploratory research | Số query phải thử; số approach mới tìm được |
| 3 | Tốn thời gian | Phải tự kiểm tra paper có đủ uy tín không: venue, năm, tác giả, citation, code hoặc reproduction. | Sinh viên / researcher | Thời gian verify mỗi paper; số paper bị loại sau khi đọc |
| 4 | Tốn thời gian | Search thường trả về blog, repo hoặc secondary source trong khi cần original paper / official publication. | Người cần citation học thuật | Tỷ lệ kết quả không phải primary source; số lần phải search lại |
| 5 | Tốn thời gian | Dataset, backbone, loss, metric, training setup và kết quả nằm rải rác trong nhiều section của paper nên phải extract thủ công. | Researcher so sánh model | Thời gian tạo bảng so sánh cho 5–10 paper; số field bị thiếu |
| 6 | AI có thể tốt hơn | Khó nhận ra hai paper đang giải quyết cùng một bottleneck nhưng dùng thuật ngữ khác nhau. | Researcher mới vào subfield | Số concept/term phải tra; số relationship phát hiện muộn |
| 7 | AI có thể tốt hơn | Khó nối quan hệ giữa paper, model, dataset và technique như “improves”, “uses”, “extends”, “addresses limitation”. | Researcher làm literature review | Thời gian dựng relationship map; số quan hệ phải dò thủ công |
| 8 | Tốn thời gian | Muốn tìm nguồn gốc của một claim phải lần theo citation chain qua nhiều paper. | Researcher cần dẫn chứng chính xác | Số citation hops; thời gian tìm original source |
| 9 | Tốn thời gian + AI có thể tốt hơn | Kết quả giữa các paper khó so sánh trực tiếp vì khác dataset, resolution, backbone, augmentation hoặc evaluation protocol. | Researcher benchmark model | Số paper không comparable; thời gian normalize context |
| 10 | AI có thể tốt hơn | Sau khi có nhiều paper, khó chuyển chúng thành một research landscape để thấy family of approaches, limitation và research gap. | Researcher tìm hướng nghiên cứu | Thời gian từ “có paper” đến “có research gap/hypothesis” |

---

# Phase 2 — Top 3 Problem Cards

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Liên kết paper/model/dataset/technique để tìm relationship và research gap | AI có lợi thế semantic; workflow rõ; impact cao với literature review | Relationship nào thực sự quan trọng với researcher? |
| 2 | Tìm nguồn uy tín và dẫn chứng phù hợp cho một claim nghiên cứu | Dễ đo; pain xảy ra thường xuyên; có thể validate nhanh | Baseline thời gian thật là bao nhiêu? |
| 3 | So sánh model giữa nhiều paper có experimental setting khác nhau | Quan trọng khi chọn model; nhiều dữ liệu cần chuẩn hóa | Có thể normalize đến mức nào mà không làm sai context? |

---

## Problem Card #1 — Research Relationship Discovery

### Problem

Khi literature review một chủ đề Computer Vision, researcher phải tự đọc nhiều paper và nối các quan hệ giữa model, paper, dataset, technique và limitation, khiến khó nhìn ra evolution của field và research gap.

### Actor

Sinh viên / researcher đang nghiên cứu Computer Vision.

### Current workflow

1. Xác định research question.
2. Search paper theo keyword.
3. Đọc abstract / method / experiment.
4. Ghi chú model, dataset, technique, limitation.
5. Mở citation/reference liên quan.
6. Tự nối relationship giữa các paper.
7. Tổng hợp thành hướng nghiên cứu.

### Bottleneck

Bước 4–6: thông tin rời rạc, thuật ngữ không thống nhất và relationship thường không được viết trực tiếp dưới dạng có cấu trúc.

### Impact

- Mất nhiều thời gian đọc lại paper.
- Dễ bỏ sót related work quan trọng.
- Khó nhìn ra model evolution và research gap.
- Research direction có thể bị giới hạn bởi keyword/search ban đầu.

### Success metric

- Giảm ít nhất 50% thời gian dựng literature relationship map.
- Với một tập paper test, ≥80% relationship quan trọng do người nghiên cứu xác nhận được tìm thấy.
- Mỗi relationship phải có source paper/section để kiểm tra.

### Non-AI alternative

- Spreadsheet / Notion table tự ghi paper.
- Citation manager + tag.
- Manual mind map / graph.

### AI hypothesis

Dùng workflow gồm retrieval + information extraction + semantic relationship linking để biến các paper thành graph có cấu trúc:

```text
Paper A → improves → Method B
Method B → uses → Backbone C
Paper D → addresses limitation → X
Model E → evaluated_on → Dataset F
```

### Quick gut

**Workflow**

### Current workflow

```text
Research question
→ Search papers
→ Read papers
→ Extract notes
→ Follow citations
→ Manually connect relationships   <-- bottleneck
→ Identify research gap
```

### Future workflow

```text
Research question
→ Retrieve relevant papers
→ Extract entities: model / dataset / method / metric / limitation
→ AI link semantic relationships
→ Researcher verify source + edge   <-- human boundary
→ Build research landscape
→ Identify research gap
```

### Fallback

Nếu relationship không có source rõ hoặc confidence thấp → không thêm vào graph, researcher kiểm thủ công.

---

## Problem Card #2 — Trustworthy Evidence Retrieval

### Problem

Khi cần bảo vệ một lựa chọn model hoặc approach trong nghiên cứu Computer Vision, researcher phải tìm và lọc nhiều paper để có được dẫn chứng trực tiếp từ nguồn uy tín.

### Actor

Sinh viên / researcher cần citation cho research proposal, report hoặc experiment.

### Current workflow

1. Search keyword.
2. Mở nhiều kết quả.
3. Loại blog / secondary source.
4. Kiểm venue / tác giả / năm.
5. Đọc abstract / experiment.
6. Tìm đoạn hỗ trợ claim.
7. Lưu citation.

### Bottleneck

Bước 2–6: nhiều kết quả nhưng ít nguồn thực sự phù hợp với claim.

### Impact

- Tốn thời gian research.
- Có thể cite nguồn không đủ mạnh.
- Dẫn chứng có thể chỉ liên quan gián tiếp đến claim.

### Success metric

- Giảm ≥50% time-to-find 3 nguồn usable.
- Top results ưu tiên original paper / official publication.
- Mỗi evidence snippet phải gắn với source và context.

### Non-AI alternative

- Google Scholar.
- Semantic Scholar.
- Filter theo venue/year.
- Citation manager.

### AI hypothesis

Workflow hỗ trợ:
- hiểu claim,
- search/retrieve paper,
- rank theo mức liên quan,
- trích evidence,
- yêu cầu researcher verify.

### Quick gut

**Workflow**

---

## Problem Card #3 — Cross-paper Model Comparison

### Problem

Khi so sánh các model Computer Vision, researcher khó kết luận model nào thực sự tốt hơn vì mỗi paper sử dụng dataset, backbone, resolution, training setup và evaluation protocol khác nhau.

### Actor

Researcher cần chọn baseline hoặc model phù hợp cho experiment.

### Current workflow

1. Chọn model cần so sánh.
2. Đọc experiment section từng paper.
3. Ghi dataset và metric.
4. Ghi backbone / resolution / training setup.
5. So sánh kết quả.
6. Loại các comparison không công bằng.
7. Chọn candidate model.

### Bottleneck

Bước 3–6: phải normalize context trước khi so sánh.

### Impact

- Dễ so sánh “apple-to-orange”.
- Có thể chọn model dựa trên metric cao nhưng setting thuận lợi hơn.
- Tốn thời gian tạo benchmark table.

### Success metric

- Giảm ≥50% thời gian tạo comparison table.
- 100% comparison phải hiển thị dataset, metric và key experiment context.
- System phải flag khi hai kết quả không đủ điều kiện để so trực tiếp.

### Non-AI alternative

Spreadsheet template cố định.

### AI hypothesis

AI extract experiment setup và semantic differences; rule layer quyết định field nào đủ để gọi là comparable.

### Quick gut

**Workflow + Rule**

---

## Card muốn pitch nhất

**Research Relationship Discovery**

### Vì sao

Đây không chỉ là search paper mà là bước biến nhiều tài liệu rời rạc thành một bức tranh nghiên cứu có cấu trúc. Nó có semantic ambiguity cao, nhiều loại entity và relationship, phù hợp để so sánh Rule / Workflow / Agent.

### Câu hỏi muốn nhóm challenge

1. Researcher thật sự cần relationship graph hay chỉ cần một comparison table tốt?
2. Relationship nào có giá trị nhất: citation, method improvement, shared dataset, limitation, hay experiment dependency?
3. Nếu AI link sai một relationship, hậu quả tới research conclusion lớn đến mức nào?

---

# Phase 3 — Group Convergence

> Điền sau khi nhóm pitch và challenge thật.

## Candidates của tôi

| Candidate | Actor | Bottleneck | Điểm mạnh |
|---|---|---|---|
| Research Relationship Discovery | Researcher CV | Nối thông tin giữa nhiều paper | Semantic problem rõ, AI fit cao |
| Trustworthy Evidence Retrieval | Researcher cần citation | Tìm nguồn thật sự hỗ trợ claim | Dễ đo, dễ validate |
| Cross-paper Model Comparison | Researcher chọn baseline | Normalize experimental context | Impact cao với model selection |

## Candidate đề xuất

**Research Relationship Discovery**

## Vì sao

- Workflow rõ.
- Có thể đo time và relationship recall.
- Có non-AI baseline.
- Không cần Agent tự chủ hoàn toàn.
- Phù hợp với nhu cầu literature review và research exploration.

---

# Phase 4 — Validation + Research

## Validation cần làm

### Interview 2–3 researcher / sinh viên CV

- Khi review 10–20 paper, phần nào mất thời gian nhất?
- Bạn đang lưu relationship giữa paper/model bằng cách nào?
- Bạn có thường đọc lại paper vì quên model nào kế thừa model nào không?
- Điều gì giúp bạn xác định research gap?
- Nếu có graph tự động, relationship nào bạn muốn thấy nhất?

### Survey 5–10 người

- Bạn thường đọc bao nhiêu paper cho một topic?
- Thời gian để hiểu research landscape?
- Bạn có dùng spreadsheet / Notion / citation manager không?
- Bạn gặp khó khăn ở search, extract, compare hay connect?
- Mức hữu ích của relationship map: 1–5?

## Evidence

| Nguồn | Số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Interview | TODO | TODO | TODO | TODO |
| Survey | TODO | TODO | TODO | TODO |
| Timing test | TODO | TODO | TODO | TODO |

---

# Phase 5 — Workflow + Problem Statement

## Current workflow

```text
Research question
→ Search paper
→ Read paper
→ Extract notes
→ Follow citation
→ Compare model
→ Manually connect relationships   <-- bottleneck
→ Identify research direction
```

## Future workflow

```text
Research question
→ Retrieve trusted papers
→ Extract entities:
   model / dataset / method / metric / limitation
→ Link relationships
→ Researcher verify source/relationship   <-- boundary
→ Build research graph
→ Compare approaches
→ Identify research gap
```

## Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên / researcher Computer Vision đang làm literature review hoặc tìm research direction |
| **Workflow** | Search → đọc → extract → follow citation → connect paper/model/dataset/technique → tìm gap |
| **Bottleneck** | Nối thông tin rời rạc giữa nhiều paper thành relationship có ý nghĩa |
| **Impact** | Tốn thời gian, dễ bỏ sót related work, khó nhìn ra evolution và research gap |
| **Success Metric** | Giảm ≥50% thời gian dựng research landscape; ≥80% relationship quan trọng được researcher xác nhận |
| **Boundary** | AI chỉ đề xuất relationship có source; researcher chịu trách nhiệm verify và kết luận nghiên cứu |

---

# Phase 6 — Rule / Workflow / Agent + Decision

## So sánh

| Mức | Phương án | Điểm mạnh | Hạn chế | Chọn? |
|---|---|---|---|---|
| **Rule** | Link theo citation, exact model name, dataset name | Dễ kiểm tra | Không hiểu synonym, implicit relationship | Không đủ |
| **Workflow** | Retrieve → extract → semantic linking → source verification → human review | Kiểm soát tốt, đủ semantic | Vẫn có hallucination/omission risk | **Chọn** |
| **Agent** | Tự search, tự mở paper, tự quyết định hướng đọc tiếp | Linh hoạt | Khó audit, dễ đi lệch scope, overkill | Chưa cần |

## Mức chọn

**Workflow**

## Vì sao

Bài toán cần semantic understanding nhưng pipeline tương đối rõ. Hệ thống không cần tự lập kế hoạch mở-ended; vì vậy Workflow dễ kiểm soát và đánh giá hơn Agent.

---

## Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Researcher Computer Vision làm literature review |
| **Workflow** | Search → retrieve → read → extract → link → verify → identify gap |
| **Bottleneck** | Semantic linking giữa paper/model/dataset/technique/limitation |
| **Impact** | Tốn thời gian và khó nhìn ra research landscape |
| **Success Metric** | ≥50% giảm thời gian; ≥80% verified relationship recall; 100% edge có source |
| **Boundary** | Không tự kết luận research claim; không tạo relationship không có source; researcher review trước khi dùng |
| **AI intervention point** | Sau retrieval/extraction và trước bước researcher tự nối relationship |
| **Mức chọn** | Workflow |
| **Rủi ro & human review** | AI có thể link sai hoặc bỏ sót; researcher kiểm source và xóa/sửa edge trước khi dùng |

---

## Final decision

**Decision: NOT YET**

### Lý do

Problem có workflow rõ và có lý do phù hợp với AI, nhưng chưa có validation đủ để chứng minh relationship discovery là bottleneck lớn nhất của researcher. Cần đo baseline và kiểm tra xem comparison table / citation manager hiện tại đã giải đủ pain hay chưa.

### Để chuyển sang GO

1. Interview 2–3 researcher.
2. Survey 5–10 người.
3. Test trên 10–20 paper của một chủ đề CV.
4. So 3 cách:
   - Manual notes.
   - Structured spreadsheet.
   - AI workflow.
5. Đo:
   - time-to-research-map,
   - verified relationship recall,
   - wrong relationship rate.

### Exit / rollback

Nếu AI tạo nhiều relationship sai hoặc researcher vẫn phải đọc lại gần như toàn bộ paper để tin graph, quay về structured table / manual mapping.

---

# Phase 7 — Individual Reflection

> Tự viết sau khi làm nhóm.

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Xác định các pain trong quá trình research Computer Vision | TODO |
| Pitch Problem Card | TODO | TODO |
| Challenge bài khác | TODO | TODO |
| Validation / research | TODO | TODO |
| Workflow nhóm | TODO | TODO |
| Problem Statement | TODO | TODO |
| Rule / Workflow / Agent | TODO | TODO |
| Decision | TODO | TODO |

## Reflection

```text
TODO — tự viết 8–12 câu sau hoạt động nhóm.
```

---

# Checklist cuối

- [x] Có 5+ problems.
- [x] Có Top 3 Problem Cards.
- [x] Có current/future workflow.
- [x] Có Problem Statement v0/v1.
- [x] Có so sánh Rule / Workflow / Agent.
- [x] Có decision tạm thời.
- [ ] Có evidence thật từ interview/survey.
- [ ] Có reflection cá nhân thật.
