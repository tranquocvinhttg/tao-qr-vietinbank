# Tạo QR VietinBank — đưa lên GitHub và Vercel

Bản đã tối ưu cho điện thoại, gồm 7 mẫu ảnh QR. Tạo mã và ảnh ngay trong trình duyệt; không cần cấu hình API hoặc cơ sở dữ liệu. Tên chủ tài khoản do người dùng nhập. Ảnh PNG tải về có kích thước 1600 × 2920 px.

## Chuẩn bị

Giải nén ZIP bằng Extract All trên Windows. Có 3 tệp:

| Tệp | Mục đích |
| --- | --- |
| index.html | Toàn bộ trang web, hình ảnh, phông chữ và bộ tạo QR |
| vercel.json | Cấu hình để Vercel phục vụ trang HTML trực tiếp |
| README.md | Hướng dẫn này |

## Đưa lên GitHub

1. Đăng nhập https://github.com/new.
2. Đặt Repository name là `tao-qr-vietinbank`, chọn Private và bấm Create repository.
3. Trong kho mới còn trống, bấm **uploading an existing file**. Với kho đã có tệp, dùng **Add file → Upload files**.
4. Kéo cả 3 tệp đã giải nén vào, rồi commit/lưu lên nhánh `main`. Nếu giao diện tạo nhánh riêng, hoàn thành pull request để đưa tệp vào `main`.
5. Kiểm tra `index.html`, `vercel.json`, `README.md` nằm ngay ở cấp đầu tiên của kho. Tải các tệp bên trong ZIP lên GitHub.

## Đưa lên Vercel

1. Đăng nhập https://vercel.com bằng tài khoản liên kết với GitHub.
2. Chọn **New Project**, kết nối GitHub nếu được yêu cầu, cấp quyền cho kho `tao-qr-vietinbank` rồi chọn kho đó để import.
3. Kiểm tra các mục dưới đây. `vercel.json` đã đặt sẵn cấu hình triển khai:

| Mục | Giá trị |
| --- | --- |
| Framework Preset | Other |
| Root Directory | Thư mục gốc, mặc định `./` |
| Build Command | Để trống |
| Install Command | Để trống |
| Output Directory | `.` |
| Environment Variables | Không cần thêm |

4. Bấm **Deploy**. Sau khi triển khai thành công, mở URL production của dự án có đuôi `.vercel.app`.
5. Mở link bằng điện thoại, thử nhập STK và tên, vuốt chọn mẫu và tải PNG. Quét QR bằng ứng dụng ngân hàng để đối chiếu đúng ngân hàng, STK và tên người nhận.

## Cập nhật sau này

Thay `index.html` trong kho bằng bản mới và commit vào nhánh production `main`; Vercel sẽ tự tạo lần triển khai mới. Giữ tên `index.html` để trang mở ở địa chỉ gốc.

## Gói sử dụng

Vercel Hobby chỉ dành cho cá nhân, phi thương mại. Khi dùng phục vụ hoạt động của chi nhánh/ngân hàng, chọn gói cho doanh nghiệp như Pro hoặc Enterprise phù hợp điều khoản Vercel.

## Tài liệu chính thức

- GitHub — tạo kho: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository
- GitHub — tải tệp: https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
- Vercel — import Git: https://vercel.com/docs/git
- Vercel — trang HTML tĩnh: https://vercel.com/docs/builds/configure-a-build
- Vercel — vercel.json: https://vercel.com/docs/project-configuration/vercel-json
- Vercel — Hobby: https://vercel.com/docs/plans/hobby
