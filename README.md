# ☕ BrewCraft Roasters - Specialty Coffee & Sensory Data Platform

> **Đồ án Giao diện Web E-Commerce Cà Phê Đặc Sản Tích Hợp Dữ Liệu Cảm Quan & Cổng Thanh Toán Quét Mã QR Tự Động Điền Tiền (VietQR)**

---

## 🌟 1. Giới thiệu Dự án

**BrewCraft Roasters** là giao diện website thương mại điện tử hiện đại, ấm áp và chuyên nghiệp dành cho thương hiệu cà phê đặc sản (Specialty Coffee). 

Dự án giải quyết trăn trở lớn nhất của người tiêu dùng khi mua cà phê trực tuyến: *"Làm sao biết hương vị hạt này có hợp gu của mình không?"* thông qua tính năng độc quyền **Hồ Sơ Hương Vị & So Sánh Cảm Quan Đa Chiều (Sensory Comparison Radar Chart)**, đồng thời đáp ứng trọn vẹn yêu cầu thực tế của Giảng viên: **Tích hợp thanh toán quét mã QR tự động hiển thị số tiền thanh toán ngay lập tức**.

---

## 🎨 2. Hệ Thống Thiết Kế & Trải Nghiệm (Design System)

- **Bảng màu ấm áp & thủ công (Earthy Artisanal Palette):**
  - Nâu Espresso đậm (`#26150D`, `#180C07`) tượng trưng cho hạt cà phê rang mộc chất lượng cao.
  - Kem yến mạch dịu mắt (`#FAF7F2`, `#F3ECE1`) tạo cảm giác thư thái, thân thiện như trong một xưởng rang specialty.
  - Đất nung Terracotta (`#C85A32`) & Xanh Matcha tự nhiên (`#4A6B53`) làm điểm nhấn tương tác sinh động.
- **Typography:**
  - Tiêu đề nghệ thuật: `Playfair Display` (Serif cổ điển sang trọng).
  - Nội dung & Thông số: `Plus Jakarta Sans` (Sans-serif hiện đại, rõ nét).
- **Ngôn ngữ:** 100% Tiếng Việt chuẩn xác thuật ngữ chuyên ngành cà phê (Cupping Score SCA, Washed, Honey, Anaerobic...).

---

## 🚀 3. Các Tính Năng Nổi Bật & Cốt Lõi

### 3.1. Tính Năng So Sánh Cảm Quan Đa Chiều (Sensory Profile & Radar Chart)
- **Thanh nổi so sánh (Floating Compare Bar):** Tự động xuất hiện ở chân trang khi chọn sản phẩm, hiển thị số lượng hạt đã chọn (tối đa 4 loại) cùng thumbnail trực quan.
- **Biểu đồ Radar Nhện (Spider Chart) trực quan hóa 6 trục cảm quan:**
  1. *Độ chua sáng (Acidity)*
  2. *Thể chất / Độ đậm đà (Body)*
  3. *Độ ngọt tự nhiên (Sweetness)*
  4. *Độ đắng thanh (Bitterness)*
  5. *Hương thơm quyến rũ (Aroma)*
  6. *Hậu vị sâu lắng (Aftertaste)*
- **Bảng đối chiếu kỹ thuật song song (Side-by-side):** So sánh điểm SCA, Giống hạt (Varietal), Phương pháp sơ chế (Process), Độ cao canh tác (Altitude) và Dụng cụ pha chế khuyên dùng (V60, Chemex, Espresso...).

### 3.2. Tính Năng Thanh Toán Quét Mã QR Tự Động (VietQR NAPAS247)
*(Yêu cầu trọng tâm của Giảng viên: "Chỉ cần quét mã QR là hiện ra số tiền thanh toán luôn")*
- **Công nghệ VietQR Động:** Mã QR được mã hóa trực tiếp số tiền của đơn hàng (`amount`), số tài khoản ngân hàng MBBank, tên chủ tài khoản và mã đơn hàng duy nhất (`BCR-XXXXXX`).
- **Khách hàng quét bằng app ngân hàng bất kỳ (Vietcombank, MB, Techcombank, BIDV, MoMo, VNPay...):** Màn hình chuyển khoản trên điện thoại sẽ **tự động điền đúng 100% số tiền** và nội dung chuyển khoản, không cần người dùng nhập tay!
- **Đồng hồ đếm ngược hiệu lực mã:** 15:00 phút.
- **Nút Sao chép 1-chạm:** Cho phép copy nhanh Số tài khoản, Số tiền, Mã đơn hàng.
- **Chức năng Demo cho Giảng viên:** Tích hợp nút *"Mô phỏng Ngân Hàng Báo Có Tự Động"* để sinh viên biểu diễn luồng thanh toán thời gian thực cho cô giáo xem: sau 2.5 giây nhận tiền, hệ thống tự động bắn pháo hoa Confetti và xuất Hóa đơn điện tử tại chỗ!

