<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=D97706,1E293B&height=220&section=header&text=BIEN%20SO%20DEP&fontSize=60&fontColor=ffffff&fontAlignY=42&desc=Nen%20tang%20giao%20dich%20%26%20dinh%20gia%20bien%20so%20xe%20hang%20dau%20Viet%20Nam&descSize=18&descAlignY=62&animation=fadeIn" alt="BienSoDep Banner" />
</p>

<p align="center">
  <a href="https://biensovip.com">
    <img src="https://img.shields.io/badge/biensovip.com-Live%20Platform-D97706?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website" />
  </a>
  <a href="https://zalo.me/0815792699">
    <img src="https://img.shields.io/badge/Zalo%20%2F%20Hotline-0815.792.699-0068FF?style=for-the-badge&logo=zalo&logoColor=white" alt="Zalo" />
  </a>
  <a href="mailto:duymc64@gmail.com">
    <img src="https://img.shields.io/badge/Email-duymc64%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

<br/>

---

## Giới Thiệu Dự Án

**Biensovip.com** là nền tảng thương mại điện tử chuyên biệt đầu tiên tại Việt Nam dành riêng cho thị trường **biển số xe ô tô và xe máy đẹp**. Được phát triển và vận hành bởi tổ chức **BienSoDep**, dưới thương hiệu **Duy Đinh — Biển Số Đẹp Đà Nẵng**, dự án giải quyết một bài toán thực tế: thị trường mua bán biển số xe đẹp tại Việt Nam lâu nay thiếu minh bạch về giá cả và chưa được số hóa đúng nghĩa.

Hệ thống được xây dựng hoàn toàn mới từ đầu qua **5 giai đoạn phát triển** với **57 Use Case đặc tả đầy đủ**, áp dụng kiến trúc phần mềm tiêu chuẩn enterprise (Clean Architecture, ACID database, RBAC, HMAC Webhook) và tích hợp dữ liệu đấu giá thực tế từ **VPA — Công ty Đấu giá Hợp danh Việt Nam**.

---

## Vấn Đề & Giải Pháp

| Vấn đề thị trường | Giải pháp của Biensovip |
|---|---|
| Giá biển số thiếu cơ sở khoa học, phụ thuộc cảm tính người bán | **VPA Price Engine**: Tính giá gợi ý từ kết quả đấu giá thực tế theo thuật toán 3 tầng |
| Không có kênh giao dịch chính thống, an toàn | **Cổng mua bán số hóa** với giữ chỗ tự động 15 phút, thanh toán VietQR/ZaloPay |
| Khó tra cứu phong thủy, hợp tuổi hợp mệnh | **Trợ lý phong thủy ngũ hành** tích hợp trực tiếp trên từng biển số |
| Admin quản lý kho biển thủ công, mất thời gian | **Admin Portal đầy đủ** với quản lý kho, duyệt giá VPA, CRM khách hàng |
| Biển số không có hình ảnh chuẩn pháp lý | **Phôi biển số số hóa** theo đúng tiêu chuẩn đồ họa Bộ Công An |

---

## Hệ Sinh Thái Repositories

Toàn bộ hệ thống được tổ chức thành 4 repository độc lập với vai trò phân tách rõ ràng:

