# 4JT V1 — PWA quản lý công việc giao hàng

## Chạy thử

Yêu cầu Node.js 20+.

```bash
npm install
npm run dev
```

Mở địa chỉ được Vite hiển thị trên máy tính. Để sử dụng trên iPhone qua mạng, triển khai lên hosting HTTPS (ví dụ Vercel, Netlify, Cloudflare Pages). Chạy `npm run build` tạo thư mục `dist/` để triển khai.

## Cài trên iPhone

Sau khi ứng dụng được triển khai tại địa chỉ HTTPS: mở bằng Safari → Chia sẻ → Thêm vào Màn hình chính.

## Tính năng

- 6 màn hình: Tổng quan, Đơn hàng, Thu nhập, Công nợ, Tài chính, Lịch sử.
- KPI tháng, đơn giá và khoản cố định tùy chỉnh.
- Công nợ khách hàng: chọn tên cũ bằng gợi ý, nhiều khoản nợ, trả một phần hoặc trả đủ, xem theo ngày.
- 6 danh mục chi phí: Ăn uống, Xăng xe, Sửa xe, Thay nhớt, Điện thoại, Chi phí khác.
- Thống kê chi phí ngày/tháng, ghi nhận tiết kiệm.
- Sao lưu và khôi phục JSON từ phần Cài đặt.
- PWA với service worker hỗ trợ tải lại khi ngoại tuyến sau khi mở trực tuyến ít nhất một lần.

## Giới hạn quan trọng

- Dữ liệu lưu trong localStorage của **một trình duyệt trên một thiết bị**, không có tài khoản hay đồng bộ. Xóa dữ liệu website có thể làm mất dữ liệu. **Sao lưu thường xuyên**.
- Chưa có lịch sử sửa/xóa chi tiết (audit trail), hoàn tác giao dịch, phiên bản hóa đơn giá theo thời gian, hay bảo mật máy chủ.
- Công nợ không được tính là chi phí và khoản thu hồi không được tính là thu nhập giao hàng.
- Khoản cố định tháng chỉ được tính nếu có ít nhất một ngày ghi nhận đơn trong tháng.
- Đây là mã nguồn ứng dụng, chưa được đưa lên hosting công khai.
