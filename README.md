# <p align="center">🚘 BIỂN SỐ ĐẸP — BIENSOVIP.VN 🚘</p>
### <p align="center">Sàn Giao Dịch & Định Giá Biển Số Xe Đẹp Trực Tuyến Hàng Đầu Việt Nam</p>
<p align="center">
  <strong>Thương hiệu Duy Đinh — Biển Số Đẹp Đà Nẵng</strong>
</p>

<p align="center">
  <a href="https://biensovip.com"><img src="https://img.shields.io/badge/Website-Biensovip.com-D97706?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website" /></a>
  <a href="https://zalo.me/0815792699"><img src="https://img.shields.io/badge/Hotline%20%2F%20Zalo-0815.792.699-0068FF?style=for-the-badge&logo=zalo&logoColor=white" alt="Zalo" /></a>
  <a href="mailto:duymc64@gmail.com"><img src="https://img.shields.io/badge/Email-duymc64%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/.NET-8.0-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
  <img src="https://img.shields.io/badge/React-19.0-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Vite-8.x-646CFF?style=flat-square&logo=vite&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-16-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Icons-Lucide%20React-F6821F?style=flat-square&logo=lucide&logoColor=white" />
  <img src="https://img.shields.io/badge/Architecture-Clean%20Architecture-059669?style=flat-square" />
</p>

---

## 🌟 VỀ TỔ CHỨC BIỂN SỐ ĐẸP (BIENSOVIP)

