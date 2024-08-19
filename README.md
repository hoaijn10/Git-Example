# Hướng dẫn sử dụng Git và GitHub cơ bản

## Git

1. Download Git (tại đây)[https://git-scm.com/download/win] 

2. Cài đặt Git

3. Mở cmd (Command Prompt) để kiểm tra
```bash
git --version
```

4. Config name và mail cho Git (chỉ cần config khi lần đầu tiên cài đặt Git)
```bash
git config --global user.name "hoaideptryvcl"
git config --global user.email "hoaideptryvcl@example.com"
```

5. Khởi tạo git repo cục bộ (tại thư mục cần tạo ví dụ D:/Example/)
```bash
git init
```

6. Thêm các thay đổi vào Staging Area
```bash
git add <ten_file>
```
hoặc
```bash
git add .
```
**Thay `<ten_file>` bằng tên file trên thực tế ví dụ `git add main.cpp`**

**`git add .` sẽ thêm toàn bộ file có thay đổi (so với commit gần nhất) vào staging area**

7. Commit các thay đổi vào local repo
```bash
git commit -m "commit message"
```
**Thay `commit message` bằng commit message trên thực tế, ví dụ `git commit -m "add README.md"`**

8. Tạo remote repo trên GitHub (public)

**Lưu ý: để cho dễ thì tạm thời cứ tạo repo public thôi để dễ connect**

Sau đó copy lại url của remote repo, ví dụ: https://github.com/hoaideptryvcl/example.git

9. Kết nối Local với Remote

```bash
git remote add origin <repo_url>
```
**Thay `<repo_url>` bằng repo url trên thực tế**

ví dụ `git remote add origin https://github.com/hoaideptryvcl/example.git`

10. Push từ local lên remote
```bash
git push -u origin main
```
cho lần push đầu (lần đầu của repo này thôi, repo khác thì lại phải như này)
```bash
git push
```
cho các lần push sau

**Nếu sau này có thay đổi gì chỉ cần lần lượt thực hiện 3 bước, `git add`, `git commit`, và `git push`**

Ví dụ
```bash
git add main.cpp
git commit -m "add main.cpp"
git push
```