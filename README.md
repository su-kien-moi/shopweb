# HQL Web Studio

Website tĩnh gồm 3 trang: trang chủ, danh mục sản phẩm và trang cá nhân có nhật ký.

## Cấu trúc

- `index.html` — web chính, dịch vụ, bảng giá, FAQ, liên hệ
- `san-pham.html` — danh mục sản phẩm có filter + modal chi tiết
- `about.html` — trang cá nhân, đổi ngôn ngữ VI/EN, nhật ký đăng ảnh/video/file

## Chạy local

Mở `index.html` bằng trình duyệt, hoặc dùng local server:

```bash
python3 -m http.server 8000
```

Rồi mở `http://localhost:8000`.

## Deploy GitHub Pages

1. Push cả 3 file lên repo
2. Vào **Settings → Pages → Source: Deploy from branch → main → / (root)**
3. Truy cập `https://username.github.io/repo-name/`

## Tuỳ chỉnh

- **Số Zalo**: sửa `CONFIG.zaloPhone` trong cả 3 file
- **Sản phẩm**: sửa mảng `PRODUCTS` trong `san-pham.html`
- **Nhật ký**: dữ liệu lưu bằng IndexedDB, không cần sửa code

## Lưu ý

- Nhật ký trong `about.html` lưu dữ liệu **trong trình duyệt** (IndexedDB).
- Xoá dữ liệu trình duyệt sẽ mất bài.
- Muốn sync giữa nhiều máy cần backend riêng.