**Biển Số Đẹp (BienSoDep)** là tổ chức vận hành nền tảng thương mại điện tử chuyên biệt [Biensovip.com](https://biensovip.com) — sàn giao dịch biển số xe đẹp ô tô và xe máy hàng đầu Việt Nam. Được bảo trợ bởi thương hiệu **Duy Đinh (Đà Nẵng)**, tổ chức cung cấp giải pháp toàn diện từ định giá thị trường, tra cứu phong thủy, ký gửi, mua bán và chuyển nhượng định danh biển số theo quy định pháp luật.

### 🎯 Sứ mệnh & Tầm nhìn
- **Minh bạch hóa thị trường:** Ứng dụng dữ liệu lớn (Big Data) và kết quả đấu giá thực tế từ Công ty Đấu giá Hợp danh Việt Nam (VPA) để đưa ra mức giá thị trường khách quan, khoa học.
- **Trải nghiệm mua sắm số:** Đưa việc tìm kiếm, tra cứu phong thủy và giao dịch biển số xe lên môi trường số hóa 100%, bảo mật và tự động hóa 24/7.
- **Tiêu chuẩn pháp lý vững chắc:** Tuân thủ Thông tư 24/2023/TT-BCA và Nghị định 13/2023/NĐ-CP về bảo vệ dữ liệu cá nhân.

---

## 🗂️ HỆ SINH THÁI MÃ NGUỒN (REPOSITORIES)

Toàn bộ hệ sinh thái phần mềm được xây dựng theo kiến trúc phân tách độc lập, khả năng mở rộng cao và kiểm thử nghiêm ngặt:

| Kho lưu trữ | Vai trò trong hệ thống | Công nghệ chính |
|---|---|---|
| 🌐 [**biensovip-web**](https://github.com/BienSoDep/biensovip-web) | **Frontend Web Application & Admin Portal**<br>Trải nghiệm khách hàng mua sắm, bói phong thủy, so sánh biển số và toàn bộ cổng quản trị kinh doanh, phê duyệt giá VPA. | React 19, Vite 8, TanStack Query v5, Lucide Icons, Recharts, Framer Motion, Vanilla CSS Tokens |
| ⚙️ [**biensovip-backend**](https://github.com/BienSoDep/biensovip-backend) | **Core RESTful API & Background Workers**<br>Hệ thống xử lý nghiệp vụ, thuật toán VPA Price Engine, crawler tự động, cổng thanh toán VietQR / ZaloPay, xác thực 2FA. | .NET 8 (C# 12), Clean Architecture, Minimal APIs, EF Core 8, PostgreSQL 16, SignalR |
| 📚 [**biensodep-infrastructure**](https://github.com/BienSoDep/biensodep-infrastructure) | **Master Specifications & Non-Code Resources**<br>Hồ sơ đặc tả 57 Use Cases qua 5 Giai đoạn, thiết kế 55 bảng CSDL 3NF, hợp đồng pháp lý, tài liệu thương hiệu và DevOps runbook. | Markdown, LaTeX, DBML, Assets, Python Scripts |
| 📦 [**biensovip-demo-ui**](https://github.com/BienSoDep/biensovip-demo-ui) | **Standalone Preview & Staging Deployment**<br>Gói giao diện xem trước độc lập phục vụ trình diễn, kiểm thử đối tác và triển khai container nhanh. | React 19, Docker Multi-stage, Nginx Alpine, Vercel |

---

## 🚀 CÔNG NGHỆ & ĐIỂM NHẤN ĐẶC SẮC

### 1. 🤖 VPA Market Price Engine (UC49)
- Thu thập tự động kết quả đấu giá biển số quốc gia theo thời gian thực.
- Thuật toán phân cấp 3 tầng suy luận giá thị trường dựa trên độ tương đồng:
  1. **Cấp 1:** Trùng đuôi số thực tế (cùng tỉnh thành, loại xe).
  2. **Cấp 2:** Cùng loại biển & cùng tỉnh thành theo phân khúc số.
  3. **Cấp 3:** Cùng loại biển trên toàn quốc (fallback).
- Minh bạch 100% công thức định giá: $\text{Giá gợi ý} = \text{TB giá trúng} \times \text{Hệ số (Factor)}$ kèm 50 phiên đấu giá mẫu chứng minh.

### 2. 🎨 Trải Nghiệm Giao Diện Đẳng Cấp
- **100% Lucide Icons:** Toàn bộ biểu tượng chuẩn hóa qua thư viện `lucide-react`, loại bỏ emoji và icon ký tự thô.
- **Bộ lọc 4 tiêu chí chuẩn hóa:** Đồng bộ xuyên suốt các trang Biển số shop, Biển VPA và Kết quả đấu giá (`Loại biển`, `Loại xe`, `Tỉnh/thành`, `Nổi bật`).
- **Phôi biển số dập nổi chuẩn BCA:** Mô phỏng đồ họa chính xác tỷ lệ, font chữ, quốc kỳ và biểu tượng theo tiêu chuẩn Bộ Công An.

### 3. 💳 Giữ Chỗ & Thanh Toán Tự Động 24/7
- Khóa giữ biển tự động trong 15 phút (`HOLDING`).
- Tích hợp VietQR Napas247 động và ZaloPay Merchant QR, xác thực tức thời qua Webhook có chữ ký bảo mật HMAC-SHA256.

### 4. 🔮 Trợ Lý Phong Thủy Ngũ Hành
- Thuật toán bói phong thủy theo kinh dịch, số nút may mắn, quẻ biến và tương sinh ngũ hành.
- Gợi ý biển số hợp tuổi, hợp mệnh cho chủ xe cá nhân và doanh nghiệp.

---

## 📍 THÔNG TIN LIÊN HỆ & KẾT NỐI

<p align="center">
  <strong>DOANH NGHIỆP BIỂN SỐ ĐẸP DUY ĐINH</strong><br>
  📍 <strong>Địa chỉ:</strong> Số 06 An Thượng 30, P. Mỹ An, Q. Ngũ Hành Sơn, TP. Đà Nẵng<br>
  📞 <strong>Hotline / Zalo:</strong> <a href="tel:0815792699">0815 792 699</a><br>
  ✉️ <strong>Email:</strong> <a href="mailto:duymc64@gmail.com">duymc64@gmail.com</a><br>
  🌐 <strong>Website chính thức:</strong> <a href="https://biensovip.com">https://biensovip.com</a>
</p>

---

<p align="center">
  <sub>© 2026 BienSoDep Organization. Bản quyền thuộc về Duy Đinh — Biển Số Đẹp Đà Nẵng.</sub>
</p>
