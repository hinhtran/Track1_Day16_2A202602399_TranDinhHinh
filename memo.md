# Memo Teardown — Notion AI

**Họ tên:** Trần Đình Hinh  
**Ngày thực hiện:** 03/10/2026

**Vì sao chọn sản phẩm này:** Notion AI cho thấy cách AI chuyển từ hỗ trợ viết sang tìm kiếm kiến thức và thực hiện công việc trong workspace. Tôi chọn sản phẩm này để phân tích lợi thế từ dữ liệu, ngữ cảnh và quy trình sẵn có.

## §1. Timeline các cập nhật lớn

| Thời điểm | Cập nhật / quyết định sản phẩm | Context lúc đó | Revert về nguyên lý |
|---|---|---|---|
| **11/2022** |Ra mắt **Notion AI private alpha** trực tiếp trong workspace ([Nguồn](https://www.notion.com/blog/introducing-notion-ai)) | Generative AI bắt đầu bùng nổ, nhưng phần lớn trải nghiệm AI vẫn tách khỏi nơi người dùng đang viết và làm việc | **Wrapper / Moat:** giá trị không chỉ ở model mà ở việc AI nằm ngay trong workflow và context sẵn có |
| **02/2023** |Mở **Notion AI cho tất cả user**, bán add-on $10/member/tháng ([Nguồn](https://www.notion.com/en-gb/releases/2023-02-22)) | Gần 2 triệu người đã đăng ký waitlist; nhu cầu viết, tóm tắt, brainstorm bằng AI rất lớn | **x10:** rút ngắn nhiều thao tác viết, sửa, dịch, tóm tắt thành một lệnh |
| **11/2023** |Ra mắt **Q&A by Notion AI** ([Nguồn](https://www.notion.com/releases/2023-11-14)) | User không chỉ muốn tạo text mà còn cần tìm lại knowledge trong workspace | **Vertical AI / JTBD:** dùng private workspace context để trả lời câu hỏi cụ thể của tổ chức |
| **09/2024** |Mở rộng bằng **AI Connectors**, tìm trong Slack, Google Drive; GitHub/Jira được mở rộng sau đó ([Nguồn](https://www.notion.com/releases/2024-09-25)) | Knowledge doanh nghiệp phân mảnh qua nhiều SaaS | **Data moat + switching cost:** AI càng hữu ích khi có quyền truy cập dữ liệu và workflow thật của doanh nghiệp |
| **05/2025** |**Enterprise Search + Research Mode + AI Meeting Notes** ([Nguồn](https://www.notion.com/releases/2025-05-13)) | AI chuyển từ generation sang retrieval, synthesis và organizational memory | **Vertical AI:** AI hiểu company knowledge, không chỉ sinh nội dung chung |
| **09/2025** |**Notion 3.0: Agents** ([Nguồn](https://www.notion.com/releases/2025-09-18)) | Chatbot trả lời là chưa đủ; người dùng muốn AI trực tiếp thực hiện task nhiều bước | **x10 / Agentic workflow:** chuyển từ “answer” sang “action” |
| **02/2026** |**Custom Agents** chạy workflow lặp lại theo trigger/schedule, dùng nhiều tool ([Nguồn](https://www.notion.com/blog/introducing-custom-agents)) | Team có các quy trình lặp lại, cần AI hoạt động liên tục thay vì chỉ phản hồi khi được hỏi | **Workflow moat + switching cost:** agent được gắn vào quy trình vận hành cụ thể |
| **05/2026** |Ra mắt **Developer Platform**, gồm Workers, External Agents, CLI và API ([Nguồn](https://www.notion.com/blog/introducing-developer-platform)) | Khi agent trở thành hạ tầng công việc, doanh nghiệp cần custom logic, tích hợp và khả năng mở rộng | **Platform moat:** Notion tiến từ ứng dụng sang nền tảng cho người + agent cùng làm việc |

**Vì sao chọn những mốc này:** Tám mốc làm thay đổi công việc AI thực hiện, phạm vi dữ liệu AI truy cập hoặc mức tự chủ trong quy trình. Tôi loại các cập nhật nhỏ về giao diện và bổ sung lựa chọn model vì chúng không thể hiện rõ bước chuyển trong JTBD bằng các mốc trên.

## §2. Tệp user & JTBD

Các tệp dưới đây là suy luận từ use case và hướng phát triển sản phẩm, không phải số liệu phân bố khách hàng do Notion công bố.

| Nội dung | Early adopters | Tệp hiện tại |
|---|---|---|
| **Đặc điểm** | PM, marketer hoặc founder tại startup đã dùng Notion để viết brief, ghi chú họp và lưu wiki; thường xuyên cần soạn và tóm tắt nội dung | PM/team lead và nhóm vận hành có tài liệu trong Notion, trao đổi trên Slack, hồ sơ trên Drive; cần tổng hợp tiến độ và xử lý công việc lặp lại |
| **JTBD chính** | Khi soạn brief hoặc tổng hợp ghi chú, tôi muốn tạo bản nháp và tóm tắt ngay trong workspace để hoàn thành tài liệu nhanh hơn | Khi chuẩn bị báo cáo tiến độ, tôi muốn tổng hợp quyết định, trạng thái và việc cần làm từ nhiều nguồn, rồi cập nhật tài liệu để giảm thời gian tìm kiếm và điều phối |
| **Trước đó làm bằng cách nào?** | Tự viết, đọc và tóm tắt; hoặc dùng chatbot bên ngoài rồi copy kết quả vào Notion | Tìm thủ công trên từng ứng dụng, hỏi đồng nghiệp, đối chiếu thông tin và tự cập nhật báo cáo/database |
| **Cách dùng** | Chủ động gọi AI trên tài liệu đang xử lý | Hỏi trên nhiều nguồn, giao Agent thực hiện tác vụ hoặc cấu hình quy trình tự chạy |

**Dịch chuyển tệp:** AI Connectors (09/2024) là mốc mở rộng giá trị từ tài liệu cá nhân sang kiến thức phân tán của team. Enterprise Search (05/2025) củng cố nhu cầu tìm và tổng hợp thông tin toàn tổ chức; Agents (09/2025) và Custom Agents (02/2026) tiếp tục mở rộng sang thực thi và tự động hóa công việc.

**Switching cost — 4 forces:**

| Force | Mức độ giữ chân — nhận định | Điều giữ user ở lại |
|---|---|---|
| **Habit** | Trung bình | Đã quen viết brief, lưu wiki, quản lý dự án và ghi chú họp trong Notion; chuyển công cụ phải học lại cách làm |
| **Data** | Cao | Tài liệu, database, liên kết và lịch sử quyết định đã tích lũy; chuyển nền tảng phải di chuyển và tái cấu trúc ngữ cảnh |
| **Integration** | Cao | Connectors, quyền truy cập và automation đã cấu hình; chuyển công cụ phải thiết lập và kiểm tra lại |
| **Collaboration / Network** | Trung bình–cao | Cả team dùng chung wiki, database và quy trình; một cá nhân chuyển công cụ có thể làm gián đoạn phối hợp |

**Lực mạnh nhất:** Data, vì kiến thức và quan hệ giữa các tài liệu tích lũy theo thời gian. Nếu đối thủ giúp chuyển đầy đủ dữ liệu, liên kết và quyền truy cập với ít công sức, lực này giảm; khi đó độ tin cậy của Agent, tích hợp và thói quen làm việc sẽ quyết định giữ chân. Người dùng chủ yếu chỉ cần viết hoặc tóm tắt có lý do thử chatbot khác nếu tiện hơn hoặc rẻ hơn.

## §3. Ba dự đoán hướng đi trong 6–12 tháng tới

Khoảng dự đoán: 04–10/2027. Đây là phán đoán, không phải kế hoạch Notion đã công bố.

### Dự đoán 1 — Phối hợp nhiều agent

**Loại:** Mở rộng tính năng.

**Dự đoán:** Notion sẽ bổ sung khả năng phân công và chuyển giao công việc giữa các agent chuyên biệt trong cùng workspace.

**Lập luận:** Personal Agent → Custom Agents → External Agents ở §1 cho thấy sản phẩm mở rộng từ một trợ lý sang nhiều tác nhân thực hiện công việc. PM/team lead ở §2 cần tổng hợp thông tin và cập nhật tiến độ qua nhiều bước; phối hợp agent có thể nối các bước đó thành quy trình chung. Dấu hiệu để kiểm chứng là tính năng handoff, phân công hoặc theo dõi tác vụ giữa agent được phát hành.

### Dự đoán 2 — Kiểm soát chất lượng và vận hành agent

**Loại:** Mở rộng tính năng cho doanh nghiệp.

**Dự đoán:** Notion sẽ tăng khả năng theo dõi lịch sử chạy, phân tích lỗi, kiểm soát chi phí và yêu cầu phê duyệt với tác vụ quan trọng.

**Lập luận:** Custom Agents và Developer Platform ở §1 làm tăng số quy trình tự động và mức độ tích hợp. Nhóm vận hành ở §2 cần công việc hoàn thành đáng tin cậy, vì cập nhật sai có thể lan sang tài liệu và database dùng chung. Dấu hiệu để kiểm chứng là công cụ đánh giá kết quả, phân tích lỗi hoặc chính sách phê duyệt agent mới.

### Dự đoán 3 — Mở rộng thu phí theo mức sử dụng

**Loại:** Mô hình kiếm tiền.

**Dự đoán:** Notion sẽ mở rộng gói credits và công cụ quản lý ngân sách cho công việc agent, song song với thuê bao theo người dùng.

**Lập luận:** Custom Agents ở §1 đã đưa credits vào mô hình sử dụng. Với nhóm vận hành ở §2, số lần chạy và độ phức tạp của quy trình không tăng tương ứng với số nhân viên; thu phí theo mức sử dụng phù hợp với chi phí xử lý và nhu cầu tự động hóa. Dấu hiệu để kiểm chứng là gói credits, giới hạn ngân sách hoặc báo cáo chi phí theo quy trình được mở rộng.

## §4. AI Log

| Việc | AI làm hay bạn làm? | Kiểm chứng / phán đoán lại thế nào? |
|---|---|---|
| Tổng hợp timeline và gắn nguồn | Tôi tự tìm kiếm và chắt lọc các mốc quan trọng, AI hỗ trợ format bảng | Các mốc được chọn lọc dựa trên sự chuyển dịch về giá trị cốt lõi (từ công cụ cá nhân sang nền tảng doanh nghiệp). Các nguồn đều trích dẫn trực tiếp từ trang chủ Notion. |
| Chọn mốc và liên hệ nguyên lý | Tôi tự phân tích và áp dụng lý thuyết bài học | Dựa vào các khái niệm bài học như x10, moat (data, workflow), JTBD để giải thích lý do đằng sau các cập nhật của Notion. |
| Phân tích tệp user, JTBD và switching cost | Tôi tự phân tích và đánh giá | Đánh giá dựa trên góc nhìn thực tế của người dùng và các rào cản chuyển đổi (Switching Costs) như Habit, Data, Integration. |
| Viết ba dự đoán | Tôi tự suy luận, AI góp ý câu chữ | Các dự đoán được xây dựng logic từ xu hướng dịch chuyển của Notion AI hiện tại (từ gen-text sang agents và workflow). |
| Điều chỉnh phạm vi memo | Tôi tự biên tập và tối ưu nội dung | Rà soát lại toàn bộ tài liệu để đảm bảo bám sát yêu cầu đề bài và định dạng chuẩn. |
