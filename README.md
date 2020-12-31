# Dự đoán giá bất động sản khu vực thành phố Hồ Chí Minh

## 1. Câu hỏi đặt ra ?

Dự đoán giá bất động sản khu vực thành phố Hồ Chí Minh.

## 2. Ý nghĩa ?

- Lĩnh vực bất động sản luôn ảnh hưởng lớn đến nền kinh tế quốc gia. Thông qua kết quả nhận được từ bài toán dự đoán giá bất động sản nêu trên, người dùng có thể sử dụng để đáp ứng các nhu cầu như sau:
  - Sử dụng kết quả làm giá tham khảo khi có nhu cầu mua bất động sản với những tiêu chí được đề ra.
  - Người dùng có nhu cầu muốn mua nhà trong tương lai, muốn định lượng được giá bất động sản với những tiêu chí đề ra, ước tính chi phí phù hợp và kế hoạch chi tiêu cho bản thân.
  - Các công ty, dịch vụ bất động sản sử dụng làm mức giá sàn tham khảo và đề xuất được mức giá phù hợp đối với công ty và khách hàng.

## 3. Thu thập dữ liệu

- Dữ liệu được thu thập bằng cách parse HTML từ các website kinh doanh dịch vụ bất động sản online nổi tiếng trong nước.
- Dưới đây là danh sách các website được nhóm khảo sát dữ liệu để thực hiện việc thu thập dữ liệu phục vụ cho bài toán.
  - <https://batdongsan.com.vn/>
  - <https://homedy.com/>
  - <https://nha.chotot.com/tp-ho-chi-minh/mua-ban-bat-dong-san>
  - <https://meeyland.com/>
- Thông qua quá trình khảo sát, nghiên cứu và so sánh dữ liệu của các trang web. Nhóm lựa chọn trang web <https://batdongsan.com.vn/> do nhận thấy dữ liệu từ trang phù hợp của yêu cầu đặt ra của bài toán. Ngoài ra, website cũng cho phép người dùng có thể thu thập dữ liệu từ trang web.

## 4. Tổng quan dữ liệu thu thập

Sau khi thực hiện quá trình thu thập dữ liệu từ trang web batdongsan.com, nhóm lưu dữ liệu vào file bds.csv

Tổng quan về dữ liệu như sau:

- Số dòng: 5000
- Số cột: 6
  - Tiêu đề
  - Chú thích
  - Diện tích
  - Giá
  - Đặc điểm bất động sản
  - Thông tin dự án
- Cột cần dự đoán: Giá

## 5. Ý nghĩa dữ liệu

### Tổng quan

Dữ liệu thu thập được còn khá tổng hợp, chưa phân tách rõ. Chưa thể phân tích và áp dụng mô hình máy học.

### Trường dữ liệu Tiêu đề

**Ý nghĩa dữ liệu**: Nội dung tiêu đề bài đăng giới thiệu về bất động sản.

**Đặc điểm dữ liệu**: Dữ liệu dạng văn bản.

**Nhận xét**: Không có giá trị cho bài toán.

### Trường dữ liệu Chú thích

**Ý nghĩa dữ liệu**: Nội dung mô tả tên và địa điểm của bất động sản bao gồm tên đường, tên phường, tên quận, tên thành phố.

**Đặc điểm dữ liệu**: Dữ liệu văn bản. Gồm nhiều trường dữ liệu nhỏ có thể phân tách được như tên bất động sản, tên đường, tên phường, tên quận và tên thành phố toạ lạc của bất động sản. Thông tin quan trọng nhưng cần xử lý phân tách chuỗi ra các cột dữ liệu nhỏ.

**Ý dữ liệu**: Định danh được bất động sản và khu vực của bất động sản.

### Trường dữ liệu Giá

**Ý nghĩa dữ liệu**: Thể hiện giá của bất động sản và là thông tin cần được dự đoán của bài toán.

## 6. Đánh giá

- Kết quả bài toán cho thấy các mức giá bất động sản tại khu vực thành phố Hồ Chí Minh, dự đoán được khoảng giá bất động sản với cái tham số đầu vào như trong bài làm.
- Về tổng quan, độ chính xác của bài làm vẫn còn khá thấp do nhiều yếu tố:
  - Dữ liệu thu thập vẫn còn ít (17000 dòng sau khi đã xử lý).
  - Giá trị của các trường dữ liệu dùng để dự đoán vẫn còn bị nhiễu khá nhiều do độ chính xác của nguồn để thu thập dữ liệu không thật sự được kiểm chúng chính xác hoàn toàn.
  - Quá trình xử lý dữ liệu còn hạn chế.
  - Mô hình áp dụng để dự đoán chưa được tối ưu.
- Tuy nhiên, thông qua kết quả và quá trình thực hiện đồ án này, bản thân các thành viên trong nhóm đã học và củng cố một số kỹ năng hỗ trợ giải quyết các bài toán về khoa học dữ liệu và hy vọng có thể ứng dụng được trong tương lai.

## 7. Phân công công việc

|  STT  |                      Công việc                       |        Thành viên thực hiện        |
| :---: | :--------------------------------------------------: | :--------------------------------: |
|  01   |                   Lựa chọn câu hỏi                   | Nguyễn Huỳnh Thảo Nhi, Lê Bá Quyền |
|  02   |        Lựa chọn phương thức thu thập dữ liệu         | Nguyễn Huỳnh Thảo Nhi, Lê Bá Quyền |
|  03   |           Lựa chọn nguồn thu thập dữ liệu            | Nguyễn Huỳnh Thảo Nhi, Lê Bá Quyền |
|  04   | So sánh, đánh giá dữ liệu thu thập được từ các nguồn |            Lê Bá Quyền             |
|  05   |                   Thu thập dữ liệu                   |            Lê Bá Quyền             |
|  06   |                  Tiền xử lý dữ liệu                  |       Nguyễn Huỳnh Thảo Nhi        |
|  07   |                   Đánh giá dữ liệu                   |            Lê Bá Quyền             |
|  08   |          Lựa chọn, áp dụng mô hình máy học           | Nguyễn Huỳnh Thảo Nhi, Lê Bá Quyền |
|  09   |                  Visualize dữ liệu                   |            Lê Bá Quyền             |
|  10   |               Tổng hợp, viết document                |       Nguyễn Huỳnh Thảo Nhi        |

## 8. Hướng dẫn chạy các file notebook

**Môi trường:** Jupyter Notebook

**Ngôn ngữ:** Python version 2.7.0

**Phần mềm cài đặt:** Anaconda-Navigator

**Hướng dẫn quy trình cài đặt:**

1. Cài đặt Python. Tham khảo tại trang web <https://www.python.org/>
2. Cài đặt Anaconda. Tham khảo tại trang web <https://www.anaconda.com/products/individual>
3. Launch Jupyter Notebook bằng Anaconda.
4. Mở file ipynb bằng Jupyter notebook.
5. Run file ipynb: Kernel -> Restart & Run All
