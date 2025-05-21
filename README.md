# OOP_N01_Term3_2025_K17_Group12
Group 12 Member:
1.Nguyễn Nhật Minh
2.Phạm Văn Minh
3. Phạm Ngọc Tiến
#  ỨNG DỤNG QUẢN LÝ SÁCH 

##  Mô tả đề tài
Ứng dụng quản lý sách được xây dựng bằng Java Spring Boot nhằm phục vụ việc quản lý thư viện sách tại các phòng đọc hoặc trung tâm thông tin. Ứng dụng có giao diện đơn giản, dễ sử dụng, hỗ trợ đầy đủ các chức năng cơ bản như thêm/sửa/xoá sách và phòng, cũng như gán sách vào từng phòng. Dữ liệu được lưu dưới dạng **file nhị phân**.


##  Yêu cầu và chức năng chính

###  Công nghệ sử dụng
- Java 11+
- Spring Boot
- Maven
- Thymeleaf (hoặc REST API nếu dùng giao diện frontend)
- HTML/CSS (nếu có UI web)
- Ghi/đọc file nhị phân bằng `ObjectOutputStream`, `ObjectInputStream`


###  Các đối tượng chính
####  Book (Đối tượng 01 – Sách)
- Mã sách
- Tên sách
- Tác giả
- Thể loại
- Năm xuất bản
- Số lượng

####  Room (Đối tượng 02 – Phòng sách)
- Mã phòng
- Tên phòng
- Vị trí

####  BookRoom (Đối tượng 03 – Gán sách vào phòng)
- Gán một sách vào một hoặc nhiều phòng
- Một phòng có thể chứa nhiều sách


###  Các chức năng chính

####  Quản lý sách
- Thêm sách
- Sửa thông tin sách
- Xoá sách
- Liệt kê danh sách sách
- Lọc sách theo tên, tác giả, năm xuất bản, thể loại

####  Quản lý phòng sách
- Thêm phòng
- Sửa thông tin phòng
- Xoá phòng

####  Gán sách vào phòng
- Chức năng gán sách cho phòng
- Hiển thị danh sách sách theo từng phòng


###  Lưu trữ dữ liệu
- Dữ liệu được lưu bằng **file nhị phân**
  - `books.dat`, `rooms.dat`, `bookrooms.dat`
- Khi đọc dữ liệu từ file, sử dụng:
  - `ArrayList`, `HashMap`, `LinkedList`,... để lưu trữ dữ liệu trong RAM


##  Cấu trúc thư mục đề xuất

```plaintext
book-management/
├── src/
│   └── main/
│       ├── java/com/example/bookmanagement/
│       │   ├── model/             # Các lớp Book, Room, BookRoom
│       │   ├── manager/           # Các lớp quản lý: BookManager,...
│       │   ├── util/              # DataUtils.java
│       │   ├── controller/        # Controller của Spring Boot
│       │   └── BookManagementApplication.java
│       └── resources/
│           ├── templates/         # Thymeleaf template (nếu có)
│           └── application.properties
├── books.dat
├── rooms.dat
└── bookrooms.dat
