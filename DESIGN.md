# DESIGN.md — Nhà hàng Bếp Lửa

Tài liệu thiết kế cho trang web nhà hàng Bếp Lửa (theo yêu cầu MSR-17, task TEC-133).
Mọi dữ liệu thật chưa có đều để placeholder rõ ràng, không bịa.

## 1. Bảng màu (mã hex kèm vai trò)

| Mã hex | Vai trò |
| --- | --- |
| `#141210` | Nền than — nền chính toàn trang, tạo cảm giác bếp than tối ấm |
| `#F3EAD9` | Chữ kem — chữ chính trên nền than, tiêu đề và nội dung |
| `#C96F2E` | Nhấn cam lửa — nút kêu gọi hành động, giá món, đường gạch nhấn, liên kết khi hover |
| `#241E19` | Nền thẻ phụ — nền của thẻ món ăn, thẻ không gian, khung form (tông than sáng hơn nền chính một bậc, vẫn tối ấm) |
| `#8A7B68` | Chữ phụ — mô tả phụ, ghi chú, giờ mở cửa, chú thích ảnh (kem pha xám, độ tương phản thấp hơn chữ chính) |

Quy tắc dùng màu: nền luôn tối (`#141210` hoặc `#241E19`); chữ chính luôn kem `#F3EAD9`; màu cam lửa `#C96F2E` chỉ dùng điểm nhấn, không dùng làm nền diện rộng.

## 2. Font chữ

- **Font tiêu đề: Playfair Display** — dùng cho tên nhà hàng, tiêu đề section, tên món ăn. Kiểu serif cổ điển, hợp không khí fine dining.
- **Font nội dung: Be Vietnam Pro** — dùng cho mô tả món, câu chuyện, chú thích, nhãn form, nút bấm. Hiển thị tốt tiếng Việt có dấu.
- Cỡ chữ chốt: tiêu đề hero 56–64px (desktop) / 36px (mobile); tiêu đề section 32px; tên món 20px; nội dung 16px; chú thích 14px.

## 3. Phong cách tham chiếu (MỘT phong cách duy nhất)

**Fine dining nền tối, ấm, điện ảnh** — không gian tối như phòng ăn buổi tối bên bếp than, ánh sáng ấm tập trung vào món ăn, ảnh có chiều sâu và bóng đổ mềm như một khung hình phim. Toàn bộ trang tuân theo đúng một phong cách này, không pha thêm phong cách khác.

## 4. Quy tắc hình ảnh

- **Ảnh lớn làm nội dung chính:** ảnh là nội dung chính của trang, không phải ảnh trang trí nhỏ. Mỗi section dùng ảnh lớn, chiếm phần lớn chiều rộng section.
- **Đồng tông tối ấm:** mọi ảnh mẫu phải tông tối, ấm (ánh lửa, gỗ, than), không dùng ảnh sáng trắng, lạnh.
- **Khung hero toàn màn hình:** ảnh hero là ảnh món ăn, chiếm toàn bộ màn hình đầu tiên (100vh), chữ tên nhà hàng và nút đặt bàn đặt chồng lên ảnh, có lớp phủ than mờ để chữ kem đọc được.
- **Lưới ảnh không gian lớn:** lưới ảnh không gian dùng ô ảnh lớn (tối thiểu 2 cột desktop, ảnh cao), không dùng lưới ảnh nhỏ dày đặc.
- **Nhiều khoảng trắng:** giữa các section chừa khoảng trống lớn (tối thiểu 96px desktop), không nhồi nội dung sát nhau.
- **Tỉ lệ khung:** hero 16:9 toàn màn hình; ảnh món ăn 4:3; ảnh không gian 3:2.
- **Ảnh mẫu:** mọi ảnh ở bản đầu tiên là ảnh mẫu chất lượng cao, ghi rõ là ảnh mẫu trong phần chú thích cho đến khi khách cung cấp ảnh thật.

## 5. Cấu trúc trang (theo đúng thứ tự)

1. **Hero:** ảnh món ăn toàn màn hình; tên "Bếp Lửa"; dòng giới thiệu ngắn về bếp than; nút "Đặt bàn".
2. **Câu chuyện bếp than:** đoạn văn ngắn về bếp than và ẩm thực Việt đương đại; kèm 1 ảnh bếp lửa lớn.
3. **Thực đơn theo mùa:** danh sách món theo mùa; mỗi món gồm ảnh (4:3) + tên món + mô tả ngắn + giá mẫu (ghi rõ "giá mẫu, chờ khách xác nhận").
4. **Lưới ảnh không gian:** lưới ảnh lớn về không gian quán (tối thiểu 4 ảnh, tỉ lệ 3:2).
5. **Giới thiệu bếp trưởng:** [PLACEHOLDER — chưa có thông tin bếp trưởng thật: tên, ảnh, tiểu sử đều để trống chờ khách cung cấp, không bịa].
6. **Form đặt bàn:** chỉ giao diện (chưa nối backend): các trường họ tên, số điện thoại, ngày, giờ, số khách; nút gửi chỉ hiển thị, chưa gửi dữ liệu thật.
7. **Thông tin chung:** giờ mở cửa mẫu 17:00–23:00 (ghi rõ là giờ mẫu); địa chỉ [PLACEHOLDER — chờ khách cung cấp]; điện thoại [PLACEHOLDER — chờ khách cung cấp].

## 6. Ghi chú placeholder

- Địa chỉ, điện thoại, tên và tiểu sử bếp trưởng, giá món thật, ảnh thật: tất cả đều là placeholder cho đến khi khách cung cấp.
- Không dùng tên người thật, thương hiệu thật hay số liệu thật nào ngoài các thông số thiết kế đã chốt ở mục 1–4.
