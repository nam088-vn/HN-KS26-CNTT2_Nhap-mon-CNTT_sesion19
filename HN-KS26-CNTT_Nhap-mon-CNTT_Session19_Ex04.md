**Bài 4 : Rủi ro đánh cắp mật khẩu từ trình duyệt**

1\. Bảng so sánh

| Tiêu chí | Google Chrome | Bitwarden |
| :---- | :---- | :---- |
| Chống mã độc Infostealer | Kém vì mã độc dễ dàng trích xuất từ file login data | Tốt vì dữ liệu bị mã hóa, tính năng tự động khóa vault |
| Zero-Knowledge Architecture | Không | Có vì chỉ có người dùng giữ chìa khóa giải mã |
| Đồng bộ chéo nền tảng | Hạn chế vì phụ thuộc vào hệ sinh thái google | Toàn diện vì mọi hệ điều hành, mọi trình duyệt |

2\.

Mã độc Infostealer trộm mật khẩu bằng cách copy file dữ liệu lưu trên máy tính.

* Chrome dùng chính phiên đăng nhập máy tính để bảo vệ file. Khi máy bị nhiễm mã độc đang chạy nên nó tự động mở khóa và đọc được toàn bộ mật khẩu ngay lập tức.  
    
* Bitwarden khóa dữ liệu bằng master password và mật khẩu này không bao giờ được lưu trên máy. Nếu máy bị nhiễm mã độc mà ăn cắp được file của Bitwarden, nó chỉ nhận được một mớ ký tự rác. Thao tác bạn phải tự tay nhập master password chính là cách chặn để giải mã dữ liệu cục bộ, khiến mã độc không làm được gì dù đã xâm nhập thành công vào máy tính.

