**Bài 5 : Xây dựng cơ chế xác thực an toàn cho Crypto Wallet**

### 1\. Sơ đồ luồng dữ liệu

Mật khẩu \-\> Điện thoại \-\> Sinh trắc học

Bước 1: Nhập Tên đăng nhập \+ Mật khẩu 

Bước 2: Mở app Authenticator trên điện thoại 

Bước 3: Bắt buộc quét Vân tay hoặc FaceID để hiển thị mã 

Bước 4: Nhập mã TOTP 6 số vào app Crypto \-\> Đăng nhập thành công

Cách 3 lớp này phối hợp chặn hacker:

* Nếu hacker lừa lấy được Mật khẩu, chúng sẽ bị chặn vì không cầm chiếc điện thoại cài app authenticator của bạn .  
* Kể cả khi hacker trộm được điện thoại, chúng vẫn không thể mở app authenticator để xem mã 6 số vì thiếu faceid hoặc vân tay của bạn.

### 2\. Xử lý bẫy

### Giải pháp: Người dùng vẫn mở app authenticator và lấy mã bình thường mà không gặp trở ngại nào.

Lý do: Thuật toán TOTP được thiết kế để hoạt động hoàn toàn offline. Nó tạo ra mã 6 số dựa trên sự kết hợp của 2 yếu tố:

1. chìa khóa bí mật  
2. Thời gian hiện tại trên đồng hồ của điện thoại.

Vì điện thoại tự tính toán mã này tại chỗ dựa vào đồng hồ rẽ nhịp mỗi  giây, nó không cần gửi hay nhận bất kỳ dữ liệu nào qua internet hay sóng viễn thông. Chỉ cần đồng hồ điện thoại chạy đúng giờ, mã sẽ luôn hợp lệ.

