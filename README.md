Hãy đọc toàn bộ cuốn sách PDF này và chưng cất thành một tài liệu tham chiếu HTML hoàn chỉnh.
Thực hiện đúng theo quy trình sau, không bỏ qua bước nào.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
BƯỚC 1 — ĐỌC TOÀN BỘ
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Chạy lệnh: pdftotext "[tên file]" /tmp/book.txt
Đọc toàn bộ nội dung file đó trước khi viết bất cứ thứ gì.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
BƯỚC 2 — NGUYÊN TẮC NGÔN NGỮ (BẮT BUỘC)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Tài liệu này phải đọc được bởi người KHÔNG giỏi tiếng Anh.
Áp dụng các quy tắc sau xuyên suốt toàn bộ nội dung:

① GIẢI THÍCH INLINE — mọi thuật ngữ tiếng Anh khi xuất hiện lần đầu
   trong phần thân (prose, cards, tables) phải có giải thích ngay bên cạnh.

   Cách viết ĐÚNG:
   → "Aggregate (nhóm object dùng chung một ranh giới giao dịch)"
   → "Idempotent — tức là gọi một lần hay mười lần kết quả vẫn như nhau"
   → "Bounded Context (vùng ranh giới rõ ràng): mỗi vùng có ngôn ngữ riêng"

   Cách viết SAI (không được dùng):
   ✗ "Aggregate là một pattern quan trọng trong DDD"  ← không giải thích
   ✗ Để thuật ngữ kỹ thuật trơn không có chú thích

② VIẾT TIẾNG VIỆT LÀ CHÍNH
   - Câu văn diễn giải: viết tiếng Việt hoàn toàn
   - Thuật ngữ gốc tiếng Anh: giữ nguyên nhưng kèm giải thích ngay sau (xem ①)
   - Không dịch tên công nghệ đã phổ biến (Kafka, REST, Docker, AWS...)

③ DÙNG VÍ DỤ ĐỜI THƯỜNG để giải thích khái niệm trừu tượng
   Mỗi khái niệm khó → thêm một ví dụ từ cuộc sống thực.
   Ví dụ tốt:
   "Value Object giống như tờ tiền 100k — bạn không quan tâm
   tờ nào cụ thể, chỉ quan tâm mệnh giá. Hai tờ 100k là hoàn toàn
   như nhau và có thể đổi cho nhau."

④ VIẾT NGẮN, RÕ, KHÔNG VÒNG VO
   - Một câu = một ý duy nhất
   - Ưu tiên danh sách bullet hơn đoạn văn dài
   - Tránh dùng từ hoa mỹ khi từ đơn giản đã đủ nghĩa

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
BƯỚC 3 — CẤU TRÚC FILE HTML
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Thiết kế tổng thể:
- Font chữ: IBM Plex Mono (nhãn/code), Source Serif 4 (thân bài), Playfair Display (tiêu đề)
- Màu nền trang: #f5f0e8 | Màu chữ chính: #1a1208
- Cỡ chữ thân bài: 15px | Khoảng cách dòng: 1.7
- Chiều rộng tối đa: 900px, căn giữa trang

Các khối bắt buộc theo thứ tự:

[1] COVER — nền tối #1a1208, chữ sáng
    - Tên sách (dịch tiếng Việt nếu có) + tác giả + năm xuất bản
    - Mô tả 1–2 câu tiếng Việt: sách này về gì, đọc xong biết được gì
    - Thống kê: số trang, số chương, số phần

[2] MỤC LỤC NHANH — nền #ede6d3
    - Anchor links đến từng section
    - Hiển thị dạng lưới 2 cột
    - Tên chương viết tiếng Việt (kèm số chương)

[3] NỘI DUNG CHÍNH
    Mỗi chương là một .section gồm:
    - Badge: "Chương X"
    - H2: tên chương bằng tiếng Việt
    - Nội dung: prose, cards, tables, callouts, blockquotes
    - GLOSSARY FOOTER ở cuối (xem Bước 4)

[4] PHẦN PHẢN BIỆN — tiêu đề: "Căn cứ Tranh luận & Phản biện"
    - 6–10 câu hỏi phản biện thực tế về chủ đề của sách
    - Mỗi câu hỏi: hộp tiêu đề (câu hỏi) + phần đáp (lý luận dựa trên sách)
    - Viết hoàn toàn bằng tiếng Việt

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
BƯỚC 4 — GLOSSARY FOOTER (bảng thuật ngữ cuối chương)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Cuối MỖI section bắt buộc có một khối glossary.

