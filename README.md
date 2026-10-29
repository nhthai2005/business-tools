# Shantek Tools

Trang chủ tổng hợp các công cụ phần mềm hữu ích cho doanh nghiệp, được xây dựng bằng HTML, CSS và JavaScript thuần. Website có giao diện responsive cho desktop, tablet và mobile.

- **Website public:** https://tools.shantek.vn
- **Thương hiệu:** Shantek BPO & IT Solutions
- **Website công ty:** https://shantek.vn

## Các công cụ

| Công cụ | File |
|---|---|
| Lập báo giá | `BaoGia.html` |
| Chấm công & tính lương | `ChamCongTinhLuong.html` |
| Quản lý công việc Gantt | `QuanLyCongViec_Gantt.html` |
| Quản lý kho — Xuất Nhập Tồn | `QuanLyKho_XNT.html` |
| Quyết toán thuế thu nhập cá nhân | `QuyetToanThueTNCN.html` |
| Sổ kế toán hộ kinh doanh | `SoKeToanHoKinhDoanh.html` |

## Cấu trúc thư mục

Đặt `index.html` và toàn bộ file công cụ trong cùng thư mục gốc để các liên kết tương đối hoạt động chính xác.

```text
.
├── index.html
├── README.md
├── BaoGia.html
├── ChamCongTinhLuong.html
├── QuanLyCongViec_Gantt.html
├── QuanLyKho_XNT.html
├── QuyetToanThueTNCN.html
└── SoKeToanHoKinhDoanh.html
```

## Chạy thử trên máy

Không cần cài framework hoặc build tool để xem trang chủ:

1. Clone hoặc tải repository về máy.
2. Mở `index.html` bằng trình duyệt.

Hoặc chạy HTTP server tĩnh bằng Python từ thư mục dự án:

```bash
python -m http.server 8000
```

Sau đó truy cập `http://localhost:8000`.

## Public website tại `tools.shantek.vn`

Có thể triển khai bằng Cloudflare Pages nếu source được lưu trên GitHub.

### GitHub + Cloudflare Pages

1. Tạo repository GitHub và tải `index.html`, `README.md` cùng các file công cụ lên repository.
2. Trong Cloudflare Dashboard, mở **Workers & Pages** và tạo Pages project kết nối repository GitHub.
3. Với HTML tĩnh thuần, để trống build command nếu được phép và đặt output directory là thư mục chứa `index.html` (thường là thư mục gốc `/`).
4. Deploy và kiểm tra URL `pages.dev` được cấp.
5. Trong project Pages, vào **Custom domains**, thêm `tools.shantek.vn` và làm theo hướng dẫn thiết lập DNS của Cloudflare.
6. Kiểm tra `https://tools.shantek.vn` và mở từng công cụ để xác nhận các liên kết hoạt động.

### Deploy bằng Wrangler CLI (tùy chọn)

Chạy tại thư mục chứa `index.html` và các file công cụ:

```bash
npx wrangler pages deploy . --project-name=shantek-tools
```

Lệnh này yêu cầu đăng nhập Cloudflare; project `shantek-tools` cần tồn tại hoặc được tạo theo hướng dẫn của Wrangler. Nếu dùng Git integration, ưu tiên kết nối repository với Cloudflare Pages để tự động deploy theo nhánh production đã chọn.

## Thương hiệu & liên hệ

- **Đại diện:** Nguyễn Hồng Thái
- **Thương hiệu:** Shantek BPO & IT Solutions
- **Điện thoại / Zalo / WhatsApp:** +84 936 436 166
- **Email:** thainguyenbpo@gmail.com
- **Website:** https://shantek.vn
- **LinkedIn:** https://www.linkedin.com/in/nguyenhongthai

## Lưu ý bảo mật

- Website public có thể cho phép mọi người truy cập và tải các file HTML đã xuất bản.
- Không đưa API key, token, mật khẩu, dữ liệu khách hàng hoặc thông tin bí mật vào repository.
- Nếu công cụ xử lý dữ liệu lương, thuế hoặc kế toán, hãy kiểm tra cách dữ liệu được lưu trữ và truyền đi trước khi public.
- Các bước triển khai trên là hướng dẫn tham khảo; hãy kiểm tra cấu hình repository và Cloudflare project thực tế trước khi deploy.

## License

Chưa chỉ định giấy phép. Nếu muốn người khác tái sử dụng hoặc sửa đổi source, hãy thêm file `LICENSE` với giấy phép phù hợp.
