Hãy đọc toàn bộ cuốn sách PDF này và chưng cất thành một tài liệu tham chiếu HTML hoàn chỉnh theo đúng quy trình sau:

---

**BƯỚC 1 — ĐỌC TOÀN BỘ**
Dùng pdftotext để extract toàn bộ text. Đọc hết trước khi viết bất cứ thứ gì.

---

**BƯỚC 2 — TẠO FILE HTML** theo cấu trúc bắt buộc:

### Thiết kế tổng thể
- Font: IBM Plex Mono (labels/code), Source Serif 4 (body), Playfair Display (headings)
- Màu nền: #f5f0e8 (paper), text: #1a1208
- Font size body: 15px, line-height: 1.7
- Max-width: 900px, centered

### Cấu trúc bắt buộc của file HTML:

1. **COVER** (nền tối #1a1208)
   - Tên sách + tác giả
   - Mô tả 1-2 câu
   - Metadata: số trang, số chương

2. **TOC** (mục lục nhanh, nền #ede6d3)
   - Links anchor đến từng section
   - Grid 2 cột

3. **MAIN CONTENT** — mỗi chương/phần là một `.section` gồm:
   - Badge (tên phần/số chương)
   - H2 title
   - Nội dung chính: prose, cards, tables, callouts, blockquotes
   - **GLOSSARY FOOTER** (xem quy tắc bên dưới)

4. **PHẦN ĐẶC BIỆT: "Căn cứ Lập luận & Phản biện"**
   - 6-10 câu hỏi phản biện thường gặp về chủ đề sách
   - Mỗi câu: debate-header (câu hỏi) + debate-body (đáp luận có dẫn chứng từ sách)

---

### GLOSSARY FOOTER — Quy tắc bắt buộc

Cuối MỖI section phải có một glossary block:
- Nền trắng `#ffffff`, border top vàng `3px solid #c8922a`
- Label: "📖 THUẬT NGỮ XUẤT HIỆN TRONG CHƯƠNG NÀY"
- Chỉ liệt kê thuật ngữ **lần đầu tiên xuất hiện** trong section đó
- Thuật ngữ đã có ở section trước → KHÔNG lặp lại
- Mỗi entry: tên term (monospace, màu rust #b5451b) + định nghĩa tiếng Việt ngắn gọn (13px)
- Định nghĩa phải: (a) giải thích bằng ngôn ngữ đơn giản, (b) nêu khi nào dùng/không dùng nếu có, (c) cho ví dụ cụ thể nếu giúp hiểu hơn

---

### CSS Components cần có

```css
/* Callout boxes */
.callout { border-left: 4px solid #c8922a; background: #fff3cd; padding: 16px 20px; }
.callout.danger { border-color: #b5451b; background: #fdf0ec; }
.callout.tip { border-color: #5a7a5e; background: #edf4ee; }

/* Cards grid */
.cards { display: grid; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); gap: 16px; }
.card { background: white; border: 1px solid #d4c9b0; border-radius: 8px; padding: 20px; }
.card::before { content:''; position:absolute; top:0;left:0; width:4px; height:100%; background:#c8922a; }

/* Decision tree (dark bg) */
.dtree { background: #1a1208; color: #f5f0e8; border-radius: 10px; font-family: monospace; }

/* Debate */
.debate-header { background: #3d4f5c; color: #f5f0e8; font-family: monospace; font-size: 12px; }

/* Glossary */
.glossary { background: #fff; border-top: 3px solid #c8922a; border: 1.5px solid #d4c9b0; }
.gterm-word { font-family: monospace; font-weight: 600; color: #b5451b; }
.gterm-def { font-size: 13px; color: #4a4035; }
```

---

### Nội dung mỗi section phải có đủ

- **Định nghĩa rõ ràng** của mọi khái niệm chính
- **Bảng so sánh** khi có nhiều variants (ví dụ: 3 loại subdomain, các patterns)
- **Khi nào dùng / không dùng** cho mọi pattern/tool
- **Sai lầm phổ biến** (callout.danger) nếu có trong sách
- **Rule of thumb** (callout) để nhớ nhanh
- **Ví dụ thực tế** từ sách nếu có

---

**BƯỚC 3 — OUTPUT**
- Lưu file: `/mnt/user-data/outputs/[tên-sách]-mastery-guide.html`
- Dùng `present_files` để share
- File phải self-contained (không cần internet trừ Google Fonts)

---

**MỤC TIÊU**: Người đọc file HTML này phải có thể:
1. Hiểu 100% nội dung sách mà không cần đọc sách gốc
2. Dùng làm reference khi làm việc thực tế
3. Có đủ căn cứ để tranh luận và phản biện về chủ đề
