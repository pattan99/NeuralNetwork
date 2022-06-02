# Cách sử dụng
## Thêm layer cho Model
![Model1](https://i.ibb.co/5T3Lr0N/image-2022-06-02-202917116.png)
<br>
Trong phần NeuralNetwork() là các layer. Layer đầu tiên phải là Input_Layer.
<br>
Input_Layer cần có dữ liệu học X, nhãn Y và độ lớn của mỗi dữ liệu output_size.
<br>
Các layer tiếp theo là Dense_Layer và Activation_Layer (hiện chỉ hỗ trợ 2 hàm activation là relu và softmax).
<br>
NeuralNetwork hiện chỉ hỗ trợ hàm mất mát cross entropy.
## Train Model
![Model2](https://i.ibb.co/nBwBq1s/image-2022-06-02-202804271.png)
<br>
Trước khi train phải compile bằng cách khai báo lr, loss và seed.
<br>
Sau đó gọi model.fit để train model, phải đặt giá trị cho epoch, còn batch_size = None sẽ train trên toàn bộ data trong 1 iteration.
