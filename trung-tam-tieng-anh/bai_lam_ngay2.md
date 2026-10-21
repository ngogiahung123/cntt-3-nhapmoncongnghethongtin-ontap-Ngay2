# BÀI LÀM – ÔN TẬP NGÀY 2

- **Họ tên:**
- **Lớp:**
- **Link repository:**
- **Hệ điều hành (Windows/macOS):**

## Bài 1. Lọc log thủ công

### Lệnh đã chạy

```shell
# Ghi lệnh vào đây (xoá dòng này)

```

### 2 dòng lỗi đầu tiên trong error_report.txt

```text
(Dán kết quả vào đây – xoá dòng này)

```

## Bài 2. Đếm bằng pipeline

### Lệnh

```shell
# Ghi 2 lệnh vào đây, mỗi lệnh một dòng (xoá dòng này)

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
WARNING trong access.log:
ERROR trong payment.log:
```

## Bài 3. Chạy script auto_warning (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
.\auto_warning.ps1

```

### Nội dung file logs/warning_report.txt

```text
Dang loc canh bao thanh toan...
Hoan thanh!
=== CANH BAO THANH TOAN ===

2025-10-18 09:19:13 [WARNING] Cong thanh toan phan hoi cham
2025-10-18 09:28:16 [WARNING] Nhieu lan nhap sai ma OTP
2025-10-18 09:43:01 [WARNING] So du vi gan bang hoc phi
2025-10-18 09:46:22 [WARNING] So du vi gan bang hoc phi
2025-10-18 09:49:43 [WARNING] So du vi gan bang hoc phi

```

## Bài 4. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
"=== TONG HOP ACCESS LOG ===" > .\logs\tong_hop_ngay2.txt
gc .\logs\access.log | Select-String "ERROR" >> .\logs\tong_hop_ngay2.txt
(gc .\logs\payment.log | Select-String "WARNING").count >> .\logs\tong_hop_ngay2.txt
```

### Nội dung file logs/tong_hop_ngay2.txt

```text
=== TONG HOP ACCESS LOG ===

2025-10-18 08:17:59 [ERROR] Khong tim thay trang /lich-thi (404)
2025-10-18 08:25:55 [ERROR] Het thoi gian cho (timeout)
2025-10-18 08:33:51 [ERROR] Ket noi may chu du lieu that bai
2025-10-18 08:37:19 [ERROR] Ket noi may chu du lieu that bai
2025-10-18 08:49:43 [ERROR] Het thoi gian cho (timeout)
2025-10-18 08:53:11 [ERROR] Het thoi gian cho (timeout)


5

```

## Bài 5. Câu hỏi ngắn

- **a) > Là ghi đè lên bản ghi cũ còn >> là thêm vào cuối của bản ghi cũ**
- **b) Thì sẽ mấy dòng === TONG HOP ACCESS LOG ===**
- **c) Vì đường dẫn tuyệt đối yêu cầu cấu trúc mọi máy tính phải giống nhau nếu không đường truyền sẽ bị hỏng còn tương đối thì không cần**

## Tự chấm (điền sau khi có đáp án)

- **Điểm tự chấm:** ..../100
- **Lỗi mình đã mắc và cách sửa:**
