#   BÀI LÀM: SO SÁNH HAI CHIẾN LƯỢC VIẾT PROMPT

## Phần 1. Phân tích và đề xuất

### 1. Xác định đầu vào và đầu ra

**Đầu vào:** Người dùng là sinh viên năm nhất PTIT, chưa có nền tảng lập trình và muốn hiểu khái niệm **Markdown Parser** ở mức cơ bản.

**Đầu ra:** AI cần giải thích dễ hiểu, phù hợp với người mới. Riêng Prompt của Minh yêu cầu rõ thêm:

-   Sử dụng ngôn ngữ đời thường và phép so sánh quen thuộc.
-   Trình bày trong khoảng 100–150 từ.
-   Có một câu Markdown minh họa và kết quả hiển thị.
-   Tránh thuật ngữ phức tạp và ví dụ code lập trình.

### 2. Ưu điểm và nhược điểm của hai chiến lược

**Chiến lược A — Văn xuôi thuần túy**

_Ưu điểm:_

-   Cách viết tự nhiên, dễ áp dụng ngay.
-   Prompt trong đề ngắn hơn, thường tốn ít token đầu vào hơn.
-   Đã nêu được trình độ người hỏi và mong muốn hiểu cơ bản.

_Nhược điểm:_

-   Yêu cầu “không cần quá chi tiết” chưa xác định rõ độ dài.
-   Chưa yêu cầu ví dụ nên câu trả lời có thể thiếu minh họa.
-   Khi có nhiều yêu cầu, người viết dễ bỏ sót hoặc trình bày lẫn nhau.

**Chiến lược B — Cấu trúc Markdown**

_Ưu điểm:_

-   Tách rõ bối cảnh, nội dung cần hỏi và yêu cầu trả lời.
-   Giúp AI nhận biết rõ hơn độ dài, cách diễn đạt và ví dụ cần có.
-   Dễ tái sử dụng bằng cách thay tên khái niệm.
-   Người dùng dễ kiểm tra xem đã nêu đủ yêu cầu chưa.

_Nhược điểm:_

-   Prompt trong đề dài hơn, thường sử dụng nhiều token đầu vào hơn.
-   Cần làm quen với tiêu đề và danh sách Markdown.
-   Có thể rườm rà với câu hỏi đơn giản.

**Nhận xét:** Lợi thế của B chủ yếu đến từ **yêu cầu cụ thể và cách tổ chức rõ ràng**. Chỉ thêm tiêu đề Markdown không bảo đảm AI trả lời chính xác hơn.

## Phần 2. So sánh và lựa chọn

### 3. Bảng so sánh theo bốn tiêu chí

|Tiêu chí|Chiến lược A — Văn xuôi|Chiến lược B — Markdown|
|-|-|-|
|**Độ chính xác theo nhu cầu**|Nêu đúng trình độ nhưng yêu cầu đầu ra còn chung chung|Nêu rõ trình độ, độ dài, ví dụ và giới hạn nên dễ đáp ứng đúng nhu cầu hơn|
|**Tiêu thụ token**|Prompt trong đề ngắn hơn, thường ít token đầu vào hơn.|Prompt trong đề dài hơn, thường nhiều token đầu vào hơn.|
|**Khả năng tái sử dụng**|Có thể dùng lại nhưng phải tìm và sửa nội dung trong đoạn văn.|Dễ dùng làm mẫu, chỉ cần thay mục “Khái niệm cần giải thích”.|
|**Dễ học cho người mới**|Rất dễ, có thể viết như đang trò chuyện.|Cần biết một ít Markdown nhưng có thể áp dụng nhanh theo mẫu.|


_Lưu ý: Tổng lượng token còn gồm câu trả lời của AI. Prompt ngắn hơn chưa chắc làm toàn bộ cuộc trao đổi ít token hơn nếu phải hỏi lại nhiều lần._

### 4. Lựa chọn theo bối cảnh

**Nên dùng chiến lược A khi:**

-   Hỏi nhanh một kiến thức đơn giản.
-   Chỉ cần câu trả lời ngắn, không có nhiều điều kiện.
-   Đang trao đổi tiếp trong cuộc trò chuyện đã có đủ bối cảnh.

Ví dụ: “Giải thích Markdown Parser trong hai câu dễ hiểu cho sinh viên năm nhất.”

**Nên dùng chiến lược B khi:**

-   Ôn tập nhiều khái niệm theo cùng một mẫu.
-   Muốn kiểm soát độ dài, cách giải thích và ví dụ.
-   Cần câu trả lời có hình thức thống nhất để ghi chép, so sánh.

**Lựa chọn của em:** Với việc ôn thi của sinh viên năm nhất, em ưu tiên **chiến lược B** vì dễ dùng lại và giúp trình bày đầy đủ điều mình cần. Với câu hỏi ngắn, ít yêu cầu, em chọn A để tiết kiệm thời gian soạn.

## Phần 3. Thiết kế và triển khai

### 5. Prompt mẫu hỏi về khái niệm “Token”

Em dùng ba phần chính và đặt nội dung “không cần” trong phần yêu cầu để giữ mẫu gọn:
```
`## Bối cảnh 
Tôi là sinh viên năm nhất ngành Công nghệ thông tin tại PTIT, mới học chưa đầy một học kỳ và chưa có nhiều kiến thức về AI. 
## Khái niệm cần giải thích 
Token trong mô hình AI ngôn ngữ như ChatGPT. 
## Yêu cầu 
- Giải thích bằng ngôn ngữ đời thường trong khoảng 100–150 từ. 
-  Dùng một phép so sánh quen thuộc để giúp tôi dễ hình dung. 
-  Cho ví dụ minh họa token có thể là một từ hoặc một phần của từ. 
- Nêu ngắn gọn vì sao số lượng token liên quan đến giới hạn nội dung và chi phí khi sử dụng API. 
- Không dùng code lập trình hoặc thuật ngữ kỹ thuật phức tạp. 
- Nếu minh họa cách chia token, ghi rõ đó chỉ là minh họa; cách chia thực tế phụ thuộc vào bộ tách token.
```
### 6. Trả lời hai bẫy dữ liệu

**Bẫy 1 — Đặt yêu cầu vào sai phần thì AI có hiểu không?**

AI **vẫn có thể hiểu** vì đọc nội dung toàn bộ Prompt, không chỉ dựa vào tên tiêu đề. Ví dụ, câu “Trả lời trong 100–150 từ” nằm trong phần “Bối cảnh” vẫn có thể được thực hiện.

Tuy nhiên, đặt sai phần khiến Prompt khó theo dõi, khó sửa và dễ gây hiểu nhầm khi có nhiều yêu cầu hoặc thông tin mâu thuẫn.

**Cách khắc phục:** Đặt thông tin người học trong “Bối cảnh”, tên kiến thức trong “Khái niệm”, còn độ dài và cách trả lời trong “Yêu cầu”.

**Bẫy 2 — Khi nào nên ưu tiên A vì ít token hơn?**

Nên ưu tiên A khi câu hỏi đơn giản, ít điều kiện hoặc cuộc trò chuyện đã có đủ bối cảnh. Khi đó, một câu văn ngắn nhưng rõ ý đã đáp ứng được nhu cầu.

Không nên chỉ chọn theo độ dài Prompt. Nếu A quá chung chung khiến phải hỏi lại nhiều lần, tổng token và thời gian trao đổi có thể nhiều hơn việc dùng B ngay từ đầu.
