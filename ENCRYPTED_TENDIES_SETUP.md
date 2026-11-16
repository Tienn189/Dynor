# Gói Tendies mã hóa cho Dynor

Công cụ web riêng: [Dynor Vault](https://dynor-vault.amberstingray1.chatgpt.site).

Hướng dẫn đầy đủ: [Thiết lập backend và ứng dụng](https://dynor-vault.amberstingray1.chatgpt.site/setup.html). Cần triển khai Supabase trước khi tạo/cài gói, rồi build IPA mới từ `Dynor-iOS-source.zip`. Hai Function mới chưa được triển khai trong project hiện tại.

- Web mã hóa `.tendies` thành `.dynor` bằng AES-256-GCM và đăng ký khóa qua API dành cho admin.
- App chỉ lưu bản mã, xin khóa được bọc cho thiết bị khi cài; không cache khóa nội dung hoặc xuất gói Tendies đã giải mã.
- Source và tài liệu backend nằm trong ZIP. `source-changes.diff` giúp xem các thay đổi văn bản so với source gốc; file nhị phân chỉ có trong ZIP.
- 21 kiểm thử Node đạt; 26 tệp Swift phân tích cú pháp đạt. Chưa build Xcode, chạy XCTest hoặc thử trên iPhone.

Với IPA do mỗi người tự ký, không thể bảo đảm độc quyền app tuyệt đối hoặc chống trích xuất sau giải mã. Hệ thống kiểm soát cấp khóa theo tài khoản/VIP và bọc khóa cho thiết bị nhận.
