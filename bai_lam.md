# BÀI LÀM – HACKATHON 02

- **Mã đề:** 02
- **Họ tên: Trịnh Phú Thịnh**
- **Lớp:HCM_KS26_CNTT1**
- **Link repository:**
- **Hệ điều hành (Windows/macOS):Windows**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng
pwd
ls -Force
mv huong_dan_van_hanh.txt docs\
mkdir backup
copy data\luot_gui_xe_thang_2.xlsx backup\
rm *.tmp
Get-ChildItem -Recurse -Force
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
    Directory: C:\Users\thien\Downloads\starter-kit\starter-kit\bai-xe-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   8:02 AM                backup
d-----        11/11/2026   7:53 AM                data
d-----        11/11/2026   8:00 AM                docs
d-----        11/11/2026   7:51 AM                evidence
d-----        11/11/2026   7:53 AM                logs
d-----        11/11/2026   7:49 AM                web
------         11/3/2026   7:06 AM             73 .env
-a----         11/3/2026   7:06 AM           2412 bai_lam.md


    Directory:
    C:\Users\thien\Downloads\starter-kit\starter-kit\bai-xe-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM           6132 luot_gui_xe_thang_2.xlsx


    Directory: C:\Users\thien\Downloads\starter-kit\starter-kit\bai-xe-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM           6132 luot_gui_xe_thang_2.xlsx


    Directory: C:\Users\thien\Downloads\starter-kit\starter-kit\bai-xe-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM            155 huong_dan_van_hanh.txt


    Directory: C:\Users\thien\Downloads\starter-kit\starter-kit\bai-xe-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:06 AM            977 gate.log


    Directory: C:\Users\thien\Downloads\starter-kit\starter-kit\bai-xe-website\web


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   7:49 AM                images
------         11/3/2026   7:06 AM            600 app.js
------         11/3/2026   7:06 AM            533 index.html
------         11/3/2026   7:06 AM            460 style.css


    Directory:
    C:\Users\thien\Downloads\starter-kit\starter-kit\bai-xe-website\web\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
------         11/3/2026   7:06 AM           3089 logo-parkeasy.png



```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
Get-Content logs\gate.log | Select-String "status=500" >> logs\loi_500.txt

```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
2026-02-28 08:08:39 POST /api/cho-trong status=500
2026-02-28 08:23:23 POST /api/cho-trong status=500

```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
Get-Content logs\gate.log | Select-String "status=400" | Measure-Object

```

```text
0

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
Y
.\tong_hop.ps1

```

### Nội dung file logs/tong_hop.txt

```text


```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [X] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [X] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [X] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 |  |  |  |
| 2 |  |  |  |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/luot_gui_xe_thang_2.xlsx`, không cần ghi vào đây.
