# Sổ tay đọc sách — PWA

## Cài đặt GitHub Pages
1. Giải nén ZIP và tải **các tệp bên trong** (không phải thư mục cha) lên thư mục gốc repository.
2. GitHub → Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save.
3. Mở URL HTTPS của Pages.
4. iPhone: Safari → Share → Add to Home Screen. Android: Chrome → Install app/Add to Home screen. Máy tính: Chrome/Edge → biểu tượng Install trên thanh địa chỉ (nếu trình duyệt hỗ trợ).

## Dữ liệu và ngoại tuyến
- Giữ nguyên localStorage key `book-quotes-library-v1`, nên dữ liệu cũ trên **cùng origin và đường dẫn** vẫn được đọc. Không tự động đồng bộ giữa thiết bị hoặc giữa các tên miền khác nhau.
- Giao diện, thêm/sửa/xóa sách, trích dẫn, tìm kiếm và xuất/nhập JSON dùng offline sau lần tải thành công.
- Nên **xuất JSON sao lưu định kỳ**; xóa dữ liệu website, chế độ riêng tư hoặc đổi domain có thể mất quyền truy cập dữ liệu cũ.
- Clipboard có thể cần HTTPS và quyền trình duyệt.

## Cập nhật
- Sửa mã và tăng hằng `VERSION` trong `sw.js`, rồi tải các file mới lên GitHub.
- Khi online, Service Worker sẽ lấy bản mới; tải lại trang để áp dụng. Không xóa localStorage khi cập nhật.
- Nếu trang không cập nhật, đóng và mở lại ứng dụng, hoặc làm mới trang khi có mạng.

## Kiểm tra
- Kiểm tra tạo sách, thêm/sửa/xóa trích dẫn, xem thêm/ẩn bớt sau 3 dòng, tìm kiếm, sắp xếp, nhập/xuất JSON.
- Mở một lần khi online, sau đó bật offline trong DevTools và tải lại để kiểm tra cache.
- Kiểm tra cài đặt trên thiết bị thực tế sau khi triển khai.