### 3.3. Trải Nghiệm Mua Sắm & Giỏ Hàng (Cart Drawer)
- Ngăn kéo trượt mượt mà từ bên phải.
- Cho phép chọn kiểu xay tùy chỉnh: *Hạt nguyên (Whole Bean), Xay V60, Xay Espresso, Xay Cold Brew*.
- Tăng / giảm số lượng, xóa món, tính phí vận chuyển và miễn phí giao hàng tự động.
- Nút "Mua ngay" tại từng sản phẩm giúp đi thẳng vào luồng thanh toán siêu tốc.

### 3.4. Hệ Thống Đăng Nhập & Đăng Ký Tài Khoản (Authentication System)
- **Đăng ký tài khoản mới:**
  - Nhập Họ tên, Tên đăng nhập (Username), Email, Mật khẩu và Xác nhận mật khẩu.
  - Tự động kiểm tra trùng lặp tài khoản/email, kiểm tra độ dài mật khẩu và mật khẩu xác nhận.
  - Sau khi đăng ký thành công, hệ thống tự động lưu vào cơ sở dữ liệu trình duyệt (`localStorage`) và tự động chuyển về màn hình đăng nhập với tên tài khoản đã được điền sẵn.
- **Đăng nhập với cơ chế đối chiếu nghiêm ngặt:**
  - Người dùng phải nhập **chính xác tài khoản (hoặc email) và mật khẩu** đã đăng ký.
  - **Nếu nhập sai tài khoản hoặc mật khẩu:** Hệ thống lập tức hiển thị hộp thông báo lỗi màu đỏ rõ nét: *"Tài khoản hoặc mật khẩu không chính xác. Vui lòng kiểm tra lại!"*, viền đỏ ô mật khẩu và phát thông báo cảnh báo Toast.
  - **Nếu nhập đúng:** Cập nhật ngay giao diện Navbar (hiển thị Avatar viết tắt, Tên người dùng và Menu thả xuống cá nhân), thông báo chào mừng.
  - **Tài khoản thử nghiệm:** Không có tài khoản hoặc mật khẩu mặc định; đăng ký một tài khoản riêng để thử luồng đăng nhập.
  - **Đăng xuất (Logout):** Xóa phiên đăng nhập và trở về trạng thái chưa đăng nhập an toàn.

### 3.5. Bắt Buộc Đăng Nhập & Form Thông Tin Nhận Hàng (+84 & Autocomplete)
- **Chặn mua hàng khi chưa đăng nhập:**
  - Nếu chưa đăng nhập hoặc đăng ký tài khoản $\rightarrow$ Khi bấm *"Mua ngay"* hoặc *"Tiến hành đặt hàng"* trong giỏ hàng, hệ thống sẽ **chặn lại ngay lập tức**, hiển thị cảnh báo và tự động mở Modal Đăng Nhập / Đăng Ký.
  - Sau khi đăng nhập thành công, hệ thống tự động tiếp tục mở màn hình Nhập thông tin giao hàng mà không cần bấm lại.
- **Số điện thoại chuẩn Việt Nam (+84):**
  - Giao diện tích hợp sẵn tiền tố quốc gia `[🇻🇳 +84]` chuẩn di động Việt Nam.
  - Kiểm tra tính hợp lệ của số điện thoại: đúng định dạng các nhà mạng Việt Nam (`+84 3/5/7/8/9...` gồm 9 chữ số sau mã quốc gia).
  - **Nếu nhập sai:** Hệ thống báo lỗi màu đỏ tức thì và chặn thanh toán.
