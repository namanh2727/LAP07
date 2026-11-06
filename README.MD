1. Tên dự án
Portfolio CV – Nguyễn Nam Anh

Website hồ sơ cá nhân dạng tĩnh (static website), dùng để giới thiệu bản thân và năng lực trong lĩnh vực phát triển giao diện web.
2. Mô tả và chức năng
Website được thiết kế theo hướng đơn giản, trực quan, hỗ trợ hiển thị trên nhiều kích thước màn hình. Nội dung được chia thành các khu vực chính:
- Trang đầu / Giới thiệu: Hiển thị lời chào, họ tên, vị trí Frontend Developer, mô tả ngắn và các nút điều hướng đến dự án hoặc phần liên hệ.
- Kỹ năng: Trình bày các kỹ năng và công nghệ gồm HTML5, CSS3, Flexbox, Grid, JavaScript ES6+, Responsive Design, Git, GitHub, Figma và Wireframe.
- Dự án tiêu biểu: Hiển thị các thẻ giới thiệu dự án:
  - Landing Page Sản Phẩm.
  - Ứng dụng Todo List.
  - Weather Dashboard.
  - Blog Cá Nhân.
- Liên hệ: Hiển thị email, Instagram và LinkedIn để nhà tuyển dụng hoặc người xem có thể liên hệ.
- Điều hướng trong trang: Các liên kết đưa người dùng đến những khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hỗ trợ truy cập cơ bản: Có liên kết “Bỏ qua điều hướng” và các nhãn mô tả ảnh (alt).
- Responsive: Giao diện hướng đến khả năng thích ứng với màn hình máy tính, máy tính bảng và điện thoại; cách hiển thị cụ thể phụ thuộc nội dung CSS trong styles.css.
Đây là website tĩnh. Trong HTML được cung cấp không thấy phần máy chủ backend, cơ sở dữ liệu, hệ thống đăng nhập hoặc quy trình build ứng dụng.
3. Công nghệ sử dụng
Công nghệ / công cụ	Vai trò
HTML5	Xây dựng cấu trúc và nội dung trang web
CSS3	Định dạng giao diện, bố cục và hiệu ứng
Flexbox	Sắp xếp các thành phần theo một chiều
CSS Grid	Xây dựng bố cục lưới, ví dụ khu vực dự án
JavaScript ES6+	Được liệt kê trong phần kỹ năng; HTML được cung cấp chưa thể hiện tệp JavaScript riêng
Git và GitHub	Quản lý phiên bản và lưu trữ mã nguồn (nếu sử dụng)
Figma / Wireframe	Công cụ thiết kế giao diện, phác thảo bố cục (nếu sử dụng)
Docker + Nginx	Phương án tùy chọn để chạy website tĩnh trong container


