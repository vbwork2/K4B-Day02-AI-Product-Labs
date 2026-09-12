# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Bùi Quang Vinh
- Mã học viên: 2A202603012
- Nhóm: Vision
- Candidate problem nhóm chọn: Research Relationship Discovery

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Xác định 10 pain trong quá trình research và chọn ra Top 3 Problem Cards: Research Relationship Discovery, Trustworthy Evidence Retrieval, Cross-paper Model Comparison. | Tạo 3 candidate có workflow, bottleneck, impact, success metric, non-AI alternative và AI hypothesis để đưa vào bước hội tụ của nhóm. |
| Pitch Problem Card | Đề xuất Problem Card #1 — Research Relationship Discovery: nối paper/concept/method/evidence/finding/limitation để tìm relationship và research gap. | Candidate này được đưa vào shortlist và được nhóm chọn với tổng điểm 34. |
| Chọn candidate problem | Đề xuất Research Relationship Discovery là candidate muốn pitch nhất. | Nhóm chọn Research Relationship Discovery làm candidate problem duy nhất. |
| Problem Statement | Phân tích metric cho bài toán: time-to-research-map, verified relationship recall, wrong relationship rate và source coverage. | Các metric được đưa vào Problem Statement và dùng làm điều kiện đánh giá pilot. |
| Rule / Workflow / Agent | Phân tích Rule / Workflow / Agent và đề xuất Workflow làm kiến trúc chính, Rule làm guardrail, chưa dùng Agent cho pilot. | Nhóm chọn Workflow vì cần semantic understanding nhưng pipeline vẫn có các stage rõ, dễ audit và human review. |
| Decision | Phân tích AI fit, metric và rủi ro của semantic relationship linking. | Nhóm chốt Decision: Not Yet vì chưa có interview/survey/timing evidence thật và chưa có baseline time-to-research-map. |
|Pitch  | Tôi là người pitch chính để làm rõ vấn đề của sản phẩm |  Thể hiện được rõ ý tưởng của sản phẩm và phản biện được các ý chính |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

Dấu tay rõ nhất của tôi là phần AI/Product Analysis: phân tích Rule / Workflow / Agent và metric cho Research Relationship Discovery. Kết quả là nhóm chọn Workflow làm kiến trúc chính, Rule làm guardrail và giữ human review trước khi relationship được dùng. Và tôi là người pitch chính.

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)


| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Dùng AI để mở rộng các pain trong quá trình research, nhóm lại thành candidate và gợi ý cách đo cho từng problem. | AI giúp tôi chuyển các pain ban đầu thành problem có actor, workflow và dấu hiệu đo cụ thể, từ đó rút xuống Top 3 candidate. | Một số gợi ý có thể chỉ nghe hợp lý nhưng chưa chứng minh đó là pain thật hoặc bottleneck lớn nhất. | Tôi chỉ giữ các problem có workflow tôi hiểu rõ và không coi các metric ban đầu là evidence đã được validate. |
| Problem Card | Dùng AI để cấu trúc Problem Card #1 Research Relationship Discovery và hai candidate còn lại theo Problem, Actor, Current workflow, Bottleneck, Impact, Success metric, Non-AI alternative và AI hypothesis. | AI giúp làm rõ rằng bottleneck nằm ở bước nối semantic relationship giữa nhiều paper chứ không chỉ ở search. | AI có xu hướng viết target như giảm 50% thời gian hoặc đạt 80% relationship recall như thể đó là số đã có cơ sở. | Tôi giữ các con số này ở mức hypothesis cần đo và chọn Research Relationship Discovery vì nó sát workflow literature review nhất. |
| Workflow | Dùng AI để diễn giải current workflow và future workflow, chia các bước retrieve, extract, link, validate và review. | AI giúp nhìn rõ điểm can thiệp của AI, human boundary và fallback khi edge không có source hoặc confidence thấp. | AI dễ đẩy workflow theo hướng tự động hóa quá nhiều, như để hệ thống tự nối hoặc sử dụng relationship mà chưa qua kiểm tra. | Tôi giữ researcher ở bước verify source, approve/edit/delete edge và không cho AI tự kết luận research gap. |
| Research | Dùng AI để tổng hợp existing solutions như Connected Papers, ResearchRabbit và Semantic Scholar rồi đối chiếu chúng với problem của nhóm. | AI giúp tôi nhận ra citation/similarity graph đã có tool làm khá tốt và khoảng trống nên tập trung vào semantic relationship có provenance. | AI có thể mô tả capability của tool quá rộng hoặc đánh đồng citation/similarity với các quan hệ nội dung như supports, extends hay addresses limitation. | Tôi thu hẹp prototype vào corpus đã chọn, semantic edge có source paper + section/snippet và giữ việc kiểm chứng nguồn trong workflow. |
| Problem Statement | Dùng AI để chỉnh Problem Statement từ problem ban đầu thành Actor, Workflow, Bottleneck, Impact, Success Metric và Boundary rõ hơn, đồng thời hỗ trợ chỉnh report theo Problem Card #1. | AI giúp làm rõ metric, boundary và mạch từ problem → workflow → AI intervention point. | Các bản trước còn bám quá nhiều vào Computer Vision và có lúc viết đẹp hơn mức evidence thật đang có. | Tôi yêu cầu thay framing Computer Vision bằng literature review/nghiên cứu học thuật chung và giữ rõ rằng baseline, interview, survey, timing test vẫn chưa có. |
| Rule / Workflow / Agent | Dùng AI để so sánh Rule, Workflow và Agent cho semantic relationship discovery. | AI giúp tách rõ Rule dùng cho exact match/provenance, Workflow dùng cho semantic linking nhiều stage, còn Agent chỉ phù hợp khi task thật sự open-ended. | AI dễ mặc định bài toán dùng AI thì Agent sẽ mạnh hơn hoặc nên tự chủ nhiều hơn. | Tôi chọn Workflow làm kiến trúc chính, Rule làm guardrail và chưa dùng Agent cho pilot vì corpus/scope đã xác định và cần dễ audit. |
| Decision | Dùng AI để rà checklist Go / Not Yet / No-Go dựa trên actor, workflow, metric, data, risk và human review. | AI giúp hệ thống hóa lý do và điều kiện cần để chuyển từ Not Yet sang Go. | AI không có interview, survey hay timing evidence thật nên không thể tự chứng minh semantic linking là bottleneck lớn nhất. | Tôi giữ Decision là Not Yet, yêu cầu validation thật và so manual notes, structured spreadsheet với AI Workflow trước khi kết luận Go. |
---

## 3. Reflection câu hỏi mở
**Reflection:**

Qua phần scan cá nhân, tôi xác định 10 vấn đề và rút xuống ba Problem Cards có workflow và metric rõ hơn. Trong ba candidate của mình, tôi ưu tiên Research Relationship Discovery vì bottleneck nằm ở việc nối semantic relationship giữa nhiều paper và có thể đo bằng time-to-research-map cùng verified relationship recall. Khi nhóm hội tụ các candidate, bài này được đưa vào shortlist và đạt tổng điểm 34, cao nhất trong ba bài cuối. Tôi thấy điểm quan trọng của bài toán không phải chỉ là tạo một graph trực quan mà là giảm công sức nối thông tin và giữ được provenance để researcher kiểm tra. Phần tôi đóng góp rõ nhất là phân tích Rule / Workflow / Agent và metric của bài toán. Rule vẫn hữu ích cho citation, exact/normalized entity name và provenance check, nhưng không đủ cho synonym hoặc implicit semantic relation. Agent chưa cần thiết vì pilot có corpus và scope xác định, trong khi Workflow cho phép chia thành các stage retrieve, extract, link, validate và review rõ ràng hơn. Một điểm khó là các target như giảm ít nhất 50% time-to-research-map hay đạt ít nhất 80% verified relationship recall mới chỉ là hypothesis vì chưa có baseline thật.


---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
