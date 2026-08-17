# Track 1 – Day 17: Finding and Validating Pain Points

## 1. Thông tin cá nhân và nhóm

- MHV: `2A202601198`
- Họ và tên: `Nguyễn Tấn Hoàng`
- Tên nhóm: `Chưa cung cấp`
- Thành viên: `Nguyễn Tấn Hoàng`
- Case đã chọn: **Case A — AI Tutor: Diagnostic Refresher**

## 2. Problem Hypothesis Brief

### 2.1. Solution directive

Thêm nút “Tôi vẫn chưa hiểu”. Khi học viên bấm nút, AI Tutor dùng nội dung bài hiện tại, câu trả lời gần đây và lịch sử học tập để đặt câu hỏi chẩn đoán, chọn khái niệm nền cần ôn, giải thích ngắn rồi đưa học viên quay lại bài đang học.

### 2.2. Capability trung tính

Phát hiện phần kiến thức nền còn thiếu tại thời điểm người học bị mắc kẹt, cung cấp hỗ trợ vừa đủ để họ khôi phục mạch hiểu và tiếp tục bài học hiện tại.

Capability này không mặc định phải được triển khai bằng nút bấm, AI hoặc một màn hình riêng.

### 2.3. Chuỗi thay đổi kỳ vọng

```text
Học viên nhận ra mình chưa hiểu
→ chủ động yêu cầu trợ giúp
→ xác định đúng lỗ hổng kiến thức nền
→ ôn lại phần kiến thức cần thiết
→ hiểu được nội dung đang học
→ tiếp tục bài thay vì bỏ dở hoặc học đối phó
```

- Output do hệ thống tạo: câu hỏi chẩn đoán và phần giải thích ngắn.
- Thay đổi hành vi cần có: học viên phải chủ động báo khó khăn, trả lời câu hỏi và sử dụng phần ôn lại.
- Outcome hệ thống chỉ có thể ảnh hưởng: học viên hiểu bài tốt hơn và tiếp tục học.

### 2.4. Actor Map

| Actor | Họ đang làm gì? | Pain/hậu quả có thể có | Lợi ích kỳ vọng |
|---|---|---|---|
| Học viên | Học bài và cố hiểu khái niệm mới | Không biết mình thiếu kiến thức nền nào; mất thời gian; bỏ dở | Khôi phục mạch hiểu và tiếp tục học |
| Giảng viên | Thiết kế bài và hỗ trợ nhiều học viên | Không biết ai đang mắc ở đâu; phản hồi chậm | Nhận diện điểm khó phổ biến, hỗ trợ đúng chỗ |
| Coach/TA | Trả lời câu hỏi và theo dõi tiến độ | Câu hỏi thiếu ngữ cảnh; hỗ trợ lặp lại | Có thêm ngữ cảnh để hỗ trợ nhanh hơn |

**Actor điều tra trước:** Học viên.

**Lý do:** Học viên là người trực tiếp trải nghiệm tình huống không hiểu bài, thực hiện workaround và chịu hậu quả ngay trong phiên học. Đây cũng là actor trực tiếp kích hoạt capability được đề xuất.

### 2.5. Situation & Job

**Mô tả Situation & Job:**

Khi đang học một bài có khái niệm mới và gặp đoạn không thể kết nối với kiến thức đã biết, học viên cố hiểu đủ để tiếp tục bài bằng cách đọc lại, xem lại ví dụ, tìm kiếm bên ngoài hoặc hỏi người khác; họ bắt đầu mắc kẹt khi không xác định được chính xác mình thiếu kiến thức nào.

**JTBD Hypothesis:**

> Khi gặp một phần bài học mà tôi chưa hiểu, tôi muốn nhanh chóng xác định điều mình đang thiếu và được giải thích theo đúng mức kiến thức hiện tại, để có thể tiếp tục học mà không mất mạch hoặc bỏ dở.

### 2.6. Hai Pain Hypothesis cạnh tranh

**Pain Hypothesis A — thiếu khả năng chẩn đoán lỗ hổng:**

