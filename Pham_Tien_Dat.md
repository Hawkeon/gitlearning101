### 1. IP (Internet Protocol )
* IP là mã định danh các thiết bị trong mạng máy tính
### 2. SSH (Secure Shell)
* **SSH** là giao thức **truy cập và điều khiển máy tính/sever từ xa một cách an toàn** qua mạng.
*  Một số lệnh cơ bản :
	* Kết nối remote  
		 ``` ssh username@serverhost ```
		-   `username`: Tên user trên server
		-   `serverhost`: Có thể là **IP** hoặc **DNS/hostname**  
### 3. SCP (Secure Copy Protocol)
* **SCP** là giao thức dùng để chuyển file một cách **an toàn** giữa các máy tính thông qua kết nối SSH
* Câu lệnh scp cơ bản :
	*  ``` 
		scp [options][[user@]host1:]source_file_or_directory ... [[user@]host2:]destination
		```
		- **options** : ví dụ như `-r`  để chuyển thư mục và toàn bộ nội dung bên trong ,` -q ` để bỏ đi thanh tiến độ,...
		- **`[user@]host1:]source_file_or_directory`**: nguồn của file cần sao chép ,có thể chọn nhiều file cùng lúc
		- **`[[user@]host2:]destination`**: đích đến của file sao chép
* Ví dụ :
	*  ``` 	
		scp -q file1.txt file2.txt file3.txt user@serverhost:/rmt/d/test/  
		```
### 4.  TCP
 * **TCP** Là giao thức Cung cấp **kết nối 2 chiều** giữa client và server
 * TCP hoạt động theo mô hình "connection-oriented", nghĩa là trước khi truyền dữ liệu, các bên phải thiết lập kết nối thông qua quy trình **bắt tay ba bước (three-way handshake)**:
  ``` 
  1. Client → Server: SYN
2. Server → Client: SYN-ACK
3. Client → Server: ACK
  ```
  * TCP sử dụng các cơ chế **kiểm soát luồng** và **kiểm soát tắc nghẽn** để đảm bảo dữ liệu đến đích một cách ổn định, đồng thời có cơ chế phát hiện lỗi và yêu cầu truyền lại các đoạn bị mất hoặc lỗi
	 
### 5.SMTP (**Simple Mail Transfer Protocol**)
* Đây là giao thức chuẩn dùng để **gửi email** giữa các máy chủ (server) và từ client đến server.
*Ví dụ về cách hoạt động của SMTP :
![this is a image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2017/02/SMTP_1.png)
* Một số câu lệnh cơ bản :
	* Mở kết nối Telnet đến máy chủ SMTP :
		 ```telnet smtp.gmail.com 25 ```
	* Giới thiệu với máy chủ bằng lệnh HELO/EHLO:
		``` HELO client.example.com(có thể là ip/DNS)```
	* Xác định địa chỉ người gửi với MAIL FROM:
		 ``` MAIL FROM:<aRandomGuy@gmail.com>  ```
	* Xác định địa chỉ người nhận với RCPT TO :
	``` RCPT TO:<recipient@gmail.com> ```
	* Gửi nội dung email với DATA : 
	``` DATA ```
	* Bắt đầu nhập nội dung :
	``` ... ```
	*Kết thúc bằng lệnh QUIT :
	``` QUIT ```
### 6.SFTP(Secure File Transfer Protocol)
* Là giao thức **truyền file an toàn** chạy trên nền **SSH (Secure Shell)**.
* Cú pháp kết nối SFTP :
 ``` sftp user@severhost ```
*Sau khi kết nối với sever có thể sử dụng một số lệnh sau :
```markdown
| Lệnh          | Mô tả                                 |
|---------------|---------------------------------------|
| ls            | Liệt kê file/folder trên sever        |
| lls           | Liệt kê file/folder trên local        |
| cd            | Di chuyển thư mục làm việc trên sever |
| lcd           | Chuyển thư mục làm việc trên local    |
| get file.name | Tải file từ sever về local            |
| put file.name | Upload file từ local lên sever        |
| exit          | Thoát khỏi SFTP                       |
```
### 7.HTTP/HTTPS(HyperText Transfer Protocol /HyperText Transfer Protocol Secure )
* HTTP là giao thức giúp trao đổi thông tin giữa máy chủ web và trình duyệt, thông tin gửi đi bằng HTTP là plain text nên có thể bị  bên thứ 3 chặn lại và lấy thông tin trong __request__ và __response__ 
* HTTPS là phiên bản bảo mật hơn của HTTP ,thông tin được gửi đi sẽ được mã hóa bằng thuật toán khiến việc chặn lại và lấy thông tin khó khăn hơn bởi vì dữ liệu đã được mã hóa
### 8.UDP (User Datagram Protocol)
* UDP là giao thức **không kết nối (connectionless)**, nghĩa là không cần thiết lập kết nối trước khi truyền dữ liệu nên tốc độ của UDP sẽ nhanh hơn phù hợp với những yêu cầu truyền tải dữ liệu nhanh chóng
### 9.DNS
* là hệ thống phân giải tên miền trên Internet, giúp chuyển đổi các tên miền dễ nhớ (ví dụ: [www.youtube.com](http://www.youtube.com)) thành địa chỉ IP mà máy tính có thể hiểu 
### 10.FTP(File Transfer Protocol ) 
*Là một giao thức mạng được sử dụng để **truyền tải file** giữa máy khách (client) và máy chủ (server)
*Câu lệnh kết nối :
`ftp serverhost `
*Sau khi kết nối với sever thì có thể sử dụng các lệnh như cd,ls,.. để xem thông tin trên sever và !ls ,!cd ,... cho máy local



----------------------------------------------------------------------------------------------------------------------------------------------
Bản phân phối em chọn để dùng linux là ubuntu.Vì ubuntu có giao diện thân thiện với người dùng ,có cộng đồng lớn, tính ổn định và phù hợp để cài đặt và quản lý hệ thống



i edit the testing text

