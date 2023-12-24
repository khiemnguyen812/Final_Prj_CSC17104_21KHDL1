# PROGRAMMING FOR DATA SCIENCE - FIT - HCMUS

## Final Project - Thu thập, phân tích và trả lời câu hỏi về bộ dữ liệu Sleep Health và Lifestyle

### I. Thông tin nhóm:

- Lớp: 21KHDL1

| MSSV     | Họ tên           |
| -------- | ---------------- |
| 21127587 | Nguyễn Trọng Đại |
| 21127726 | Nguyễn Tấn Khiêm |

### II. Thông tin đề tài:

#### **_01. Dataset:_**

- [Sleep Health and Lifestyle Dataset](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset) gồm 400 hàng và 13 cột, chứa nhiều biến số liên quan đến giấc ngủ và lối sống. Nó bao gồm các chi tiết như giới tính, tuổi tác, nghề nghiệp, thời gian ngủ, chất lượng giấc ngủ, mức độ hoạt động thể chất, mức độ căng thẳng, chỉ số BMI, huyết áp, nhịp tim, số bước đi hàng ngày và sự hiện diện hay vắng mặt của rối loạn giấc ngủ. Bộ dataset này sẽ cho bạn cái nhìn tổng quan về sự ảnh hưởng của lối sống và sức khoẻ đối với chứng rối loạn giấc ngủ.

