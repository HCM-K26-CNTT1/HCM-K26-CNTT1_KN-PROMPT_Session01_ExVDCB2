# BÀI TẬP: KHẮC PHỤC LỖI RÒ RỈ DỮ LIỆU MẬT KHI CHAT VỚI AI

## PHẦN 1. XÁC ĐỊNH THÔNG TIN NHẠY CẢM

Trong đoạn code ban đầu có 2 thông tin nhạy cảm:

| Tên biến | Giá trị bị lộ | Loại thông tin |
|---|---|---|
| `db_password` | `rikkei_secret_password_2026` | Mật khẩu cơ sở dữ liệu |
| `api_key` | `google_gemini_api_abc123` | Khóa API Gemini |

**Rủi ro:** Người khác có thể sử dụng các thông tin này để truy cập trái phép vào cơ sở dữ liệu hoặc dịch vụ API.

## PHẦN 2. LÀM SẠCH CODE VÀ VIẾT PROMPT AN TOÀN

### 2.1. Code sau khi làm sạch

Thay thế thông tin thật bằng Placeholder:

```python
def connect_database():
    db_password = '[YOUR_DATABASE_PASSWORD]'
    api_key = '[YOUR_API_KEY]'
    print('Đang kết nối...')
```

### 2.2. Prompt an toàn gửi cho AI

Bạn là chuyên gia lập trình Python. Hãy kiểm tra và tối ưu đoạn code sau.

Yêu cầu:
- Phân tích và đề xuất cách cải thiện code.
- Giữ nguyên các Placeholder, không yêu cầu mật khẩu hoặc API Key thật.
- Không tự tạo thông tin xác thực thay thế.
- Hướng dẫn sử dụng Environment Variables để lưu thông tin bí mật.
- Giải thích ngắn gọn, dễ hiểu.

Code cần kiểm tra:

```python
def connect_database():
    db_password = '[YOUR_DATABASE_PASSWORD]'
    api_key = '[YOUR_API_KEY]'
    print('Đang kết nối...')
```

## PHẦN 3. KẾT LUẬN

- Không chia sẻ mật khẩu và API Key thật lên AI công cộng.
- Thay thế thông tin nhạy cảm bằng Placeholder trước khi gửi code.
- Sử dụng biến môi trường để bảo vệ thông tin bí mật.
- Thêm `.env` vào `.gitignore` để tránh đưa dữ liệu mật lên GitHub.
- Nếu thông tin thật đã bị lộ, cần thu hồi hoặc thay mới ngay.

**Kết luận:** Làm sạch dữ liệu trước khi sử dụng AI là bước quan trọng giúp hạn chế nguy cơ rò rỉ thông tin và bảo vệ hệ thống.