- **Địa chỉ giao hàng tự động gợi ý (Autocomplete Dropdown):**
  - **Tỉnh / Thành phố:** Khi người dùng gõ chữ, hệ thống tự động lọc và gợi ý tỉnh thành tương ứng ngay lập tức.
    - *Ví dụ:* Gõ chữ **"Q"** $\rightarrow$ Hiển thị ngay các tỉnh: **Quảng Trị, Quảng Ngãi, Quảng Bình, Quảng Nam, Quảng Ninh**.
  - **Quận / Huyện & Phường / Xã:** Tương tự, tự động gợi ý theo từng ký tự gõ.
  - **Thông tin hóa đơn:** Toàn bộ họ tên, SĐT (+84...) và địa chỉ giao hàng chi tiết được lưu trữ và xuất trực tiếp trên Hóa đơn điện tử sau khi quét mã QR thanh toán thành công.

---

## 💻 4. Cấu Trúc & Hướng Dẫn Chạy Dự Án

Project vẫn là frontend tĩnh, không chuyển thành Django/Python thật. Markup được tổ chức trong `templates/`, tài nguyên trong `static/`, còn `index.html` là entry loader.

### Cấu trúc chính

```text
index.html
templates/
├── home.html
└── components/                  # Dành cho partial giao diện khi cần tách tiếp
static/
├── css/main.css
└── js/
  ├── app.js                    # Entry point duy nhất
  ├── legacy-core.js            # Core tương thích, giữ nguyên nghiệp vụ hiện tại
  ├── tailwind.config.js
  ├── auth/auth.js
  ├── cart/cart.js
  ├── checkout/checkout.js
  ├── compare/compare.js
  ├── payment/payment.js
  ├── product/product.js
  └── ui/ui.js
backup/pre-refactor/              # Bản sao trước refactor
```

### Chạy bằng VS Code Live Server
1. Mở thư mục `d:/cong nghe phan mem 2/` trong VS Code.
2. Chuột phải vào `index.html` -> Chọn **"Open with Live Server"**.
3. Trang web sẽ chạy tại địa chỉ: `http://127.0.0.1:5500/index.html`.

Không mở trực tiếp bằng `file://`, vì entry point dùng `fetch()` để nạp `templates/home.html` và ES Modules cần HTTP server.

---

## 🎯 5. Kịch Bản Thuyết Trình Trước Giảng Viên (Gợi ý cho Sinh viên)

1. **Mở đầu (1 phút):**
   > *"Em chào Cô và các bạn. Nhóm em phát triển website thương mại điện tử BrewCraft Roasters dành cho cà phê đặc sản. Điểm khác biệt lớn nhất của dự án là không chỉ bán sản phẩm, mà còn số hóa dữ liệu cảm quan hương vị bằng biểu đồ Radar và tích hợp thanh toán quét mã QR tự động điền số tiền theo đúng yêu cầu của Cô."*

2. **Demo Tính năng So Sánh Cảm Quan (2 phút):**
   - Chọn thử 2 loại hạt: **Ethiopia Yirgacheffe G1** (hương hoa quả, rang sáng) và **Colombia Geisha** (lên men kỵ khí).
   - Chỉ vào thanh nổi góc dưới màn hình và nhấn **"So Sánh Chi Tiết Ngay"**.
   - Thuyết minh Biểu đồ Radar: *"Tại đây khách hàng nhìn thấy ngay hạt Colombia vượt trội về độ ngọt (9.8/10) và hương thơm (9.9/10), trong khi Ethiopia có độ chua sáng thanh khiết (9.2/10)."*

3. **Demo Tính năng Quét Mã QR Hiện Số Tiền (2 phút - Trọng tâm yêu cầu):**
   - Bấm thêm 1 sản phẩm vào giỏ hàng hoặc bấm **"Mua ngay"**.
   - Mở giỏ hàng, tổng tiền ví dụ là `395.000₫` + phí ship.
   - Bấm nút **"Thanh toán ngay bằng mã QR"**.
   - Thuyết minh mã QR: *"Thưa Cô, đây là mã VietQR động được tạo tự động với đúng số tiền của đơn hàng. Khi khách hàng mở app ngân hàng quét mã này thì số tiền sẽ tự động nhảy lên màn hình điện thoại mà không cần nhập tay."*
   - Nhấn nút **"Mô phỏng Ngân hàng Báo Có (Demo)"** để biểu diễn phản hồi nhận tiền -> Màn hình bắn pháo hoa chúc mừng và hiển thị Hóa đơn điện tử chuyên nghiệp.
