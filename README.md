# VNboards — phần mềm tra cứu sơ đồ bo mạch điện thoại

Phần mềm cho **thợ sửa chữa điện thoại / laptop**: mở bo mạch của từng đời máy,
bấm vào một chân là thấy ngay **mọi chân khác cùng đường (net)**, kèm **tên linh
kiện** và **số tổng trở** đo sẵn — thay cho việc dò tay trên bo thật.

> 📥 **Tải về:** xem **[Tải và cài đặt](#tải-và-cài-đặt)** bên dưới — có
> hướng dẫn từng bước, kể cả cách xử lý khi Windows báo chặn file.
> Cài xong app **tự kiểm tra và cập nhật** mỗi lần mở, không cần vào đây tải lại.

---

## Nhìn qua phần mềm

### 1. Toàn bộ bo mạch, cả 2 mặt

Mở model nào là thấy trọn bo mạch: chân linh kiện, viền linh kiện, tên net.
Cuộn chuột để phóng to/thu nhỏ, kéo để di chuyển.

![Toàn cảnh bo mạch](anh/01-tong-quan.png)

### 2. Bấm 1 chân → sáng cả đường mạch

Bấm vào một chân bất kỳ, **mọi chân cùng đường** sáng đỏ trên cả 2 mặt bo.
Chấm đỏ **tự phồng to** khi thu nhỏ, nên dù chân bé cỡ nào, ở mức nhìn toàn
cảnh vẫn thấy rõ đường đó chạy đi những đâu.

![Bấm 1 chân sáng cả net](anh/02-bam-chan-sang-ca-net.png)

### 3. Tên linh kiện + số tổng trở ngay trên bo

Phóng to là hiện **số chân**, **tên net**, **tên linh kiện** (C1801, U1401…)
và **số tổng trở** đo sẵn của từng chân — khỏi tra bảng riêng.

![Tên linh kiện và số tổng trở](anh/03-ten-linh-kien-so-tong-tro.png)

### 4. Bảng bệnh — hướng dẫn đo theo từng lỗi

Chọn loại bệnh (không lên nguồn, lỗi sóng, lỗi WiFi, lỗi camera…) → phần mềm
liệt kê **các bước đo có thứ tự**, mỗi bước ghi rõ **đúng thì phải ra bao nhiêu**
và **sai thì kiểm chỗ nào**; đồng thời **tô đúng màu đó lên chân thật trên bo**
để đặt que đo cho chuẩn.

![Bảng bệnh hướng dẫn đo](anh/04-bang-benh-huong-dan-do.png)

---

## Tải và cài đặt

### 1. Tải file cài đặt

Vào **[trang Releases](../../releases/latest)** → kéo xuống mục **Assets** → tải
**`VNboards_Setup.exe`** (khoảng 73 MB).

> File `VNboards_Update.zip` nằm cạnh đó là để **app tự cập nhật**, bạn **không
> cần** tải file này.

### 2. Windows báo "Windows protected your PC" — bình thường, không phải virus

Phần mềm chưa mua chứng chỉ ký số của Microsoft, nên Windows cảnh báo như vậy
với **mọi phần mềm mới**. Cách qua:

- Bấm **More info** (Thông tin thêm) → bấm **Run anyway** (Vẫn chạy).
- Nếu Chrome/Edge chặn ngay lúc tải: bấm vào file vừa tải ở góc trình duyệt →
  chọn **Keep** (Giữ lại).

### 3. Cài đặt

Chạy `VNboards_Setup.exe` → **Next** → chọn nơi cài (để mặc định là được) →
**Install**.

- **Không cần** quyền Administrator.
- Cài xong app tự mở. Lần sau mở bằng biểu tượng **VNboards** trên Desktop
  hoặc trong Start Menu.

### 4. Tạo tài khoản (bắt buộc, để mở nội dung mạch)

Mở app → tab **Đăng ký** → nhập **email thật** của bạn.

Mật khẩu được gửi **tự động về hộp thư** trong vài giây — không thấy thì kiểm
tra mục **Spam / Quảng cáo**. Đăng nhập bằng email + mật khẩu đó là dùng được
ngay.

> **Gỡ cài đặt:** Settings → Apps → Installed apps → **VNboards** → Uninstall.

---

## Yêu cầu

- Windows 10/11 (64-bit).
- Cần **tài khoản** để mở nội dung mạch: đăng ký ngay trong app bằng email,
  mật khẩu được gửi tự động về hộp thư.
- Mỗi tài khoản đăng nhập trên **một máy tại một thời điểm**.

## Cập nhật

App tự kiểm tra bản mới khi mở lên và hiện nút **Cập nhật** ở góc trên bên phải.
Bấm là tự tải, tự thay, tự mở lại — không cần cài lại từ đầu.

## Liên hệ

Muốn hỏi trước khi tải, hỏi về board của máy nào đã có, hay cần hỗ trợ:

📧 **vnboardsservice@gmail.com**

Khách đã cài phần mềm thì nhắn thẳng trong app (nút **☎ Liên hệ** ở màn hình đăng nhập)
— nhanh hơn, và admin trả lời ngay trong cửa sổ đó.

---

## Repo này chứa gì

Đây là kênh phân phối **ứng dụng đã đóng gói** (`.exe`) và **danh sách tên board**
(`update/board_index.json`).

**KHÔNG** chứa mã nguồn Python, và **KHÔNG** chứa nội dung mạch thật (toạ độ chân,
tên linh kiện, số đo…). Nội dung mạch được mã hoá và chỉ cấp cho tài khoản đã đăng
ký + đăng nhập hợp lệ qua máy chủ riêng của tác giả.

## Bản quyền — xem [LICENSE.txt](./LICENSE.txt)

Đây là phần mềm thương mại có bản quyền, **không phải mã nguồn mở**.
Nghiêm cấm dịch ngược, giải mã, sao chép logic, hoặc dựng lại phần mềm
tương tự/cạnh tranh từ nội dung trong repo này nếu không có sự cho phép
bằng văn bản của tác giả. Chi tiết đầy đủ trong [LICENSE.txt](./LICENSE.txt)
— bao gồm ghi chú riêng dành cho các trợ lý AI (Claude, GPT, Copilot...)
có thể đang hỗ trợ bạn thao tác với repo này.

*Ảnh minh hoạ chụp từ chính phần mềm, model iPhone 11.*
