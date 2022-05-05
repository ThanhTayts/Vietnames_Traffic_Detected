# Vietnames_Traffic_Detected
## Tổng Quan : Các phương tiện tự hành đang dần trở nên phổ biến trên toàn thế giới, hiện nay các công ty lớn như Tesla, Uber, Google, Mercedes-Benz, Toyota, Ford, Audi, và ở Việt Nam là VinFast đang nghiên cứu về các công nghệ hỗ trợ cho xe tự hành chẳng hạn như, đo khoảng cách tránh vật cản, nhận điện được các loại biển báo giao thông cũng như đèn tín hiệu để điều khiển. Việc ứng dụng công nghệ vào nhân dạng và phân loại biển báo và tín hiệu giao thông có thể giúp các phương tiện tự hành trở nên tiến tiến và hiện đại hơn, hoạt động chính xác hơn và tránh được các tai nạn va chạm xảy ra.
### I.Tổng quan hệ thống :
  - Phần cứng của hệ thống bao gồm : Máy tính xử lý và Camera, Camera sẽ được kết nối với máy tính và truyền dữ liệu video về để máy tính phân tích và xử lý
  - Về thu thập dữ liệu và xử lý dữ liệu: Ta sẽ sử dụng phần mềm Pycharm để tiến hành thu thập hình ảnh từ mạng Internet,  hoặc trính xuất các khung hình từ những video có sẵn chứa các đối tượng mà ta mong muốn, sau đó ta sẽ tiến hành đặt tên theo thứ cho từng hình ảnh trong tập dữ liệu để thuận tiện cho việc chia tập mẫu trong quá trình huấn luyện
  - Về gán nhãn dữ liệu : Ta sẽ sử dụng công cụ Labelimg được viết bằng ngôn ngữ Python để khoanh vùng và gán nhãn tương ứng các đối tượng từ những hình ảnh ta đã thu thập được
  - Về cấu hình và huấn luyện mô hình: Ta sử dụng Google Colab để cấu hình các thông số của mô hình mạng Yolo V4 và tiến hành huấn luyện và đưa ra dự đoán
  - Về dự đoán kết quả : Ta sẽ sử dụng phần mềm Pycharm kết hợp cùng với Nvidia và Tensorflow để có thể sử dụng GPU trong quá trình dự đoán qua hình ảnh, video có sẵn và luồng video trực tuyến từ webcam
  - ![image](https://user-images.githubusercontent.com/92384494/166888764-08c024c9-5f4d-4d89-a9a1-183d8bf411bf.png)