> Khi gặp một đoạn khó trong bài học, học viên gặp khó khăn trong việc tiếp tục học vì không xác định được khái niệm nền nào mình đang thiếu, dẫn đến đọc lại không hiệu quả, tìm kiếm lan man, mất thời gian và có thể bỏ dở bài.

**Pain Hypothesis B — thiếu cách giải thích phù hợp:**

> Khi gặp một đoạn khó trong bài học, học viên gặp khó khăn trong việc tiếp tục học vì nội dung hiện tại được giải thích quá nhanh, quá trừu tượng hoặc không phù hợp với cách họ tiếp thu, dẫn đến phải tìm nguồn giải thích khác và mất mạch học.

**Giả thuyết điều tra trước:** A.

**Lý do chọn:** Solution directive dành phần lớn logic cho chẩn đoán trước khi giải thích. Tuy nhiên, đây chỉ là giả thuyết xuất phát từ solution và phải được kiểm chứng bằng hành vi thực tế.

### 2.7. Evidence Map

| Cần kiểm tra | Evidence làm nhóm tin hơn | Evidence làm nhóm nghi ngờ/bác bỏ |
|---|---|---|
| Situation có thật | Người học kể được một lần cụ thể trong 7 ngày gần đây, gồm bài nào, đoạn nào và chuyện gì xảy ra | Chỉ nói chung chung; không nhớ lần cụ thể; hiếm khi bị mắc |
| Pain có ý nghĩa | Phiên học bị gián đoạn đáng kể, phải bỏ đoạn/bỏ bài hoặc ảnh hưởng bài tập | Chỉ khó chịu nhẹ và tự xử lý trong vài phút |
| Workaround tồn tại | Đọc lại nhiều lần, Google/YouTube, hỏi bạn/giảng viên, dùng AI Chat hoặc đổi tài liệu | Không làm gì vì không đáng để xử lý |
| Chi phí/hậu quả tồn tại | Mất nhiều thời gian, mất tập trung, hiểu sai, trả lời sai hoặc bỏ dở | Không có hậu quả quan sát được |
| Pattern có lặp | Có nhiều sự kiện tương tự trong thời gian gần đây | Chỉ là một trường hợp đặc biệt |
| Chẩn đoán là nút thắt | Người học không biết nên hỏi gì/tìm gì; tìm kiếm lan man | Người học biết chính xác phần thiếu nhưng chỉ cần lời giải thích tốt hơn |
| Mức độ chủ động | Đã tự tìm nhiều cách hoặc nhờ người khác hỗ trợ | Không chủ động xử lý dù có cơ hội và chi phí thấp |

### 2.8. Problem Hypothesis

> Khi học một nội dung mới có phụ thuộc vào kiến thức nền, học viên VLearn đã từng mắc kẹt trong bảy ngày gần đây gặp khó khăn trong việc tiếp tục bài vì không xác định được chính xác phần kiến thức nền mình còn thiếu. Họ phải thử nhiều cách như đọc lại, tìm nguồn bên ngoài, hỏi người khác hoặc dùng AI Chat; việc này làm gián đoạn mạch học, tốn thời gian và đôi khi khiến họ bỏ qua hoặc bỏ dở nội dung.

**Điều phải đúng để giả thuyết đứng vững:**

1. Tình huống mắc kẹt xảy ra đủ gần đây và đủ thường xuyên.
2. Người học không chỉ thiếu lời giải thích mà còn không xác định được lỗ hổng kiến thức.
3. Workaround hiện tại có chi phí hoặc hiệu quả thấp.
4. Hậu quả đủ đáng kể để người học chủ động tìm cách xử lý.

**Điều có thể khiến nhóm sửa hoặc bác bỏ:**

1. Phần lớn người học biết chính xác mình thiếu gì và chỉ cần cách giải thích khác.
2. Họ tự xử lý nhanh bằng công cụ hiện có, không có hậu quả đáng kể.
3. Tình huống hiếm khi xảy ra hoặc chỉ xuất hiện do chất lượng một bài học cụ thể.
4. Nguyên nhân chính là thiếu động lực, thời gian hoặc sự tập trung chứ không phải kiến thức nền.

