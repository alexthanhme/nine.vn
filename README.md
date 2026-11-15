# nine.vn

Landing page tĩnh của nine (thương hiệu mẹ) và ninePOS. Không cần build, không cần hosting trả phí.

## Cấu trúc

| File | Vai trò |
|---|---|
| `index.html` | Toàn bộ trang (HTML, CSS, JS và logo SVG nằm chung một file) |
| `404.html` | Trang báo lỗi đường dẫn |
| `og.png` | Ảnh hiện khi chia sẻ link lên Facebook, Zalo |
| `favicon.*`, `apple-touch-icon.png`, `icon-*.png`, `site.webmanifest` | Biểu tượng trang |
| `CNAME` | Báo cho GitHub Pages biết tên miền là `nine.vn` |
| `.nojekyll`, `robots.txt` | Cấu hình phụ |

## Đưa lên GitHub Pages (miễn phí)

1. Tạo repo công khai trên GitHub, ví dụ `alexthanhme/nine.vn`.
2. Đưa toàn bộ file trong thư mục này vào nhánh `main` (kéo thả trên web GitHub cũng được).
3. Vào **Settings → Pages**, mục **Source** chọn **Deploy from a branch**, nhánh `main`, thư mục `/ (root)`, bấm **Save**.
4. Ở **Custom domain** nhập `nine.vn`, bấm **Save**.

## Trỏ tên miền ở PA Việt Nam

Đăng nhập trang quản lý của PA Việt Nam, vào phần quản lý DNS của `nine.vn`, xóa các bản ghi A hoặc CNAME cũ của `@` và `www` nếu có, rồi thêm:

| Host | Loại | Giá trị |
|---|---|---|
| `@` | A | `185.199.108.153` |
| `@` | A | `185.199.109.153` |
| `@` | A | `185.199.110.153` |
| `@` | A | `185.199.111.153` |
| `www` | CNAME | `alexthanhme.github.io` |

Tên miền phải đang dùng nameserver mặc định của PA Việt Nam thì các bản ghi này mới có hiệu lực. Chờ DNS cập nhật (thường vài phút tới vài giờ), sau đó quay lại **Settings → Pages** và bật **Enforce HTTPS**.

## Sửa nội dung

Mở `index.html`, tìm đúng câu chữ cần đổi và sửa trực tiếp. Màu và font nằm ở khối `:root` đầu phần `<style>`. Logo là hình vẽ SVG gốc của bộ nhận diện, không thay bằng chữ gõ.
