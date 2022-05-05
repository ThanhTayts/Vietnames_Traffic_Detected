# Vietnames_Traffic_Detected
## Tổng Quan : Các phương tiện tự hành đang dần trở nên phổ biến trên toàn thế giới, hiện nay các công ty lớn như Tesla, Uber, Google, Mercedes-Benz, Toyota, Ford, Audi, và ở Việt Nam là VinFast đang nghiên cứu về các công nghệ hỗ trợ cho xe tự hành chẳng hạn như, đo khoảng cách tránh vật cản, nhận điện được các loại biển báo giao thông cũng như đèn tín hiệu để điều khiển. Việc ứng dụng công nghệ vào nhân dạng và phân loại biển báo và tín hiệu giao thông có thể giúp các phương tiện tự hành trở nên tiến tiến và hiện đại hơn, hoạt động chính xác hơn và tránh được các tai nạn va chạm xảy ra.
### I.Tổng quan hệ thống :
  - Phần cứng của hệ thống bao gồm : Máy tính xử lý và Camera, Camera sẽ được kết nối với máy tính và truyền dữ liệu video về để máy tính phân tích và xử lý
  - Về thu thập dữ liệu và xử lý dữ liệu: Ta sẽ sử dụng phần mềm Pycharm để tiến hành thu thập hình ảnh từ mạng Internet,  hoặc trính xuất các khung hình từ những video có sẵn chứa các đối tượng mà ta mong muốn, sau đó ta sẽ tiến hành đặt tên theo thứ cho từng hình ảnh trong tập dữ liệu để thuận tiện cho việc chia tập mẫu trong quá trình huấn luyện
  - Về gán nhãn dữ liệu : Ta sẽ sử dụng công cụ Labelimg được viết bằng ngôn ngữ Python để khoanh vùng và gán nhãn tương ứng các đối tượng từ những hình ảnh ta đã thu thập được
  - Về cấu hình và huấn luyện mô hình: Ta sử dụng Google Colab để cấu hình các thông số của mô hình mạng Yolo V4 và tiến hành huấn luyện và đưa ra dự đoán
  - Về dự đoán kết quả : Ta sẽ sử dụng phần mềm Pycharm kết hợp cùng với Nvidia và Tensorflow để có thể sử dụng GPU trong quá trình dự đoán qua hình ảnh, video có sẵn và luồng video trực tuyến từ webcam
  - ![image](https://user-images.githubusercontent.com/92384494/166888764-08c024c9-5f4d-4d89-a9a1-183d8bf411bf.png)
### II.Quá trình thu thập và xử lý dữ liệu
 - Tham khảo video : https://www.youtube.com/watch?v=sKDysNtnhJ4&t=34s
 - Code : https://github.com/haroonshakeel/simple_image_download
 - ![image](https://user-images.githubusercontent.com/92384494/166889195-7e19ee8d-5d8c-417b-811d-3bd6d2021ed6.png)

### III.Quá trình gán nhãn dữ liệu 
 - Tham khảo video : https://www.youtube.com/watch?v=sKDysNtnhJ4&t=34s
 - ![image](https://user-images.githubusercontent.com/92384494/166889758-501d020d-833e-4bf3-bd4a-46bc8a4ac04c.png)
 - Code : https://github.com/tzutalin/labelImg
 - ![image](https://user-images.githubusercontent.com/92384494/166889783-f50565b5-f5ba-4779-af45-94a7c69c52e4.png)
 - Tập dữ liệu đã được gán nhãn : https://drive.google.com/drive/folders/1POPUjSwON_yRD_Db9YZa6BMBHOpinCDz?usp=sharing
### VI. Quá trình huấn luyện
  - Tham khảo các bước tải và cấu hình darknet trên Colab 
    + link bài viết : https://www.miai.vn/2020/05/25/yolo-series-train-yolo-v4-train-tren-colab-chi-tiet-va-day-du-a-z/
    + ![image](https://user-images.githubusercontent.com/92384494/166890381-58a11a5d-ce38-4e47-9017-af206052aa3f.png)
    + link video : https://www.youtube.com/watch?v=-NEB5P-SLi0&t=372s
    + ![image](https://user-images.githubusercontent.com/92384494/166890398-1466519d-8c5c-4b43-8d55-2ebe3d43389a.png)
    + link Colab : https://colab.research.google.com/drive/1kMTmDntUGu6AfKRN_mRO9aTzfVv46nD_?usp=sharing
  - Quá trình huấn luyện kết thúc ta sẽ thu được file trong số của mô hình dưới dạng file .weight
### V. Dự đoán
  - Để sử dụng được GPU trong quá trình dự đoán ta cần cài đặt Cuda Toolkit và Cudnn
      + Link cài đặt : https://www.youtube.com/watch?v=PlW9zAg4cx8&t=168s
  - Conver file trong số mô hình YoLo V4 (.weight) sau khi đã training sang Tensorflow
      + Link video : https://www.youtube.com/watch?v=iPwepy-SVCQ&t=524s
      + Link code : https://github.com/theAIGuysCode/tensorflow-yolov4-tflite
  - Kết quả dự đoán trên hình ảnh
  
    ![image](https://user-images.githubusercontent.com/92384494/166890679-f6a8770c-5ce2-4987-8cd8-1312ccc18517.png)
    ![image](https://user-images.githubusercontent.com/92384494/166890698-57227624-5174-47c3-93b1-f6c1d9aa295a.png)
    ![image](https://user-images.githubusercontent.com/92384494/166890762-36b4e8b0-46a8-47e7-b5d3-206a3325fe9a.png)
    ![image](https://user-images.githubusercontent.com/92384494/166890784-9da00278-4f9f-4489-b545-c2b9172f00bc.png)
  - Kết quả dự đoán trên video
 
    ![image](https://user-images.githubusercontent.com/92384494/166890867-f91d3318-eab1-4bcc-a013-21e68c8008fd.png)
    ![image](https://user-images.githubusercontent.com/92384494/166890887-33f7fca0-58a2-4002-88b3-f631ae8bc2fd.png)


