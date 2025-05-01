Here is the Vietnamese translation of your document:

---

# 0G Storage Auto Bot

Bot tự động tương tác với Mạng Lưu Trữ 0G trên Galileo Testnet để tối đa hóa khả năng nhận airdrop.

## Tổng Quan

Công cụ này tự động hóa quá trình tải lên các tệp ngẫu nhiên lên Mạng Lưu Trữ 0G trên Galileo Testnet. Nó giúp người dùng tham gia vào các hoạt động của testnet, từ đó có thể dẫn đến cơ hội nhận airdrop trong tương lai.

## Tính Năng

- **Hỗ Trợ Nhiều Ví**: Thực hiện tác vụ tuần tự trên nhiều khóa riêng
- **Tích Hợp Proxy**: Sử dụng proxy xoay vòng để tránh bị giới hạn tốc độ
- **Luân Phiên User-Agent**: Tự động thay đổi user agent cho mỗi yêu cầu
- **Thống Kê Chi Tiết**: Theo dõi các thao tác thành công và thất bại
- **Lịch Sử Giao Dịch**: Lưu lại tất cả chi tiết giao dịch để tham khảo sau này

## Cài Đặt

```bash
# Clone kho lưu trữ
git clone https://github.com/bronkdrop/0G-Storage-Auto-Bot.git

# Di chuyển vào thư mục
cd 0G-Storage-Auto-Bot

# Cài đặt các gói phụ thuộc
npm install
```

## Cấu Hình

1. Tạo một tệp `.env` ở thư mục gốc chứa các khóa riêng của bạn:

```
# Với một ví duy nhất
PRIVATE_KEY=your_private_key_here

# HOẶC với nhiều ví
PRIVATE_KEY_1=your_first_private_key
PRIVATE_KEY_2=your_second_private_key
PRIVATE_KEY_3=your_third_private_key
```

2. (Tùy chọn) Tạo tệp `proxies.txt` với mỗi proxy một dòng:

```
http://username:password@ip:port
http://ip:port
socks5://username:password@ip:port
```

## Sử Dụng

Chạy bot bằng lệnh:

```bash
node index.js
```

Khi được yêu cầu, nhập số lượng tệp bạn muốn tải lên cho mỗi ví.

## Cách Hoạt Động

1. Bot sẽ tải các khóa riêng và proxy của bạn
2. Với mỗi ví:
   - Bot sẽ tải hình ảnh ngẫu nhiên
   - Tính toán hash và chuẩn bị dữ liệu
   - Tải từng phần tệp lên indexer của 0G
   - Gửi giao dịch blockchain để đăng ký tệp đã tải lên
   - Chờ xác nhận rồi mới tiếp tục với lần tải tiếp theo
3. Kết quả sẽ được lưu trong thư mục `results`

## Khắc Phục Sự Cố

- **Lỗi Gas**: Đảm bảo ví của bạn có đủ token testnet 0G
- **Sự Cố Mạng**: Kiểm tra kết nối internet hoặc thử dùng proxy
- **Lỗi RPC**: RPC của testnet có thể đang quá tải, hãy thử lại sau

## Tuyên Bố Miễn Trừ Trách Nhiệm

Công cụ này chỉ dành cho mục đích giáo dục và tham gia testnet. Việc sử dụng bot không đảm bảo bạn sẽ được nhận airdrop trong tương lai. Luôn sử dụng các công cụ testnet một cách có trách nhiệm.

## Giấy Phép

MIT