### 2.9. Solution Parking Lot

| # | Hướng giải quyết có thể có | AI/Không AI |
|---|---|---|
| 1 | Cây prerequisite cho từng bài, cho phép quay lại đúng khái niệm nền | Không AI |
| 2 | Bộ câu hỏi tự kiểm tra ngắn trước hoặc trong bài | Không AI |
| 3 | Nút yêu cầu coach/TA hỗ trợ kèm vị trí đang học | Không AI |
| 4 | AI đặt câu hỏi chẩn đoán và tạo phần ôn tập cá nhân hóa | AI |
| 5 | AI gợi ý nguồn học bổ sung dựa trên lỗi sai gần đây | AI |
| 6 | Nhóm học ngang hàng theo chủ đề đang gặp khó khăn | Không AI |

## 3. Conversation Guide — phiên bản trước khi luyện

### 3.1. Big 3

| Điều cần học | Evidence cần tìm | Điều khiến nhóm xem lại giả thuyết |
|---|---|---|
| Tình huống mắc kẹt gần nhất diễn ra thế nào? | Một sự kiện cụ thể, trigger, mục tiêu và trình tự | Không kể được sự kiện gần đây hoặc sự kiện không ảnh hưởng việc học |
| Người học đã làm gì để xử lý? | Hành vi thật, workaround, thời gian/công sức | Tự xử lý ngay bằng cách sẵn có, gần như không có chi phí |
| Nút thắt là không biết mình thiếu gì hay thiếu cách giải thích phù hợp? | Dấu hiệu tìm kiếm lan man, không biết hỏi gì, hoặc ngược lại biết rõ phần thiếu | Nguyên nhân chính là động lực, thời gian, giao diện hoặc chất lượng bài cụ thể |

**Câu hỏi đáng sợ:** Nếu người học đã biết chính xác mình không hiểu gì và luôn xử lý được nhanh bằng công cụ hiện có, giả thuyết “thiếu khả năng chẩn đoán lỗ hổng kiến thức” cần được thay đổi.

### 3.2. Tiêu chí tuyển người

Người đã có ít nhất một lần không hiểu một phần bài học và phải tìm cách xử lý trong vòng **7 ngày gần đây**.

**Recruitment check:**

> Trong bảy ngày vừa qua, bạn có lần nào đang học nhưng gặp một đoạn không hiểu và phải làm gì đó để tiếp tục không?

### 3.3. Lời mở đầu

> Cảm ơn bạn đã tham gia. Nhóm mình đang tìm hiểu cách mọi người xử lý khi gặp một phần khó hiểu trong quá trình học. Mình muốn nghe về trải nghiệm thực tế gần đây của bạn; không có câu trả lời đúng hay sai. Buổi trao đổi kéo dài khoảng 15 phút. Với sự đồng ý của bạn, mình muốn ghi âm chỉ để xem lại và phục vụ bài học, không chia sẻ công khai. Bạn có đồng ý không?

Chỉ bắt đầu ghi âm sau khi người tham gia đồng ý rõ ràng.

### 3.4. Story opener

> Kể mình nghe về lần gần nhất trong bảy ngày vừa qua bạn đang học một bài nhưng gặp một phần không hiểu và phải tìm cách xử lý?

### 3.5. Big 3 Questions

1. Lúc đó bạn đang học gì, muốn hoàn thành việc gì và chuyện gì khiến bạn nhận ra mình đang mắc?
2. Sau khi nhận ra mình chưa hiểu, bạn đã làm gì tiếp theo? Hãy kể theo đúng trình tự.
3. Ở thời điểm đó, phần khó nhất là không biết mình đang thiếu kiến thức nào, hay bạn đã biết phần thiếu nhưng chưa tìm được cách giải thích phù hợp? Điều gì khiến bạn nói vậy?

### 3.6. Probe bank

