BEHIND THE NEWS — BẢN 2.0 (AI FACT-CHECKING)

Website đã được nâng cấp để người dùng nhập link bài viết công khai. Backend sẽ:
1) Truy cập và trích xuất nội dung bài viết.
2) Dùng AI xác định các khẳng định có thể kiểm chứng.
3) Tìm kiếm nguồn đối chiếu trên Internet qua Tavily.
4) Dùng AI tổng hợp bằng chứng, mức độ chắc chắn, lời khuyên và liên kết nguồn.

YÊU CẦU
- Node.js 20 trở lên
- OpenAI API key: https://platform.openai.com/api-keys
- Tavily API key: https://app.tavily.com/home

CHẠY THỬ TRÊN MÁY TÍNH
1. Cài Node.js 20+.
2. Mở Terminal/Command Prompt tại thư mục này.
3. Chạy: npm install
4. Sao chép .env.example thành .env.
5. Điền OPENAI_API_KEY và TAVILY_API_KEY vào .env (không chia sẻ file .env).
6. Chạy: npm start
7. Mở http://localhost:3000

ĐƯA LÊN INTERNET
- Đây không còn là website tĩnh chỉ có index.html. Cần nền tảng chạy Node.js (ví dụ Render Web Service hoặc Railway), không thể chỉ kéo-thả thư mục lên Netlify Drop như bản cũ.
- Đẩy toàn bộ thư mục này lên một GitHub repository riêng tư hoặc công khai.
- Tạo Web Service trên Render, kết nối repository, Build Command: npm install, Start Command: npm start.
- Trong Environment Variables của dịch vụ, thêm OPENAI_API_KEY, OPENAI_MODEL (gpt-4.1-mini) và TAVILY_API_KEY.
- Deploy. Dịch vụ sẽ phục vụ cả website và API trên cùng một domain.

BẢO MẬT
- Tuyệt đối không đặt API key trong index.html hoặc bất kỳ mã JavaScript chạy trên trình duyệt.
- Không tải file .env lên GitHub. File .env.example chỉ là mẫu.
- API có thể phát sinh chi phí theo mức sử dụng và chính sách của OpenAI/Tavily. Kiểm tra hạn mức, đặt giới hạn chi tiêu và theo dõi usage.
- Backend có kiểm tra URL công khai và chặn một số địa chỉ mạng nội bộ, nhưng trước khi mở rộng cho công chúng cần bổ sung rate limit, giới hạn lưu lượng và giám sát lạm dụng.

GIỚI HẠN KIỂM CHỨNG
- Một số trang chặn bot, yêu cầu đăng nhập, nội dung động, PDF, mạng xã hội hoặc paywall có thể không đọc được.
- Tìm kiếm web không đảm bảo tìm thấy mọi nguồn liên quan. AI có thể hiểu sai hoặc kết luận sai.
- Kết quả phải được xem là gợi ý nghiên cứu; người dùng cần mở và đọc nguồn gốc, đặc biệt với thông tin y tế, pháp luật, tài chính hoặc khẩn cấp.
- “Có cơ sở ủng hộ” không đồng nghĩa đã chứng minh tuyệt đối là thật; “chưa đủ căn cứ” không có nghĩa là giả.
