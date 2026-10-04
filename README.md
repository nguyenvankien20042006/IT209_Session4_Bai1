# Báo Cáo Bài Tập 1: Khởi tạo Local Repository và Cấu hình danh tính

- **Môn học:** IT209
- **Bài tập:** Session 04 - Bài 1 (ex1)
- **Đường dẫn nộp bài dự kiến:** `homework/session_04/ex1/`

---

## 1. Mục tiêu thực hiện
- Khởi tạo Git repository trống tại thư mục làm việc cục bộ.
- Thiết lập thông tin danh tính tác giả (`user.name` và `user.email`) ở cấp độ **cục bộ (`--local`)**.
- Tạo tệp tin mới, đưa vào Staging Area (`git add`) và thực hiện commit đầu tiên (`git commit`).
- Kiểm tra trạng thái và lịch sử commit thông qua các lệnh kiểm tra.

---

## 2. Các bước và lệnh đã thực hiện

### Bước 1: Khởi tạo Git Repository cục bộ
```bash
git init
```
**Kết quả:**
```text
Initialized empty Git repository in E:/IT209/IT209-SS4/SS4-B1/.git/
```

---

### Bước 2: Cấu hình danh tính ở cấp độ Cục bộ (Local)
> **Lưu ý:** Sử dụng cờ `--local` để cấu hình chỉ áp dụng riêng cho repository này, không ảnh hưởng đến cấu hình `--global`.

```bash
# Cấu hình tên tác giả cục bộ
git config --local user.name "LLL"

# Cấu hình email tác giả cục bộ
git config --local user.email "Zeikezan12345@gmail.com"
```

---

### Bước 3: Thêm tệp tin vào Staging Area và tạo Commit đầu tiên
```bash
# Đưa tệp tin vào vùng Staging Area
git add README.md

# Thực hiện commit đầu tiên với thông điệp rõ ràng
git commit -m "feat: init repository and configure local identity"
```

---

## 3. Kết quả kiểm tra & Chứng minh (Verification)

### 3.1. Kiểm tra cấu hình email cục bộ
```bash
git config --local user.email
```
**Kết quả:**
```text
Zeikezan12345@gmail.com
```

### 3.2. Kiểm tra cấu hình tên cục bộ
```bash
git config --local user.name
```
**Kết quả:**
```text
LLL
```

### 3.3. Kiểm tra toàn bộ cấu hình cục bộ (`--local --list`)
```bash
git config --local --list
```
**Kết quả:**
```text
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
user.name=LLL
user.email=Zeikezan12345@gmail.com
```

### 3.4. Kiểm tra lịch sử Commit (`git log --oneline`)
```bash
git log --oneline
```
**Kết quả:**
```text
09cd283 feat: init repository and configure local identity
```

---

## 4. Kết luận
- Repository đã được khởi tạo thành công ở local.
- Cấu hình danh tính tác giả (`user.name`, `user.email`) được lưu đúng trong file cấu hình cục bộ (`.git/config`) mà không tác động đến global config.
- Đã thực hiện thành công commit đầu tiên và sẵn sàng đẩy lên kho lưu trữ từ xa.