4. Yêu cầu môi trường
Cách chạy trực tiếp
- Windows 10/11, macOS hoặc Linux.
- Trình duyệt hiện đại: Google Chrome, Microsoft Edge, Firefox hoặc Safari.
- Không bắt buộc cài Node.js, npm hay cơ sở dữ liệu để mở trang HTML tĩnh.
- Trình soạn thảo mã nguồn khuyến nghị: Visual Studio Code.
Cách chạy bằng Docker (tùy chọn)
- Đã cài Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux).
- Có thể sử dụng Docker Compose nếu muốn quản lý cấu hình bằng Compose.
- Cần có kết nối Internet ở lần đầu tải image Nginx.
5. Cấu trúc thư mục
Cấu trúc tối thiểu dự kiến để các đường dẫn trong index.html hoạt động:
portfolio-cv/
├── index.html
├── README.md
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/
│       ├── 8458cf3632d40c5428b83a2d30b640bb.jpg
│       ├── 20-34-49-252_640.jpg
│       ├── images (1).jfif
│       ├── images (2).jfif
│       └── images.jfif
└── Dockerfile                 # Tạo nếu muốn chạy bằng Docker
Tên và số lượng ảnh trong thư mục assets/img/ cần khớp chính xác với các đường dẫn src trong HTML. Trên Linux, tên tệp có phân biệt chữ hoa/chữ thường.
6. Cài đặt và cấu hình
6.1. Lấy mã nguồn
Nếu dự án đã được đưa lên Git:
git clone <URL_REPOSITORY>
cd <TEN_THU_MUC_DU_AN>
Nếu chưa có repository, giải nén hoặc sao chép toàn bộ thư mục dự án vào máy tính. Đảm bảo index.html nằm ở thư mục gốc và thư mục assets nằm cùng cấp.
6.2. Kiểm tra đường dẫn tài nguyên
Trong phần <head>, trang đang liên kết CSS bằng đường dẫn:
<link rel="stylesheet" href="./assets/css/styles.css" />
Ảnh được tham chiếu từ thư mục assets/img/. Nếu đổi tên hoặc di chuyển tệp, cần cập nhật lại đường dẫn trong HTML.
6.3. Cập nhật thông tin cá nhân
Trước khi công khai website, hãy kiểm tra và chỉnh sửa:
- Họ tên hiển thị ở phần thương hiệu, tiêu đề trang và phần giới thiệu. Trong HTML được cung cấp, tên ở thương hiệu đang là “Trần Vũ Đại”, trong khi tiêu đề và phần giới thiệu ghi “Nguyễn Nam Anh”.
- Email liên hệ: namanh271205@gmail.com.
- Instagram: naman_h27 (liên kết hiện đang để #, cần thay bằng URL hồ sơ thật).
- LinkedIn: nội dung đang là linkedin.com/in/nguyenvanan nhưng liên kết href hiện để #; cần kiểm tra và thay bằng URL hồ sơ chính xác.
- Các nút “Xem chi tiết” của dự án hiện đang dùng href="#"; hãy thay bằng liên kết dự án thật hoặc trang chi tiết tương ứng.
Không đưa mật khẩu, khóa API hoặc thông tin bí mật vào mã nguồn công khai.
7. Chạy thử dự án
7.1. Windows 10/11
Cách 1 – Mở trực tiếp
1. Mở thư mục dự án bằng File Explorer.
2. Nhấp đúp vào index.html.
3. Trang sẽ mở bằng trình duyệt mặc định.
Cách 2 – Dùng Visual Studio Code
1. Mở Visual Studio Code.
2. Chọn File → Open Folder... và mở thư mục dự án.
3. Mở index.html.
4. Có thể dùng tiện ích Live Server (nếu đã cài): nhấp chuột phải vào index.html → Open with Live Server.
Cách 3 – Dùng Python làm máy chủ tĩnh

Mở PowerShell hoặc Command Prompt tại thư mục dự án:
py -m http.server 8000
Nếu lệnh py không hoạt động nhưng đã cài Python, thử:
python -m http.server 8000
Mở trình duyệt tại:
http://localhost:8000
Dừng máy chủ bằng Ctrl + C.
7.2. macOS
Cách 1 – Mở trực tiếp
1. Mở Finder và tìm đến thư mục dự án.
2. Nhấp đúp index.html hoặc nhấp chuột phải → Open With → chọn Safari/Chrome.
Cách 2 – Dùng Terminal

Mở Terminal, chuyển đến thư mục dự án:
cd /duong/dan/toi/portfolio-cv
python3 -m http.server 8000
Mở trình duyệt tại http://localhost:8000.

Dừng máy chủ bằng Control + C.
7.3. Linux
Mở Terminal và chuyển đến thư mục dự án:
cd /duong/dan/toi/portfolio-cv
python3 -m http.server 8000
Mở trình duyệt tại http://localhost:8000.

Nếu hệ thống chưa có Python 3, cài đặt Python 3 bằng trình quản lý gói của bản phân phối Linux đang sử dụng. Dừng máy chủ bằng Ctrl + C.
7.4. Chạy bằng Docker
Docker là phương án tùy chọn. Vì dự án là website tĩnh, có thể dùng Nginx để phục vụ các tệp HTML, CSS và hình ảnh.

Bước 1 – Tạo Dockerfile tại thư mục gốc
FROM nginx:alpine

# Xóa trang mặc định của Nginx
RUN rm -rf /usr/share/nginx/html/*

# Sao chép website vào thư mục phục vụ của Nginx
COPY . /usr/share/nginx/html

EXPOSE 80
Bước 2 – Tạo image

Chạy tại thư mục có Dockerfile:
docker build -t portfolio-cv .
Bước 3 – Khởi chạy container
docker run -d --name portfolio-cv-web -p 8080:80 portfolio-cv
Bước 4 – Truy cập website

Mở trình duyệt tại:
http://localhost:8080
Bước 5 – Kiểm tra và dừng container
docker ps
docker logs portfolio-cv-web
docker stop portfolio-cv-web
Khởi động lại:
docker start portfolio-cv-web
Xóa container khi không còn sử dụng:
docker rm -f portfolio-cv-web
Nếu cổng 8080 đã được ứng dụng khác sử dụng, đổi phần bên trái của tham số -p, ví dụ -p 8081:80, rồi truy cập http://localhost:8081.

Lưu ý: Không sao chép các thư mục không cần thiết (ví dụ .git) vào image nếu không muốn đưa chúng vào container. Có thể bổ sung .dockerignore:
.git
.gitignore
README.md
.DS_Store
8. Kiểm tra sau khi chạy
Sau khi mở website, nên kiểm tra các nội dung sau:
1. Trang chủ hiển thị đầy đủ tiêu đề, lời giới thiệu và ảnh đại diện.
2. CSS được tải thành công, không xuất hiện giao diện HTML thô.
3. Các ảnh trong phần dự án hiển thị đúng.
4. Các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ điều hướng đến đúng vị trí.
5. Các nút và liên kết liên hệ dẫn đến địa chỉ chính xác.
6. Giao diện không bị tràn hoặc vỡ bố cục trên màn hình điện thoại và máy tính.
7. Mở Developer Tools của trình duyệt (phím F12) và kiểm tra tab Console/Network nếu có lỗi tải tài nguyên.
9. Khắc phục sự cố thường gặp
Hiện tượng	Nguyên nhân có thể	Cách xử lý
Không thấy CSS	Sai đường dẫn hoặc thiếu styles.css	Kiểm tra assets/css/styles.css và đường dẫn trong HTML
Ảnh không hiển thị	Thiếu ảnh, sai tên hoặc sai chữ hoa/chữ thường	Đối chiếu tên ảnh trong assets/img/ với thuộc tính src
Không truy cập được localhost	Máy chủ chưa chạy hoặc cổng bị chiếm	Chạy lại lệnh máy chủ hoặc đổi sang cổng khác
Docker không build được	Thiếu Dockerfile hoặc chạy lệnh sai thư mục	Đặt Dockerfile ở thư mục gốc và chạy docker build tại đó
Container chạy nhưng trang lỗi	Nội dung chưa được sao chép đúng vào image	Kiểm tra cấu trúc thư mục và lệnh COPY trong Dockerfile
Liên kết dự án không hoạt động	Đường dẫn đang để #	Cập nhật URL dự án thực tế


10. Triển khai
Do đây là website tĩnh, có thể triển khai lên dịch vụ lưu trữ static hosting hoặc máy chủ web có hỗ trợ phục vụ HTML/CSS/ảnh. Khi triển khai:
- Đưa index.html và toàn bộ thư mục assets/ lên cùng cấu trúc.
- Kiểm tra lại đường dẫn tương đối và phân biệt chữ hoa/chữ thường.
- Cập nhật các liên kết liên hệ và dự án.
- Kiểm tra giao diện trên nhiều trình duyệt và thiết bị.
- Nếu dùng Docker, triển khai container Nginx theo cấu hình ở mục 7.4 và cấu hình HTTPS ở lớp máy chủ/proxy phù hợp.
11. Thông tin liên hệ
Thông tin được thể hiện trong mã nguồn HTML:
- Họ tên: Nguyễn Nam Anh
- Email: namanh271205@gmail.com
- Instagram: naman_h27 – cần cập nhật liên kết hồ sơ thật trong HTML.
- LinkedIn: linkedin.com/in/nguyenvanan – cần xác minh và cập nhật URL liên kết thật.
Website được xây dựng nhằm giới thiệu kỹ năng, dự án và mở rộng cơ hội thực tập, việc làm trong lĩnh vực Frontend Development.
12. Giấy phép
Chưa có thông tin giấy phép sử dụng trong mã nguồn được cung cấp. Nếu dự án được chia sẻ công khai, chủ sở hữu nên bổ sung tệp LICENSE và ghi rõ điều kiện sử dụng, sao chép hoặc chỉnh sửa.