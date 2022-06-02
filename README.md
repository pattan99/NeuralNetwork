# Cách sử dụng
## Thêm layer cho Model
![Model1](https://i.ibb.co/HGw1gxG/image-2022-06-02-203233124.png)
<br>
Trong phần NeuralNetwork() là các layer. Layer đầu tiên phải là Input_Layer.
<br>
Input_Layer cần có dữ liệu học X, nhãn Y và độ lớn của mỗi dữ liệu output_size.
<br>
Các layer tiếp theo là Dense_Layer và Activation_Layer (hiện chỉ hỗ trợ 2 hàm activation là relu và softmax).
<br>
NeuralNetwork hiện chỉ hỗ trợ hàm mất mát cross entropy.
## Train Model
![Model2](https://i.ibb.co/0fxX5yv/image-2022-06-02-203417983.png)
<br>
Trước khi train phải compile bằng cách khai báo lr, loss và seed.
<br>
Sau đó gọi model.fit để train model, phải đặt giá trị cho epoch, còn batch_size = None sẽ train trên toàn bộ data trong 1 iteration.
## Test model
model.predict để predict ra nhãn dựa trên bộ test truyền vào.
<br>
model.evaluate để đánh giá model dựa trên nhãn dự đoán và nhãn thực.
### Qua nhiều lần thử nghiệm với số nút của hidden layer và batch_size khác nhau, ta có được kiến trúc mạng như trên sẽ có độ chính xác cao nhất: 0.9817.
# Ưu và nhược điểm của neural network
## Ưu điểm
- Có thể điều chỉnh các tham số hoặc tăng số hidden layer để tăng độ chính xác của mô hình.
- Dễ dàng giải quyết các bài toán phi tuyến tính như nhận diện ảnh, xử lý âm thanh, ngôn ngữ tự nhiên, ..., mà các mô hình tuyến tính khó mà làm được.
## Nhược điểm
- Phụ thuộc lớn vào data, để tăng độ chính xác của mô hình ta sẽ cần thêm nhiều data. Đây chính là một trong những điểm yếu lớn nhất của neural network.
- Khó mà giải thích được kết quả của mô hình.
