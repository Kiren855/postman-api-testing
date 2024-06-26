# postman-api-testing

# API Student được phát triển để quản lý thông tin về sinh viên. Nó cung cấp các phương thức để lấy danh sách sinh viên, tạo mới sinh viên, cập nhật thông tin sinh viên, và xoá sinh viên khỏi hệ thống. Địa chỉ của API là https://6639dadf1ae792804bed06b5.mockapi.io/api/v1/student.
## 1. kiểm thử phương thức get lấy danh sách student từ API
### Mục đích:
Đảm bảo rằng API trả về danh sách sinh viên
### Kịch bản kiểm thử:
Sử dụng phương thức GET để lấy danh sách sinh viên từ API
### Kết quả: 
API trả về danh sách sinh viên như mong đợi.
![](https://github.com/Kiren855/postman-api-testing/blob/main/Screenshot%202024-05-07%20151109.png)

## 2. kiểm thử phương thức post tạo mới 1 student
### Mục đích: 
Kiểm tra tính năng tạo mới student của API.
### Kịch bản kiểm thử: 
Gửi một yêu cầu POST với dữ liệu mới để tạo một student mới 
### Kết quả: 
trả về thông tin student vừa được thêm mới
![](https://github.com/Kiren855/postman-api-testing/blob/main/Screenshot%202024-05-07%20151734.png)

## 3. kiểm thử phương thức get lấy thông tin 1 student
### Mục đích: 
Đảm bảo rằng API có thể trả về thông tin chi tiết của một student dựa trên ID.
### Kịch bản kiểm thử: 
Sử dụng phương thức GET với một ID cụ thể để lấy thông tin của student đó.
### Kết quả: 
trả về thông tin student dựa trên id
![](https://github.com/Kiren855/postman-api-testing/blob/main/Screenshot%202024-05-07%20152150.png)

## 4. kiểm thử phương thức put để update thông tin student
### Mục đích: 
Kiểm tra tính năng cập nhật thông tin student của API.
### Kịch bản kiểm thử: 
Gửi một yêu cầu PUT với dữ liệu cập nhật để thay đổi thông tin của một student.
### Kết quả: 
trả về thông tin student mới sau khi được update
![](https://github.com/Kiren855/postman-api-testing/blob/main/Screenshot%202024-05-07%20152718.png)

## 5. kiểm thử phương thức delete để xoá student
### Mục đích: 
Kiểm tra tính năng xoá sinh viên của API.
### Kịch bản kiểm thử: 
Gửi một yêu cầu DELETE để xoá một student khỏi hệ thống.
### Kết quả: 
trả về thông tin student vừa được xoá khỏi hệ thống
![](https://github.com/Kiren855/postman-api-testing/blob/main/Screenshot%202024-05-07%20152947.png)

## 6. Kiểm thử tự động các phương thức của API student
### Mục đích: 
Kiểm tra toàn bộ tính năng có sẵn của API Student và đánh giá hiệu suất của nó dưới điều kiện tải cao.
### Kịch bản kiểm thử: 
Chạy tự động lặp lại gửi các yêu cầu đến API Student, bao gồm các phương thức GET, POST, PUT, và DELETE với các dữ liệu khác nhau.
### Kết quả kiểm thử: 
API Student chạy tốt với lượng request không cao, nhưng khi request nhiều, API bắt đầu trả về lỗi 429 Too Many Requests, cho thấy API không thể xử lý số lượng request lớn trong một khoảng thời gian ngắn.

- Với 100 request trong 1 phút: API hoạt động một cách ổn định và trả về kết quả chính xác cho mỗi yêu cầu.
- Với 1000 request trong 1 phút: API vẫn hoạt động nhưng bắt đầu trả về lỗi 429 Too Many Requests, cho thấy API không thể xử lý số lượng request lớn trong một khoảng thời gian ngắn.

![](https://github.com/Kiren855/postman-api-testing/blob/main/Screenshot%202024-05-13%20085800.png)

