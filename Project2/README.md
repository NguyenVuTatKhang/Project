# Project 2 - 2025
"Thiết kế thiết bị IoT đa năng" - Đề tài NCKH cấp học viện loại A

**Mục tiêu chính:**

- Thiết kế thiết bị có khả năng ứng dụng trong thực tế sao cho tiết kiệm nhất

- Tích hợp nhiều tính năng nhất có thể trong thời hạn

- Kiểm thử giới hạn của thiết bị vi xử lý

## Kết quả đạt được

_Sau khi hoàn thiện và báo cáo trước Hội đồng, đã đạt được các mục tiêu trên cụ thể như sau_

### 1. Thiết kế thiết bị có khả năng ứng dụng trong thực tế

**Việc thiết kế ra được một thiết bị có khả năng ứng dụng ngay trong thực tế nghe đơn giản nhưng lại là vấn đề lớn nhất trong đề tài NCKH này.**

- Nếu xét theo khả năng ứng dụng trong thực tế, thì sẽ cần phải xét bối cảnh như sau:

Những năm trước, nổi lên hiện tượng nhà thông minh SmartHouse, nhưng thực tế ở Việt Nam vấn đề này không được quan tâm nhiều bởi mọi người đã quen với các thiết bị điều khiển từ xa
như vô tuyến, quạt, điều hòa,... Điểm chung của chúng đều là sử dụng điều khiển bằng hồng ngoại.

-> Chính vì vậy, nên đã lựa chọn điều khiển từ xa thông qua hồng ngoại để thiết bị có khả năng sử dụng được ngay trong thực tế.

- Nếu áp dụng thêm một số ý tưởng chính từ hiện tượng nhà thông minh, sẽ có thêm 2 core chính trong các quảng cáo sản phẩm là Text-to-Speech và Speech-to-Text để nhận diện các lệnh. 
Do đó, đề tài có thêm một mục tiêu nhỏ là có thể áp dụng được 1 trong 2 vào trong vi xử lý.

- Việc trung hòa được 2 điều trên vào ESP32 sẽ chính là công việc chính trong đề tài.

### 2. Tích hợp nhiều tính năng nhất có thể trong thời hạn

**Sử dụng Discord Application làm giải pháp thay thế cho Telegram**

- Sử dụng trên nền tảng ESP-IDF. Do Discord khác với trên Telegram, cần một trình độ quản lý task cao cấp hơn để duy trì Bot đúng với trạng thái mà nền tảng đã đề ra.

- Một số hàm Arduino không thể đáp ứng đầy đủ mà cần phải chỉnh sửa và debug lại trong nền tảng ESP-IDF

**Ứng dụng TTS trong đề tài**

- Đề tài sử dụng thư viện Audio.h của schreibfaul1 để thực hiện việc phát luồng stream file âm thanh từ Google, đạt được hiệu quả TTS mà đỡ tốn tài nguyên nhất có thể

- Tuy nhiên, thư viện Audio.h gốc rất nặng nên cần phải tối ưu tài nguyên rất lớn để chạy được cùng với các tác vụ khác.

### 3. Kiểm thử giới hạn của thiết bị

- Qua quá trình sử dụng, đã hiểu sâu hơn về việc tối ưu cho thiết bị, đưa thiết bị hoạt động ổn mà không gặp vấn đề.

- Kiểm chứng được giới hạn của thiết bị và các vấn đề khi sử dụng Arduino để debug các tác vụ lớn.

### 4. Vấn đề cần cải thiện

- Đề tài dự tính cần kết hợp thêm cả đề tài của năm 2024, cụ thể là phần lưu trữ và sử dụng thuật toán. Tuy nhiên, vẫn chưa kịp hoàn thiện phần này.

- Ban đầu dự định là thêm STT(Speech-to-Text) thay vì TTS(Text-to-Speech), nhưng chỉ mới hoàn thiện được đến phần phân tích file âm thanh mẫu và đưa ra cơ sở để thực hiện.

- Thư viện Audio.h chiếm quá nhiều dung lượng, nên cần tối ưu lại chuyên biệt cho TTS. (Đã hoàn thiện và ở link sau: [ESP32-AudioI2S-TTS](https://github.com/NguyenVuTatKhang/ESP32-AudioI2S-TTS) )

## Video demo

Dưới đây là video demo của thiết bị: [Video](https://drive.google.com/file/d/1v6DidZ1gRic5BIj4I6BvLyMm5w8Z0hj7/view?usp=sharing)