- Tác giả: [Laksika Tharmalingam](https://www.kaggle.com/uom190346a)
- License: CC0: Public Domain

#### **_02. Các câu hỏi có ý nghĩa:_**

- **Câu hỏi 1**: Lối sống lý tưởng để không bị rối loạn giấc ngủ là gì?

    - **Thành viên phụ trách**: Nguyễn Trọng Đại
    
    - **Mục đích**: Đưa ra mẫu hình lý tưởng về lối sống để từ đó mỗi người có thể tự điều chỉnh bản thân, giúp bản thân có một giấc ngủ ngon, không mắc chứng rối loạn khi đang ngủ.

    - **Ý tưởng thực hiện**: Phân tích các đặc trưng liên quan đến lối sống, tìm ra giá trị phù hợp ở mỗi đặc trưng (giá trị có tần suất rối loạn giấc ngủ là ít nhất), kết hợp các giá trị để đưa ra mẫu hình lý tưởng. Gộp nhóm các giá trị theo giới tính vì sinh học của nam và nữ là khác nhau, cần có hình mẫu riêng.

- **Câu hỏi 2**: Liệu nam giới hay nữ giới bị rối loạn giấc ngủ nhiều hơn và tại sao?

    - **Thành viên phụ trách**: Nguyễn Trọng Đại

    - **Mục đích**: Giúp chúng ta có cái nhìn tổng quát về sự ảnh hưởng của giới tính đối với chứng rối loạn giấc ngủ cũng như tác nhân gây ra nó.

    - **Ý tưởng thực hiện**: Phân tích tỷ lệ bị rối loạn giấc ngủ giữa nam và nữ, sau đó phân tích sự ảnh hưởng (mối quan hệ) của các đặc trưng khác theo từng giới tính.

- **Câu hỏi 3**: Liệu có mối liên quan nào giữa mức độ hoạt động vận động hàng ngày và chất lượng giấc ngủ?

  - **Thành viên phụ trách**: Nguyễn Tấn Khiêm
  
  - **Mục đích**: Điều tra xem liệu việc tăng cường hoạt động vận động có thể ảnh hưởng đến chất lượng giấc ngủ hay không, từ đó có thể đề xuất giải pháp cải thiện giấc ngủ thông qua việc thay đổi mức độ hoạt động hàng ngày.
  
  - **Ý tưởng thực hiện**: Kết hợp dữ liệu về Quality of Sleep với thông tin về Physical Activity Level và Daily Steps để xác định mức độ ảnh hưởng của chất lượng giấc ngủ đối với hiệu suất công việc và sức khỏe tổng thể.

- **Câu hỏi 4**: Làm thế nào chất lượng giấc ngủ ảnh hưởng đến sức khỏe của người tham gia khảo sát?
  
  - **Thành viên phụ trách**: Nguyễn Tấn Khiêm
  
  - **Mục đích**: Tìm hiểu về mối quan hệ giữa chất lượng giấc ngủ ảnh hưởng đến sức khỏe tổng thể, nhằm đưa ra những khuyến nghị về quản lý giấc ngủ trong môi trường làm việc.
  
  - **Ý tưởng thực hiện**: Kết hợp dữ liệu về Quality of Sleep với thông tin về Stress Level, BMI Category, Systolic, Diastolic, Heart Rate và Sleep Disorder để xác định mức độ ảnh hưởng của chất lượng giấc ngủ đối với hiệu suất công việc và sức khỏe tổng thể.

#### **_03. Phân tích các câu hỏi:_**

- **Câu hỏi 1**: Lối sống lý tưởng để không bị rối loạn giấc ngủ là gì?

    - Các bước phân tích dữ liệu:

        - Bước 1: Tính số lần xuất hiện cho từng giá trị của mỗi cột, gộp nhóm theo giới tính.
![Q1-B1](./Images/q1_b1.png)

        - Bước 2: Trực quan hoá bước 1.
![Q1-B2](./Images/q1_b2.png)

        - Bước 3: Chọn các giá trị tốt nhất (số lần xuất hiện nhiều nhất) của từng cột, đưa ra mẫu hình lối sống lý tưởng cho từng giới tính.
![Q1-B3](./Images/q1_b3.png)

- **Câu hỏi 2**: Liệu nam giới hay nữ giới bị rối loạn giấc ngủ nhiều hơn và tại sao?

    - Các bước phân tích dữ liệu:

        - Bước 1: Tính số lượng bị và không bị rối loạn giấc ngủ, đưa ra tỷ lệ phần trăm cho từng giới tính.
![Q2-B1](./Images/q2_b1.png)

        - Bước 2: Kiểm tra khoảng trung bình giữa nam và nữ trong các cột Numeric: `Sleep Duration`, `Quality of Sleep`, `Physical Activity Level`, `Stress Level`, `Heart Rate` và `Daily Steps`.
![Q2-B2](./Images/q2_b2.png)

        - Bước 3: Dùng phân phối tích luỹ thực nghiệm để tính xác suất bị rối loạn giấc ngủ tăng dần theo độ tuổi.
![Q2-B3](./Images/q2_b3.png)

        - Bước 4: Xác định tỷ lệ cân nặng giữa nam và nữ.
![Q2-B4](./Images/q2_b4.png)

    - Bước 1 để trả lời phần `Liệu nam giới hay nữ giới bị rối loạn giấc ngủ nhiều hơn` và các bước còn lại là dựa vào biểu đồ để tìm ra nguyên nhân.

- **Câu hỏi 3**: Liệu có mối liên quan nào giữa mức độ hoạt động vận động hàng ngày và chất lượng giấc ngủ?

  - Các bước phân tích dữ liệu:

    - Bước 1: Xác định các phân vị của các cột. <br>
![C3_B1](./Images/Cau3_B1.png)

    - Bước 2: Các giá trị của từng cột sẽ được chia theo phân vị, các giá trị nằm trong khoảng Minimum đến Quartile 1 sẽ là 1(ít/kém), nằm trong khoảng hơn Quartile 1 và Quartile 2 sẽ là 2(trung bình), từ hơn Quartile 2 đến Quartile 3 là 3(khá) và từ hơn Quartile 3 Maximum sẽ là 4(tốt). <br>
![C3_B1](./Images/Cau3_B2.png)

    - Bước 3: Đếm xem sự xuất hiện của các giá trị 1,2,3,4 của 'Physical Activity Level' và 'Daily Steps' như thế nào theo nhóm 1,2,3,4 của 'Quality of Sleep'.<br>
![C3_B2](./Images/Cau3_B3.png)

    - Bước 4: Sử dụng biểu đồ scatter để trực quan hóa.<br>
![C3_B4](./Images/Cau3_B4.png)

- **Câu hỏi 4**: Làm thế nào chất lượng giấc ngủ ảnh hưởng đến sức khỏe của người tham gia khảo sát?
  
  - Các bước phân tích dữ liệu:
    
    - Bước 1: Ta sẽ tiếp tục chia cột 'Quality of Sleep' theo phân vị như Câu hỏi 3. Sau đó xem những người gặp tình trạng 'Sleep Apnea' hoặc 'Insomnia' có phần trăm thế nào theo 'Quality of Sleep'. <br>
![C4_B1](./Images/Cau4_B1.png)
    
    - Bước 2: Xác định phần trăm tình trạng 'High'và 'Normal' của 'Blood Pressure Status' theo từng 'Quality of Sleep'.<br>
![C4_B2](./Images/Cau4_B2.png)
    
    - Bước 3: Tương tự với cột 'BMI Category'.<br>
![C4_B3](./Images/Cau4_B3.png)
    
    - Bước 4: Xem những người có tình trạng 'Sleep Apnea', 'High' ở 'Blood Pressure Status' và bị thừa hoặc thiếu cân sẽ có chất lượng giấc ngủ như thế nào và xem những người không có tình trạng 'Sleep Apnea', 'Normal' ở 'Blood Pressure Status' và 'BMI Category' sẽ có chất lượng giấc ngủ như thế nào.<br>
![C4_B4](./Images/Cau4_B4.png)

#### **_04. Kế hoạch thực hiện:_**

![Schedule](./Images/schedule.png)