| Repository | Vai trò | Stack chính | Quyền |
|---|---|---|:---:|
| [**biensovip-web**](https://github.com/BienSoDep/biensovip-web) | Frontend SPA & Admin Portal | React 19, Vite 8, TanStack Query v5, Framer Motion, Vanilla CSS Design Tokens | Public |
| [**biensovip-backend**](https://github.com/BienSoDep/biensovip-backend) | Core RESTful API & Background Workers | .NET 8, Clean Architecture, EF Core 8, PostgreSQL 16, SignalR, JWT, HMAC | Private |
| [**biensodep-infrastructure**](https://github.com/BienSoDep/biensodep-infrastructure) | Master Docs, Contracts & Brand Assets | Markdown, DBML, LaTeX, Python, Excel | Private |
| [**biensovip-demo-ui**](https://github.com/BienSoDep/biensovip-demo-ui) | Staging Preview & Container Deploy | React 19, Docker Multi-stage, Nginx Alpine, Vercel | Private |

---

## Kiến Trúc Hệ Thống

Backend được thiết kế theo **Clean Architecture** với 4 layer tách biệt hoàn toàn:

```
Biensovip.Api          ← Web Host: Endpoints, Middleware, Auth
  └─► Biensovip.Infrastructure  ← EF Core, Repos, Background Workers, External Services
        └─► Biensovip.Application  ← DTOs, Business Interfaces, Use Case Logic
              └─► Biensovip.Domain  ← Core Entities, Enums (không phụ thuộc vào bất kỳ layer nào)
```

Database được thiết kế chuẩn **3NF/ACID** với **55 bảng**, hỗ trợ JSONB và PostgreSQL Trigram Index cho tìm kiếm toàn văn nhanh.

---

## Công Nghệ Nền Tảng

<p align="center">
  <img src="https://img.shields.io/badge/.NET-8.0-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
  <img src="https://img.shields.io/badge/React-19.0-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/PostgreSQL-16-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Vite-8.x-646CFF?style=flat-square&logo=vite&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-Containerized-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/SignalR-Realtime-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
  <img src="https://img.shields.io/badge/Caddy-v2%20Reverse%20Proxy-1F88C0?style=flat-square&logo=caddy&logoColor=white" />
  <img src="https://img.shields.io/badge/Architecture-Clean%20Architecture-059669?style=flat-square" />
</p>

---

## Tính Năng Theo Từng Phân Hệ

### 1. VPA Market Price Engine (UC49)

Đây là tính năng cốt lõi và độc đáo nhất của nền tảng. Hệ thống tự động **cào kết quả đấu giá biển số quốc gia** từ cổng VPA và áp dụng **thuật toán phân cấp 4 tầng** để suy luận giá thị trường khách quan:

| Tầng | Điều kiện | Độ tin cậy |
|:---:|---|:---:|
| **Tầng 1** | Trùng đuôi số thực tế + cùng tỉnh thành + cùng loại xe | Cao nhất |
| **Tầng 2** | Cùng loại biển + cùng tỉnh thành theo phân khúc số | Cao |
| **Tầng 3** | Cùng loại biển trên toàn quốc (fallback khi tỉnh thiếu dữ liệu) | Trung bình |
| **Tầng 4** | Giá khởi điểm của chính biển số đó | Tham khảo |

**Công thức:** `Giá gợi ý = Trung bình giá trúng × Hệ số thị trường (Factor)`

Mỗi kết quả định giá đều kèm **50 phiên đấu giá mẫu** thực tế làm căn cứ minh bạch, cùng mô tả phương thức suy luận (`matchType`) và hệ số áp dụng (`factor`).

---

### 2. Cổng Mua Bán & Giữ Chỗ Tự Động

- Khách hàng xem biển, nhấn **"Giữ chỗ"** → hệ thống tự động khóa biển trong **15 phút** (trạng thái `HOLDING`)
- Sinh mã **VietQR Napas247 động** hoặc **ZaloPay Merchant QR** theo thời gian thực
- Webhook nhận xác nhận thanh toán, xác thực chữ ký **HMAC-SHA256** để chống giả mạo
- Tự động chuyển trạng thái biển → `SOLD` hoặc giải phóng lại nếu hết thời gian giữ

---

### 3. Trợ Lý Phong Thủy Ngũ Hành

- Phân tích biển số theo **kinh dịch**, số nút may mắn, quẻ biến và tương sinh ngũ hành
- Gợi ý biển số **hợp tuổi, hợp mệnh** cho cá nhân (sinh năm, can chi) và doanh nghiệp (ngành nghề)
- Tích hợp ngay trên trang chi tiết biển số, không cần màn hình riêng

---

### 4. Phôi Biển Số Số Hóa (Chuẩn BCA)

- Mô phỏng đồ họa chính xác **phôi biển số xe** theo tiêu chuẩn Bộ Công An Việt Nam
- Đúng tỷ lệ, font chữ, bố cục, màu sắc theo từng loại biển (ô tô trắng, xe máy vàng, biển xanh...)
- Hiển thị quốc kỳ và biểu tượng đúng vị trí theo quy định

---

### 5. Admin Portal Quản Trị Toàn Diện

- **Quản lý kho biển:** Thêm/sửa/xóa biển, gắn nhãn, ẩn hiện, cập nhật giá bán
- **Duyệt giá VPA:** Xem giá gợi ý từ engine, so sánh với giá đang bán, phê duyệt hoặc điều chỉnh
- **Phân tích thị trường:** Biểu đồ biến động giá theo tỉnh thành, loại biển, thời gian
- **CRM Khách hàng:** Quản lý yêu cầu tư vấn, lịch sử liên hệ, trạng thái giữ chỗ
- **Quản lý Crawler VPA:** Kích hoạt cào thủ công, lịch sử các đợt crawl, xử lý lỗi

---

### 6. Bộ Lọc & Tìm Kiếm Nâng Cao

Bộ lọc **4 tiêu chí chuẩn hóa** được đồng bộ xuyên suốt 3 trang chính:

- **Loại biển:** Ô tô / Xe máy / Biển tỉnh / Biển thành phố...
- **Loại xe:** Phân loại theo nhóm phương tiện
- **Tỉnh / Thành phố:** 63 tỉnh thành Việt Nam
- **Nổi bật:** Lọc nhanh biển VIP, biển ngũ quý, biển siêu đẹp...

Tìm kiếm hỗ trợ **PostgreSQL Trigram Index** giúp tra cứu biển số theo chuỗi ký tự một phần, không cần nhập chính xác toàn bộ.

---

## Quy Mô Dự Án

| Hạng mục | Chi tiết |
|---|---|
| Số Use Case đặc tả | 57 UC qua 5 Giai đoạn phát triển |
| Số bảng cơ sở dữ liệu | 55 bảng thiết kế chuẩn 3NF/ACID |
| Số API Endpoints | 30+ endpoints (Public + Admin) |
| Hợp đồng phát triển | 4 giai đoạn hợp đồng kinh tế (182+ man-days) |
| Hạ tầng tài liệu | SRS, BA Specs, Test Plan, Security Framework, DevOps Runbook |

---

## Bảo Mật & Tuân Thủ Pháp Lý

- **Xác thực:** JWT HS256 + Refresh Token Rotation + TOTP 2FA (Google Authenticator)
- **Mã hóa:** BCrypt (mật khẩu người dùng), HMAC-SHA256 (xác thực Webhook thanh toán)
- **Phân quyền:** RBAC (Role-Based Access Control) — Super Admin / Admin / Customer
- **Pháp lý:** Tuân thủ **Thông tư 24/2023/TT-BCA** về biển số xe và **Nghị định 13/2023/NĐ-CP** về bảo vệ dữ liệu cá nhân
- **Bảo mật web:** OWASP Security Framework, Security Headers Middleware, Rate Limiter

---

## Liên Hệ

<p align="center">
  <strong>Doanh Nghiệp Biển Số Đẹp — Duy Đinh</strong><br/>
  Số 06 An Thượng 30, P. Mỹ An, Q. Ngũ Hành Sơn, TP. Đà Nẵng<br/><br/>
  <a href="tel:0815792699">0815 792 699</a> &nbsp;|&nbsp;
  <a href="mailto:duymc64@gmail.com">duymc64@gmail.com</a> &nbsp;|&nbsp;
  <a href="https://biensovip.com">biensovip.com</a>
</p>

<p align="center">
  <sub>© 2026 BienSoDep Organization. Bản quyền thuộc về Duy Đinh — Biển Số Đẹp Đà Nẵng.</sub>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=D97706,1E293B&height=100&section=footer" alt="footer" />
</p>
