# Hướng dẫn sử dụng Git và GitHub cơ bản

## Git & GitHub

1. **Tải Git**  
   Tải Git từ trang chính thức: [Tải Git cho Windows](https://git-scm.com/download/win)

2. **Cài đặt Git**  
   Tiến hành cài đặt Git bằng cách làm theo hướng dẫn trên màn hình.

3. **Kiểm tra cài đặt**  
   Mở Command Prompt (cmd) và nhập lệnh sau để kiểm tra phiên bản Git:
   ```bash
   git --version
   ```

4. **Cấu hình thông tin người dùng** (Chỉ cần thực hiện khi cài đặt Git lần đầu)
   ```bash
   git config --global user.name "Tên của bạn"
   git config --global user.email "email@example.com"
   ```

5. **Khởi tạo kho lưu trữ (repository) Git cục bộ**  
   Di chuyển đến thư mục mà bạn muốn khởi tạo repo (ví dụ: D:/Example/) và nhập:
   ```bash
   git init
   ```

6. **Thêm thay đổi vào Staging Area**  
   Thêm một tệp cụ thể vào Staging Area:
   ```bash
   git add <tên_file>
   ```
   Hoặc thêm tất cả các tệp đã thay đổi:
   ```bash
   git add .
   ```
   **Lưu ý**:  
   - Thay `<tên_file>` bằng tên tệp thực tế, ví dụ: `git add main.cpp`.
   - Lệnh `git add .` sẽ thêm tất cả các tệp đã thay đổi (so với commit gần nhất) vào Staging Area.

7. **Commit các thay đổi**  
   Lưu các thay đổi vào local repository:
   ```bash
   git commit -m "Nội dung commit"
   ```
   **Lưu ý**: Thay `"Nội dung commit"` bằng thông điệp commit thực tế, ví dụ: `git commit -m "Thêm README.md"`

8. **Tạo kho lưu trữ (repository) trên GitHub**  
   - Truy cập GitHub và tạo một repo mới (khuyến nghị chọn chế độ public để dễ kết nối).
   - Sao chép URL của repo vừa tạo, ví dụ: `https://github.com/username/example.git`.

9. **Kết nối repo cục bộ với repo trên GitHub**  
   Sử dụng lệnh sau để kết nối:
   ```bash
   git remote add origin <repo_url>
   ```
   **Lưu ý**: Thay `<repo_url>` bằng URL repo thực tế, ví dụ: `git remote add origin https://github.com/username/example.git`

10. **Push từ local lên GitHub**  
    Thực hiện lệnh sau để push lần đầu:
    ```bash
    git push -u origin main
    ```
    Với các lần push sau, chỉ cần thực hiện:
    ```bash
    git push
    ```

    **Lưu ý**: Sau khi có thay đổi mới, bạn chỉ cần thực hiện lại ba bước: `git add`, `git commit`, và `git push`.

    Ví dụ:
    ```bash
    git add main.cpp
    git commit -m "Thêm main.cpp"
    git push
    ```
