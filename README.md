# Thửa đất & quy hoạch TP. Hồ Chí Minh – MCP

Kết nối trợ lý AI (Claude, ChatGPT, Cursor…) với dữ liệu thửa đất tại TP. Hồ Chí Minh trên [BumiAtlas](https://bumiatlas.com) qua Model Context Protocol (MCP).

- Tra cứu thửa đất theo số tờ bản đồ và số thửa như ghi trên sổ đỏ, sổ hồng (*"tờ 3 thửa 65, Bến Thành, Quận 1"*), theo mã thửa đất hoặc theo tọa độ
- Mục đích sử dụng đất (ODT đất ở đô thị, ONT đất ở nông thôn, LUC đất chuyên trồng lúa, CLN đất trồng cây lâu năm…), diện tích ghi nhận và diện tích theo ranh thửa
- Địa chỉ theo đơn vị hành chính mới (từ 1/7/2025) và địa chỉ cũ (phường, xã, quận, huyện) như trên giấy chứng nhận cấp trước đó; tìm bằng tên cũ hay tên mới, có dấu hoặc không dấu
- Quy hoạch phân khu tại TP. Hồ Chí Minh cũ (chưa có Bình Dương, Bà Rịa – Vũng Tàu): chức năng sử dụng đất của từng ô phố, mật độ xây dựng, hệ số sử dụng đất, tầng cao và chiều cao tối đa
- Ảnh vệ tinh hoặc bản đồ của thửa đất và các thửa xung quanh, mỗi thửa ghi số thửa

Từ 1/7/2025, TP. Hồ Chí Minh gồm cả tỉnh Bình Dương và Bà Rịa – Vũng Tàu cũ; dữ liệu phủ cả ba.

Dữ liệu là những gì các cổng thông tin công bố, nên chưa có đủ mọi thửa đất. Không có tên chủ sở hữu, số giấy chứng nhận hay giá đất.

## Kết nối

```
https://bumiatlas.com/mcp/hochiminh
```

Thêm địa chỉ này làm custom connector (trình kết nối tùy chỉnh) trong Claude, ChatGPT, Cursor hoặc ứng dụng khác hỗ trợ MCP, rồi đăng nhập bằng Google. Không cần API key. Hướng dẫn chi tiết: [bumiatlas.com/mcp-docs/hochiminh](https://bumiatlas.com/mcp-docs/hochiminh).

Tên công cụ bằng tiếng Anh, nhưng trợ lý vẫn trả lời bằng tiếng Việt. Đây là bộ công cụ Việt Nam của BumiAtlas, nên cũng tra cứu được thửa đất ở các tỉnh, thành khác.

## Công cụ

| Công cụ | Chức năng |
|---|---|
| `VN_parcel_search` | Tìm thửa đất theo mã thửa, theo số tờ và số thửa kèm địa danh, hoặc theo tọa độ `vĩ độ, kinh độ` |
| `VN_parcel_get` | Chi tiết một thửa: mục đích sử dụng, diện tích, địa chỉ mới và cũ, các khu quy hoạch phủ lên thửa; ranh thửa dạng GeoJSON |
| `VN_parcel_image` | Ảnh vệ tinh hoặc bản đồ quanh một thửa hay một điểm; các thửa trong khung hình được viền và ghi số thửa |
| `VN_zoning_get` | Khu quy hoạch tại một điểm (TP. Hồ Chí Minh và Đà Nẵng): cấp quy hoạch, chức năng sử dụng đất, mật độ xây dựng, hệ số sử dụng đất, tầng cao |

## Ví dụ câu hỏi

- *"Tìm thửa đất tờ 3 thửa 65, phường Bến Thành, Quận 1. Mục đích sử dụng và diện tích là bao nhiêu?"*
- *"Quy hoạch tại 10.7769, 106.7009 ở Quận 1 là gì? Hệ số sử dụng đất và chiều cao tối đa bao nhiêu?"*
- *"Thửa đất tại 10.97966, 106.66365 ở Thủ Dầu Một (Bình Dương cũ) là thửa nào?"*
- *"Tìm tờ 15 thửa 21, phường Thắng Tam, Vũng Tàu."*
- *"Cho tôi xem ảnh vệ tinh thửa đất tại 10.79344, 106.74035 ở Thảo Điền và các thửa xung quanh."*

## Nguồn dữ liệu

Thửa đất từ guland.vn, cenhomes và các cổng thông tin đất đai, quy hoạch: ungdung-sotnmt.baria-vungtau.gov.vn (Bà Rịa – Vũng Tàu), qhkhsdd.binhduong.gov.vn (Bình Dương) và quyhoach.hochiminhcity.gov.vn. Quy hoạch phân khu từ cổng thông tin quy hoạch TP. Hồ Chí Minh (quyhoach.hochiminhcity.gov.vn). Mỗi thửa ghi rõ nguồn.

## Các xã, phường có dữ liệu

Xếp theo quận, huyện, thị xã, thành phố cũ. Mỗi xã, phường mới (từ 1/7/2025) kèm các phường, xã, thị trấn cũ đã nhập vào.

### TP. Hồ Chí Minh cũ

#### Huyện Bình Chánh

- **Xã Bình Chánh**: Bình Chánh, Tân Quý Tây, An Phú Tây
- **Xã Bình Hưng**: Bình Hưng, Phong Phú
- **Xã Bình Lợi**: Lê Minh Xuân, Bình Lợi
- **Xã Hưng Long**: Đa Phước, Hưng Long, Quy Đức
- **Xã Tân Nhựt**: Tân Kiên, Tân Nhựt, Tân Túc
- **Xã Tân Vĩnh Lộc**: Vĩnh Lộc B, Phạm Văn Hai
- **Xã Vĩnh Lộc**: Vĩnh Lộc A, Phạm Văn Hai

#### Huyện Cần Giờ

- **Xã An Thới Đông**: An Thới Đông, Lý Nhơn
- **Xã Bình Khánh**: Bình Khánh, Tam Thôn Hiệp, An Thới Đông
- **Xã Cần Giờ**: Long Hòa, Cần Thạnh
- **Xã Thạnh An**: Thạnh An _(chỉ có ranh thửa và diện tích)_

#### Huyện Củ Chi

- **Xã An Nhơn Tây**: An Nhơn Tây, Phú Mỹ Hưng, An Phú
- **Xã Bình Mỹ**: Bình Mỹ, Trung An, Hòa Phú
- **Xã Củ Chi**: Tân Phú Trung, Tân Thông Hội, Phước Vĩnh An
- **Xã Nhuận Đức**: Trung Lập Hạ, Nhuận Đức, Phạm Văn Cội
- **Xã Phú Hòa Đông**: Tân Thạnh Đông, Phú Hòa Đông, Tân Thạnh Tây
- **Xã Tân An Hội**: Tân An Hội, Phước Hiệp, Củ Chi
- **Xã Thái Mỹ**: Trung Lập Thượng, Phước Thạnh, Thái Mỹ

#### Huyện Hóc Môn

- **Xã Bà Điểm**: Bà Điểm, Xuân Thới Thượng, Trung Chánh; Trung Mỹ Tây (Quận 12)
- **Xã Đông Thạnh**: Thới Tam Thôn, Đông Thạnh, Nhị Bình; Tân Chánh Hiệp (Quận 12)
- **Xã Hóc Môn**: Tân Hiệp, Tân Xuân, Hóc Môn
- **Xã Xuân Thới Sơn**: Tân Thới Nhì, Xuân Thới Sơn, Xuân Thới Đông

#### Huyện Nhà Bè

- **Xã Hiệp Phước**: Hiệp Phước, Nhơn Đức, Long Thới
- **Xã Nhà Bè**: Phước Kiển, Phú Xuân, Nhà Bè, Phước Lộc

#### Quận 1

- **Phường Bến Thành**: Phạm Ngũ Lão, Bến Thành, Nguyễn Thái Bình, Cầu Ông Lãnh
- **Phường Cầu Ông Lãnh**: Nguyễn Cư Trinh, Cầu Kho, Cô Giang, Cầu Ông Lãnh
- **Phường Sài Gòn**: Bến Nghé, Đa Kao, Nguyễn Thái Bình
- **Phường Tân Định**: Tân Định, Đa Kao

#### Quận 3

- **Phường Bàn Cờ**: Phường 4, Phường 5, Phường 3, Phường 2, Phường 1
- **Phường Nhiêu Lộc**: Phường 11, Phường 14, Phường 9, Phường 12
- **Phường Xuân Hòa**: Võ Thị Sáu

#### Quận 4

- **Phường Khánh Hội**: Phường 8, Phường 15, Phường 4, Phường 9
- **Phường Vĩnh Hội**: Phường 2, Phường 3, Phường 4, Phường 1
- **Phường Xóm Chiếu**: Phường 16, Phường 13, Phường 18, Phường 15

#### Quận 5

- **Phường An Đông**: Phường 5, Phường 9, Phường 7
- **Phường Chợ Lớn**: Phường 12, Phường 13, Phường 14, Phường 11
- **Phường Chợ Quán**: Phường 1, Phường 4, Phường 2

#### Quận 6

- **Phường Bình Phú**: Phường 10, Phường 11; Phường 16 (Quận 8)
- **Phường Bình Tây**: Phường 9, Phường 2
- **Phường Bình Tiên**: Phường 8, Phường 7, Phường 1
- **Phường Phú Lâm**: Phường 12, Phường 13, Phường 14

#### Quận 7

- **Phường Phú Thuận**: Phú Thuận, Phú Mỹ
- **Phường Tân Hưng**: Tân Hưng, Tân Kiểng, Tân Quy, Tân Phong
- **Phường Tân Mỹ**: Tân Phú, Phú Mỹ
- **Phường Tân Thuận**: Tân Thuận Đông, Tân Thuận Tây, Bình Thuận

#### Quận 8

- **Phường Bình Đông**: Phường 7, Phường 5, Phường 6; An Phú Tây (Huyện Bình Chánh)
- **Phường Chánh Hưng**: Phường 4, Rạch Ông, Hưng Phú, Phường 5
- **Phường Phú Định**: Phường 16, Phường 14, Xóm Củi, Phường 15

#### Quận 10

- **Phường Diên Hồng**: Phường 14, Phường 8, Phường 6
- **Phường Hòa Hưng**: Phường 12, Phường 13, Phường 15
- **Phường Vườn Lài**: Phường 9, Phường 1, Phường 4, Phường 10, Phường 2

#### Quận 11

- **Phường Bình Thới**: Phường 3, Phường 8, Phường 10
- **Phường Hòa Bình**: Phường 5, Phường 14
- **Phường Minh Phụng**: Phường 16, Phường 1, Phường 7
- **Phường Phú Thọ**: Phường 15, Phường 11

#### Quận 12

- **Phường An Phú Đông**: Thạnh Lộc, An Phú Đông
- **Phường Đông Hưng Thuận**: Tân Thới Nhất, Đông Hưng Thuận, Tân Hưng Thuận
- **Phường Tân Thới Hiệp**: Hiệp Thành, Tân Thới Hiệp, Tân Chánh Hiệp
- **Phường Thới An**: Thạnh Xuân, Thới An
- **Phường Trung Mỹ Tây**: Tân Chánh Hiệp, Trung Mỹ Tây

#### Quận Bình Tân

- **Phường An Lạc**: An Lạc, Bình Trị Đông B, An Lạc A
- **Phường Bình Hưng Hòa**: Bình Hưng Hoà A, Bình Hưng Hòa
- **Phường Bình Tân**: Bình Hưng Hoà B, Tân Tạo, Bình Trị Đông A; Vĩnh Lộc B (Huyện Bình Chánh)
- **Phường Bình Trị Đông**: Bình Trị Đông, Bình Trị Đông A, Bình Hưng Hoà A
- **Phường Tân Tạo**: Tân Tạo A, Tân Tạo

#### Quận Bình Thạnh

- **Phường Bình Lợi Trung**: Phường 11, Phường 13, Phường 5
- **Phường Bình Quới**: Phường 28, Phường 27
- **Phường Bình Thạnh**: Phường 12, Phường 26, Phường 14
- **Phường Gia Định**: Phường 17, Phường 7, Phường 1, Phường 2
- **Phường Thạnh Mỹ Tây**: Phường 25, Phường 22, Phường 19

#### Quận Gò Vấp

- **Phường An Hội Đông**: Phường 16, Phường 15
- **Phường An Hội Tây**: Phường 12, Phường 14
- **Phường An Nhơn**: Phường 5, Phường 6
- **Phường Gò Vấp**: Phường 10, Phường 17
- **Phường Hạnh Thông**: Phường 3, Phường 1
- **Phường Thông Tây Hội**: Phường 11, Phường 8

#### Quận Phú Nhuận

- **Phường Cầu Kiệu**: Phường 7, Phường 1, Phường 2
- **Phường Đức Nhuận**: Phường 9, Phường 5, Phường 4
- **Phường Phú Nhuận**: Phường 11, Phường 13, Phường 10, Phường 8, Phường 15

#### Quận Tân Bình

- **Phường Bảy Hiền**: Phường 10, Phường 12, Phường 11
- **Phường Tân Bình**: Phường 13, Phường 14
- **Phường Tân Hòa**: Phường 9, Phường 6, Phường 8
- **Phường Tân Sơn**: Phường 15; Phường 10 (Quận Gò Vấp)
- **Phường Tân Sơn Hòa**: Phường 2, Phường 3, Phường 1
- **Phường Tân Sơn Nhất**: Phường 4, Phường 5, Phường 7

#### Quận Tân Phú

- **Phường Phú Thạnh**: Phú Thạnh, Hiệp Tân, Tân Thới Hòa
- **Phường Phú Thọ Hòa**: Phú Thọ Hòa, Tân Quý, Tân Thành
- **Phường Tân Phú**: Phú Trung, Hòa Thạnh, Tân Thới Hòa, Tân Thành
- **Phường Tân Sơn Nhì**: Tân Sơn Nhì, Sơn Kỳ, Tân Quý, Tân Thành
- **Phường Tây Thạnh**: Tây Thạnh, Sơn Kỳ

#### Thành phố Thủ Đức

- **Phường An Khánh**: Thảo Điền, An Khánh, An Phú
- **Phường Bình Trưng**: Bình Trưng Tây, Bình Trưng Đông, An Phú, Thảo Điền
- **Phường Cát Lái**: Thạnh Mỹ Lợi, Cát Lái
- **Phường Hiệp Bình**: Hiệp Bình Chánh, Hiệp Bình Phước, Linh Đông
- **Phường Linh Xuân**: Linh Xuân, Linh Trung, Linh Tây
- **Phường Long Bình**: Long Bình, Long Thạnh Mỹ; Bình Thắng (Thành phố Dĩ An, Bình Dương)
- **Phường Long Phước**: Trường Thạnh, Long Phước
- **Phường Long Trường**: Phú Hữu, Long Trường
- **Phường Phước Long**: Phước Long B, Phước Long A, Phước Bình
- **Phường Tam Bình**: Bình Chiểu, Tam Phú, Tam Bình
- **Phường Tăng Nhơn Phú**: Tăng Nhơn Phú A, Hiệp Phú, Tân Phú, Tăng Nhơn Phú B, Long Thạnh Mỹ
- **Phường Thủ Đức**: Trường Thọ, Linh Chiểu, Bình Thọ, Linh Đông

### Bà Rịa - Vũng Tàu cũ

#### Huyện Châu Đức

- **Xã Bình Giã**: Bình Trung, Bình Giã, Quảng Thành
- **Xã Châu Đức**: Xà Bang, Cù Bị
- **Xã Kim Long**: Kim Long, Bàu Chinh, Láng Lớn
- **Xã Ngãi Giao**: Suối Nghệ, Ngãi Giao, Bình Ba
- **Xã Nghĩa Thành**: Đá Bạc, Nghĩa Thành
- **Xã Xuân Sơn**: Sơn Bình, Suối Rao, Xuân Sơn

#### Huyện Long Đất

- **Xã Đất Đỏ**: Phước Long Thọ, Đất Đỏ, Long Tân, Láng Dài
- **Xã Long Điền**: Long Điền, Tam An
- **Xã Long Hải**: Long Hải, Phước Hưng, Phước Tỉnh
- **Xã Phước Hải**: Phước Hội, Phước Hải

#### Huyện Xuyên Mộc

- **Xã Bàu Lâm**: Bàu Lâm, Tân Lâm
- **Xã Bình Châu**: Bình Châu
- **Xã Hồ Tràm**: Phước Tân, Phước Thuận, Phước Bửu
- **Xã Hòa Hiệp**: Hòa Hiệp
- **Xã Hòa Hội**: Hòa Bình, Hòa Hội, Hòa Hưng
- **Xã Xuyên Mộc**: Xuyên Mộc, Bưng Riềng, Bông Trang

#### Thành phố Bà Rịa

- **Phường Bà Rịa**: Phước Nguyên, Long Toàn, Phước Hưng, Phước Trung
- **Phường Long Hương**: Tân Hưng, Kim Dinh, Long Hương
- **Phường Tam Long**: Hoà Long, Long Phước, Long Tâm

#### Thành phố Phú Mỹ

- **Phường Phú Mỹ**: Mỹ Xuân, Phú Mỹ
- **Phường Tân Hải**: Tân Hải, Tân Hoà
- **Phường Tân Phước**: Tân Phước, Phước Hoà
- **Phường Tân Thành**: Hắc Dịch, Sông Xoài
- **Xã Châu Pha**: Châu Pha, Tóc Tiên

#### Thành phố Vũng Tàu

- **Phường Phước Thắng**: Phường 12, Phường 11
- **Phường Rạch Dừa**: Thắng Nhất, Phường 10, Rạch Dừa
- **Phường Tam Thắng**: Phường 7, Phường 8, Nguyễn An Ninh, Phường 9
- **Phường Vũng Tàu**: Thắng Nhì, Phường 4, Phường 3, Phường 2, Thắng Tam, Phường 5, Phường 1
- **Xã Long Sơn**: Long Sơn

### Bình Dương cũ

#### Huyện Bắc Tân Uyên

- **Phường Bình Cơ**: Bình Mỹ; Hội Nghĩa (Thành phố Tân Uyên)
- **Xã Bắc Tân Uyên**: Tân Định, Tân Thành, Đất Cuốc
- **Xã Thường Tân**: Lạc An, Thường Tân, Tân Mỹ, Hiếu Liêm

#### Huyện Bàu Bàng

- **Phường Bến Cát**: Lai Hưng, Tân Hưng; Mỹ Phước (Thành phố Bến Cát)
- **Phường Long Nguyên**: Long Nguyên; An Điền, Mỹ Phước (Thành phố Bến Cát)
- **Xã Bàu Bàng**: Lai Uyên
- **Xã Trừ Văn Thố**: Trừ Văn Thố, Cây Trường II, Lai Uyên

#### Huyện Dầu Tiếng

- **Phường Tây Nam**: Thanh Tuyền, An Lập; An Tây (Thành phố Bến Cát)
- **Xã Dầu Tiếng**: Dầu Tiếng, Định An, Định Thành, Định Hiệp
- **Xã Long Hòa**: Long Hoà, Long Tân, Minh Thạnh, Minh Tân
- **Xã Minh Thạnh**: Minh Thạnh, Minh Hoà, Minh Tân
- **Xã Thanh An**: Thanh An, An Lập, Định Hiệp, Thanh Tuyền

#### Huyện Phú Giáo

- **Xã An Long**: Tân Long, An Linh, An Long
- **Xã Phú Giáo**: An Bình, Phước Vĩnh, Tam Lập
- **Xã Phước Hòa**: Phước Hoà, Vĩnh Hoà, Tam Lập
- **Xã Phước Thành**: Phước Sang, Tân Hiệp, An Thái

#### Thành phố Bến Cát

- **Phường Chánh Phú Hòa**: Chánh Phú Hòa; Hưng Hòa (Huyện Bàu Bàng)
- **Phường Hòa Lợi**: Tân Định, Hòa Lợi
- **Phường Phú An**: Phú An; Tân An, Hiệp An (Thành phố Thủ Dầu Một)
- **phường Thới Hòa**: Thới Hòa

#### Thành phố Dĩ An

- **Phường Dĩ An**: Dĩ An, Tân Đông Hiệp, An Bình
- **Phường Đông Hòa**: Đông Hòa, Bình An, Bình Thắng
- **Phường Tân Đông Hiệp**: Tân Bình, Tân Đông Hiệp; Thái Hòa (Thành phố Tân Uyên)

#### Thành phố Tân Uyên

- **Phường Tân Hiệp**: Tân Hiệp, Khánh Bình
- **Phường Tân Khánh**: Tân Phước Khánh, Tân Vĩnh Hiệp, Thái Hòa, Thạnh Phước, Thạnh Hội
- **Phường Tân Uyên**: Uyên Hưng, Bạch Đằng; Tân Mỹ, Tân Lập (Huyện Bắc Tân Uyên)
- **Phường Vĩnh Tân**: Vĩnh Tân; Tân Bình (Huyện Bắc Tân Uyên)

#### Thành phố Thủ Dầu Một

- **Phường Bình Dương**: Phú Mỹ, Hoà Phú, Phú Tân; Phú Chánh (Thành phố Tân Uyên)
- **Phường Chánh Hiệp**: Định Hoà, Chánh Mỹ, Hiệp An, Tương Bình Hiệp
- **Phường Phú Lợi**: Phú Hòa, Phú Lợi, Hiệp Thành
- **Phường Thủ Dầu Một**: Chánh Nghĩa, Phú Thọ, Phú Cường, Hiệp Thành, Chánh Mỹ

#### Thành phố Thuận An

- **Phường An Phú**: An Phú, Bình Chuẩn
- **Phường Bình Hòa**: Bình Hòa, Vĩnh Phú
- **Phường Lái Thiêu**: Lái Thiêu, Bình Nhâm, Vĩnh Phú
- **Phường Thuận An**: An Thạnh, An Sơn, Hưng Định
- **Phường Thuận Giao**: Thuận Giao, Bình Chuẩn

**Chưa có dữ liệu:** Đặc khu Côn Đảo.