Quy tắc hình thức:
- Nền trắng #ffffff
- Viền trên: 3px solid #c8922a (vàng)
- Viền ngoài: 1.5px solid #d4c9b0 (nhạt)
- Nhãn tiêu đề: "📖 THUẬT NGỮ XUẤT HIỆN TRONG CHƯƠNG NÀY"
- Tên thuật ngữ: font monospace, đậm, màu #b5451b
- Định nghĩa: 13px, màu #4a4035

Quy tắc nội dung:
- Chỉ liệt kê thuật ngữ XUẤT HIỆN LẦN ĐẦU trong section này
- Thuật ngữ đã giải thích ở section trước → KHÔNG lặp lại
- Mỗi định nghĩa phải có đủ 3 yếu tố:
    (a) Là gì — giải thích bằng tiếng Việt đơn giản nhất
    (b) Dùng khi nào / không dùng khi nào
    (c) Ví dụ cụ thể (bắt buộc nếu khái niệm trừu tượng)

Ví dụ định nghĩa ĐÚNG:
  "Aggregate — Nhóm các object được quản lý cùng nhau, chỉ có một
  cửa vào duy nhất gọi là aggregate root (gốc của nhóm). Dùng khi
  cần đảm bảo dữ liệu nhất quán trong một thao tác. Ví dụ: Đơn hàng
  (Order) và danh sách sản phẩm trong đơn (OrderItem) là một nhóm —
  không ai được sửa OrderItem trực tiếp, phải đi qua Order."

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
BƯỚC 5 — NỘI DUNG MỖI CHƯƠNG
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Mỗi chương phải có đủ các mục sau (nếu sách có đề cập):

✅ Định nghĩa    — "X là gì?" viết bằng tiếng Việt, có ví dụ
✅ Tại sao cần  — vấn đề gì tồn tại trước khi có X
✅ Cách hoạt động — ngắn gọn, theo bước nếu phù hợp
✅ Bảng so sánh — khi có nhiều loại/biến thể của cùng một khái niệm
✅ Khi nào dùng / không dùng — hộp ghi chú màu xanh lá
✅ Sai lầm phổ biến — hộp ghi chú màu đỏ
✅ Quy tắc nhanh để nhớ — hộp ghi chú màu vàng
✅ Ví dụ thực tế — lấy từ sách hoặc tự đặt ra gần với thực tế

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
BƯỚC 6 — CSS COMPONENTS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

/* Hộp ghi chú (callout) */
.callout        → viền vàng #c8922a, nền #fff3cd  — quy tắc nhanh
.callout.danger → viền đỏ #b5451b, nền #fdf0ec   — sai lầm phổ biến
.callout.tip    → viền xanh #5a7a5e, nền #edf4ee — khi nào dùng

/* Thẻ thông tin (cards) */
.cards → grid tự động, tối thiểu 260px/thẻ, gap 16px
.card  → nền trắng, viền nhạt, thanh màu bên trái 4px, border-radius 8px

/* Cây quyết định (decision tree) */
.dtree → nền tối #1a1208, font monospace, border-radius 10px
  .q   → câu hỏi, màu vàng #c8922a
  .a   → nhánh trả lời, màu xanh nhạt #a8d8b0, thụt vào 24px
  .r   → kết quả cuối, màu cam #f4a87a, đậm, thụt vào 48px

/* Phần phản biện (debate) */
.debate-header → nền #3d4f5c, chữ trắng, font monospace 12px
.debate-body   → padding 14px, font 14px, nền trắng

/* Bảng thuật ngữ (glossary) */
.glossary      → nền #fff, viền trên 3px #c8922a, viền 1.5px #d4c9b0
.gterm         → dạng grid 2 cột: tên | định nghĩa, padding 9px 0
.gterm-word    → monospace, đậm, màu #b5451b, không xuống dòng
.gterm-def     → 13px, màu #4a4035, line-height 1.6

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
BƯỚC 7 — OUTPUT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

- Lưu file tại: /mnt/user-data/outputs/[tên-sách]-mastery-guide.html
- Gọi present_files để chia sẻ file với người dùng
- File phải tự hoạt động được (chỉ cần Google Fonts là dependency ngoài)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
TIÊU CHÍ THÀNH CÔNG
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Người đọc file HTML này — kể cả người KHÔNG biết tiếng Anh — phải có thể:
① Hiểu 100% nội dung sách mà không cần mở bản gốc
② Tra cứu nhanh bất kỳ khái niệm nào khi làm việc thực tế
③ Có đủ căn cứ để tranh luận, bảo vệ hoặc phản bác các luận điểm trong sách