- Lúc đó chuyện gì xảy ra tiếp theo?
- Bạn đã làm gì đầu tiên?
- Vì sao bạn chọn cách đó?
- Bạn đã tìm bằng từ khóa hoặc câu hỏi nào?
- Bạn đã thử cách nào khác chưa?
- Bạn mất khoảng bao lâu?
- Kết quả cuối cùng thế nào?
- Việc đó ảnh hưởng phần còn lại của buổi học ra sao?
- Lần gần nhất trước đó là khi nào?
- Có chi tiết nào khiến bạn quyết định tiếp tục hoặc bỏ qua?

### 3.7. Câu hỏi cần tránh

- Bạn có muốn có nút “Tôi vẫn chưa hiểu” không?
- AI Tutor có hữu ích với bạn không?
- Nếu AI hỏi ba câu rồi giải thích lại, bạn có dùng không?
- Bạn có thường xuyên không hiểu bài không?
- Bạn nghĩ tính năng nào sẽ giải quyết vấn đề này?

## 4. Conversation Guide — phiên bản cuối

> Phiên bản này được chỉnh sau cuộc phỏng vấn trực tiếp với Nguyễn Minh Đức — 2A202601946.

### Thay đổi sau phần luyện phỏng vấn

- Đổi câu hỏi lựa chọn thành câu hỏi mở để giảm dẫn dắt.
- Thêm probe về từ khóa tìm kiếm, cách chọn nguồn và thời điểm dừng tìm.
- Giữ trọng tâm vào hành vi đã xảy ra, không yêu cầu đánh giá solution.

### Guide cuối

1. Kể mình nghe về lần gần nhất trong bảy ngày vừa qua bạn gặp một phần bài học không hiểu?
2. Khi đó bạn đang học gì và muốn hoàn thành việc gì?
3. Chi tiết nào khiến bạn nhận ra mình đang mắc?
4. Sau đó bạn đã làm gì? Hãy kể theo đúng trình tự.
5. Khi bắt đầu tìm cách xử lý, bạn nghĩ nguyên nhân là gì?
6. Bạn đã tìm bằng từ khóa hoặc câu hỏi nào?
7. Bạn chọn nguồn để xem dựa trên điều gì?
8. Cách nào có ích và cách nào không có ích? Chuyện gì đã xảy ra?
9. Bạn mất bao lâu và việc đó ảnh hưởng phần còn lại của buổi học ra sao?
10. Điều gì khiến bạn quyết định tiếp tục tìm, bỏ qua hoặc dừng lại?

## 5. Practice Reflection

1. **Câu hỏi nào giúp user kể một tình huống cụ thể?**  
   Câu “Sau đó bạn đã làm gì?” giúp người được hỏi kể việc đọc bài hai lần, tìm Google rồi xem YouTube thay vì chỉ nói chung là gặp khó khăn.

2. **Chỗ nào cần làm tốt hơn trong lần phỏng vấn thật?**  
   Câu hỏi đưa sẵn hai khả năng có thể làm người trả lời chọn theo gợi ý. Lần sau cần hỏi mở trước, nghe câu trả lời rồi mới đào sâu.

3. **Sau phần luyện phỏng vấn, Conversation Guide được sửa ở đâu và vì sao?**  
   Guide được bổ sung câu hỏi về từ khóa tìm kiếm, cách chọn nguồn và thời điểm dừng tìm. Các câu này giúp làm rõ workaround và chi phí.

## 6. AI Support Log

- AI hỗ trợ cấu trúc hóa chuỗi Solution → Change → Actor → Situation & Job → Pain → Evidence.
- AI gợi ý hai Pain Hypothesis cạnh tranh, Evidence Map, Big 3 và Conversation Guide.
- Các nội dung trên vẫn là giả thuyết, không phải fact về học viên.
- AI hỗ trợ định dạng nội dung phỏng vấn do người nộp cung cấp và gợi ý Practice Reflection.
- Người nộp xác nhận nội dung cung cấp là cuộc phỏng vấn thật. AI không tự tạo thêm dữ liệu hoặc quote ngoài nội dung được cung cấp.

## Tuyên bố trạng thái

Case A hiện ở trạng thái **problem hypothesis practiced with one interview**, chưa được tuyên bố là validated. Một cuộc phỏng vấn luyện tập chưa đủ để xác nhận pain cho toàn bộ nhóm người dùng.
